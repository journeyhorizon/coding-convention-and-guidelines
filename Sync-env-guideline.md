# How To SYNC-ENV - Journey Horizon Guideline

Do you think it would be a good idea for us to have a centralized .ENV management area instead of store it in localfile? This way, we could assign permissions based on teams, and each team would have access to their own ENV files without having to worry about sharing them or using incorrect ENV files due to a lack of synchronization between team members. We wouldn't have to send ENV files via Discord or any other platform to avoid fragmentation. Developers could simply call the CLI to retrieve the live ENV files and use them in their projects.

I think this idea is pretty cool, what do you think?

The idea look like this, but I think we can do with our current approach: Secret Manager

-----------

## Why should we do it:

Centralizing our ENV variable management is important for security reasons. Storing ENV files in a centralized location with restricted access ensures that only authorized personnel can access sensitive information. This reduces the risk of information leaks, accidental exposure, or misuse of confidential data. In addition, it allows us to monitor and track who has access to our ENV files and when they are accessed, providing an added layer of security.

-----------


## Here is how to work with it.

1. First you need to install aws cli:

    https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html


2. Use aws cli to setup profile:

    - Access to aws console -> secret manager (Mostly in JH's AWS, sometimes in client's aws console).

    - Get aws secret manager region, aws_access_key_id, aws_secret_access_key.

    - Setup aws profile in your local machine by using Cli:
        ```
        aws configure --profile
        ``` 
        Then fullfill all info, and using output=json
    
    - Or you can open ~/.aws/credentials (Most of MacOS default settings) and input:
        ```
        [envProfile]
        aws_access_key_id=Input here
        aws_secret_access_key=Input here
        region=Input here
        ```

3. In /scripts directory of the project, create json2env.js file with content:
    ```js
    const fs = require('fs');
    const inputFilePath = process.argv[2];
    const outputFilePath = process.argv[3];

    const run = () => {
    const fileContent = fs.readFileSync(inputFilePath, 'utf8');
    const env = JSON.parse(fileContent);
    const content = Object.entries(env).reduce((envResult, keyPair) => {
        const [key, value] = keyPair;
        return envResult + `${key}=${value}\n`;
    }, '');

    fs.writeFileSync(outputFilePath, content);
    };

    run();
    ```

4. Add this line into local project's package.json, at the bottom of scripts part:

    ```json
    "sync-env": "rm -f .env && aws secretsmanager get-secret-value --secret-id [Secret Id (ARN) of project in Secret Manager] --region=ap-southeast-1 --query SecretString --output text --profile=[Input your env profile name] > .env.json && node ./scripts/json2env.js .env.json .env && rm -f .env.json"
    ```

5. Before you run a project, you can run this command:

    ```
    yarn sync-env

    or 

    npm run sync-env
    ```

    to pull ENV from Secret Manager into .env file of yoru project.

6. If you want to test env in your own local machine and not want to share (Maybe becasue your feature are not ready to release or share) you can create a .env.local file and input your customize variables and it will combine with .env from Secret Manager.

    For example:

    .env.local
    ```
    MY_CUSTOM_ENV=123
    MY_CUSTOM_ENV_2=567
    ```

7. Remember to ignore .env.* file

8. Remember to update ENV variables into Secret Manager after you finalize your feature to help others developers sync with env.
