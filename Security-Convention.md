
# Security Convention - Journey Horizon Guideline

The Security Convention in Journey Horizon is a set of guidelines and protocols that are to be followed by each and every member of the organization. The purpose of this convention is to ensure the highest level of security for both our clients and the company itself.

The convention is a comprehensive framework that covers all aspects of security, including data protection, physical security, cybersecurity, and personnel security. The guidelines outline best practices for securing sensitive information, preventing unauthorized access, and protecting against cyber attacks.

All employees are expected to adhere to these guidelines at all times, and the company provides regular training and resources to ensure that everyone is up-to-date with the latest security protocols. In addition, the convention is regularly reviewed and updated to reflect any new threats or developments in the field of security.

By following the Security Convention, Journey Horizon can provide its clients with the assurance that their data and assets are being protected to the highest standards, and that the company is taking every measure possible to safeguard against security breaches.



## Part I - General rules

By following these security conventions, every member of Journey Horizon can ensure the high security level for our clients and company.

### 1. Passwords 

Every member of Journey Horizon should ensure that their working passwords are strong, unique, and not shared with anyone. 

- Use a mix of characters: A strong password should contain a mix of uppercase and lowercase letters, numbers, and symbols.

- Avoid using common words: Avoid using common words, phrases, or easily guessable information such as your name, date of birth, or address.

- Use longer passwords: Longer passwords are more secure. Aim for at least 12 characters or more.

- Avoid using dictionary words: Avoid using words found in the dictionary or common phrases. Instead, use a combination of words or random characters that are not easily guessable.

### 2. Two-Factor Authentication

Every member should enable two-factor authentication for all accounts that support it, including email, social media, and work-related accounts. Two-factor authentication provides an additional layer of security by requiring a second factor, such as a text message or an authentication app, in addition to a password.

Do not send secret code generated by two-factor authentication app to anyone without your control.

You can use Google Anthenticator or Authy or any other legit app.

### 3. Data Encryption

If you have to send sensitive data through internet to clients, please use secure protocal with encryption method to transit. Encryption ensures that even if data is intercepted, it will be unreadable to unauthorized individuals. Members should use encryption protocal such as HTTPS, SSL/TLS, and VPNs to encrypt data.

### 4. Regular Updates and Patches

Members should keep all devices, software, and systems up to date with the latest patches and updates when old versions get a security issues. This helps to protect against known vulnerabilities and exploits.

### 5. Awareness of Phishing Scams

Members should be vigilant against phishing scams, which are attempts to trick individuals into revealing sensitive information such as passwords or credit card details. Members should not click on links or download attachments from unknown sources, and should report any suspicious emails or messages to the appropriate person or team.

### 6. Secure Communication Channels

Members should use secure communication channels such as encrypted messaging apps or secure email platforms when transmitting sensitive information. They should also ensure that the recipient of the information is authorized to receive it and that the information is transmitted securely.

### 7. Physical Security

Members should ensure that their work environment is physically secure, with locked doors and windows and restricted access to sensitive areas. They should also be aware of their surroundings and report any suspicious activity or individuals.

## Part II - Protect Sensitive data rules

These actions aim to ensure the highest level of safety for our customers and to ensure that you do not unintentionally cause difficult security issues later on.

### 1. Env data

Please store all project environments variables on the secret manager (including projects that self-host environments on Heroku or on their own AWS, we should also have a copy in the company's Secret Manager and ensure it is synchronized with the customer's side).

You can read Sync-env Guideline to know how to have good practice with env: https://github.com/journeyhorizon/coding-convention-and-guidelines/blob/master/Sync-env-guideline.md

### 2. Team secret

All keys and team-specific secret information (shared flex console accounts, team-specific course accounts, shared Google API accounts, etc.) should be stored on the team's **SECRET MANAGER** on the company's AWS (the secret manager has the format: ***team-secret/your-team-name***, which has been created for each team). These pieces of information should not be stored on the company's Wiki anymore. ***Within 48 hours from this notification (09:00 04/05/2023), all key and secret information about the team on the Wiki will be deleted***.

If you want to store more secret data for each project (Which is not env variables) you can create secret manager with this format ``team-secret/your-team-name/project-name`` and add tag ``team=your-team-name``

### 3. Store pem file

In regards to files containing security signatures and secret documents such as PEM files (used to SSH into EC2 instances or other remote machines), certificate files, P12 files, client's business secret, etc., we will store them on the company's AWS S3 storage.
Each team will have a default bucket in the form of:

```
team-[your-team-name]-secret 
(for example: team-yang-secret)
```

This bucket will only be visible to members of the team. Additionally, teams can create additional buckets for their team in the form of: 

```
team-[your-team-name]-[whatever-you-want] 
(for example: team-mobi-app-only), which only 
```

the team members will have access to.

### 4. Sensitive data not from your working team

**ABSOLUTELY DO NOT USE** api keys from other projects for any purpose in the project you are working on. If in some rare, exceptional cases, it is necessary to check security or correlation, it is **MANDATORY** to inform the PM of the team managing the project you want to use the api key for and receive permission. If not approved, do not use it. At the same time, inform your own team's PM to be aware of the situation."

### 5. Working with Public key

When a customer's keys are set up as public keys (used for client-side functionalities such as displaying maps, searching locations, using promo codes, etc.), it is mandatory to have a restricted domain, API rate limit, and restricted API functions (only open the functions that are needed).

### 6. Working with Secret key

Secret keys should be stored in the Secret Manager and **ABSOLUTELY** should not be placed or stored in a public location that is accessible to many people.





