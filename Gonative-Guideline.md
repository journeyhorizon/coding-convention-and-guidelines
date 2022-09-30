# HOW TO GONATIVE - JOURNEY HORIZON GUIDELINE

Hello JHers, we know that developing a project with web and mobile platforms may cost our clients double the budget. We need two teams (Mobile and Web) to manage a project simultaneously (It may lead to a complex process with a small project, and we have to spend a lot of time syncing between teams). That is the reason why GoNative appears and resolves some of our problems.

- [HOW TO GONATIVE - JOURNEY HORIZON GUIDELINE](#how-to-gonative---journey-horizon-guideline)
- [What is GoNative?](#what-is-gonative)
- [How to convert your website into a native app with GoNative](#how-to-convert-your-website-into-a-native-app-with-gonative)
  - [1) Build & Preview](#1-build--preview)
  - [2) Configure & Customize](#2-configure--customize)
    - [Overview](#overview)
    - [Branding](#branding)
    - [Navigation](#navigation)
    - [Link handling](#link-handling)
    - [Interface](#interface)
    - [Website overrides](#website-overrides)
    - [Permission](#permission)
    - [Push notification](#push-notification)
    - [Native plugins](#native-plugins)
    - [Build and test](#build-and-test)
    - [License](#license)
  - [3) Publish & Launch](#3-publish--launch)
    - [Buy a license](#buy-a-license)
    - [Apple Developer Account](#apple-developer-account)
- [GoNative APIs - Easily add powerful native features without writing native code](#gonative-apis---easily-add-powerful-native-features-without-writing-native-code)
    - [Device Info: https://gonative.io/docs/device-info](#device-info-httpsgonativeiodocsdevice-info)
    - [Clipboard: https://gonative.io/docs/clipboard](#clipboard-httpsgonativeiodocsclipboard)
    - [Prompt Share Dialogue: https://gonative.io/docs/prompt-share-dialogue](#prompt-share-dialogue-httpsgonativeiodocsprompt-share-dialogue)
    - [Download File: https://gonative.io/docs/download-file](#download-file-httpsgonativeiodocsdownload-file)
    - [App Settings: https://gonative.io/docs/app-settings](#app-settings-httpsgonativeiodocsapp-settings)
    - [Clear Webview Cache: https://gonative.io/docs/clear-webview-cache](#clear-webview-cache-httpsgonativeiodocsclear-webview-cache)
- [Why GoNative?](#why-gonative)
  - [Build in minutes](#build-in-minutes)
  - [Get source code](#get-source-code)
  - [Many plugins](#many-plugins)
- [Development Process With GoNative Mobile App](#development-process-with-gonative-mobile-app)
  - [Gonative development process](#gonative-development-process)
- [Resources](#resources)
- [FAQ](#faq)
    - [How can I use camera to capture image or get images from Gallery](#how-can-i-use-camera-to-capture-image-or-get-images-from-gallery)
    - [How can I use QRCode in web?](#how-can-i-use-qrcode-in-web)
    - [Should we use WebToNative instead of GoNative?](#should-we-use-webtonative-instead-of-gonative)
<br/>
<br/>

----------------------------------------
<br/>

# What is GoNative?

- GoNative is a tool (run on web) which convert a website into a native app by using webView technique.
- Guaranteed Acceptance by the Apple App Store and Google Play.
- You only need to enter your website URL to build a native iOS and Android mobile app and preview immediately in your browser.

# How to convert your website into a native app with GoNative

Here below is step by step how to make your website into a mobile native application.

## 1) Build & Preview

- Click "Create A New App" on topbar menu or access this url "https://gonative.io/app"
<img src="https://drive.google.com/uc?export=view&id=1l_Ts-hBMnaZ0OzIqDjpf13rDl6eL78Yj" alt="Select create app buttom" data-canonical-src="https://drive.google.com/uc?export=view&id=1l_Ts-hBMnaZ0OzIqDjpf13rDl6eL78Yj" width="100%"/>

- Then you will see this page

<img src="https://drive.google.com/uc?export=view&id=1dPwkoEvCGDVk6WOphIHMVaG20iG1VoIs" alt="Create new app page" data-canonical-src="https://drive.google.com/uc?export=view&id=1dPwkoEvCGDVk6WOphIHMVaG20iG1VoIs" width="100%"/>

- Enter a URL, App name, and your contact email 

![Enter url](https://drive.google.com/uc?export=view&id=1Lxpz2p4rul4ihCLDEAmEDYspoKvJjpkh)

- Next, click "Start building my app" button (Green one) then within minutes the GoNative online app builder will create a native app that displays your web content.

![Video build app](https://drive.google.com/uc?export=view&id=1JaUF6q0KPL_YJzcOLQ1UHoApLwhci7hl)

- Now you are in app dashboard where you can update config, add app icon, splash screen for android, add navigation bar, grant permission, add more plugin.

- You can see on the left sidebar of dashboard is control list, where you can do action

![Left sidebar](https://drive.google.com/uc?export=view&id=1IMa0cpjUHSr7F_eI2QYYvBbl6K-AKkaG)

- Beside that you will also receive an email from GoNative about some details info: Link to Dashboard, Link to share demo app, licensing, documentation and your appConfig.json file.

![Email content](https://drive.google.com/uc?export=view&id=17fFWMp6zY0bgpvNQtfOgdUTbkmNNbKZx)

- Remember that **Private Management Link** is private link, do not share not public in any where, with this link anyone can get app source code and modify app configs.


## 2) Configure & Customize

Add your own app icon and branding, then configure push notifications and other features to optimize your app.
Should not Export source code before you finish config and cutomize your app in dashboard, because after any change in dashboard, you have to download a new source code and it take a lot of time for you to migrate changes (If you do any update directly into source code) from old source code to the new one.

### Overview

In overview page, you can change web site url, app name, contact email or app description

- Web site url: You can update to any web page you want. So don't worry if you input wrong url at the first time, you can update it.
- App name: You can update to any name you want. So don't worry if you input wrong name at the first time, you can update it.

### Branding

- **App Icon:** Your app icon is your app’s identity and is used on the device home screen and in other locations such as settings. Upload a PNG or JPG square image to use as your app's launch icon. Recommended resolution is 1024x1024 pixels.
  - If your image has transparency, it will be given a white background. For Android, a small rounding of the corners of your image will be applied. This same effect is automatically applied to your app icon on iOS by the operating system.
  - For more information about app icons on iOS review Apple’s guidelines and recommendations https://developer.apple.com/design/human-interface-guidelines/ios/icons-and-images/app-icon/.
  - For more information about app icons on Android review Google's guidelines and recommendations https://material.io/design/platform-guidance/android-icons.html#usage.
  - You should upload and save app Icon after you enter First Step (Build & Preview). 
 
- **Splash screen:** A splash screen is shown during the launch animation when a user launches your app from the home screen or switches back to it from a backgrounded state.
  - There are three options
    - App icon option: Use app icon as a picture of splash screen
    - New image: Add new image as a splash screen
    - Solid image: Use background color as aa splash screen.
  - In case splash screen on iOS not working please follow this documents: https://gonative.io/docs/ios-launch-images

- **Theme colors:** Set a Primary Color used for text fields and labels, and Status Bar Background Colors for your app. The Primary Color is also referred to as the Tint color for iOS and the Accent color for Android.

You may also customize and [dynamically set the status bar visibility and style during runtime](https://gonative.io/docs/dynamic-status-bar-styling) using the GoNative JavaScript Bridge.

### Navigation

You can setup navigation bar in the dashboard to make our app look more native.

Follow this document https://gonative.io/docs/native-navigation-overview if you need

### Link handling

Link handling settings control how links on pages displayed within your app open. You can also configure deep linking to set links pointing to your website in text messages, emails and on other webpages to open within your app.

Follow this document https://gonative.io/docs/link-handling-overview when you need.

### Interface

App Interface settings control the functionality of your app, allowing you to optimize the app versus website experience for your users.

Follow this document https://gonative.io/docs/app-interface-overview when you need.

### Website overrides

Web Overrides allow you to control how your website is presented within your app and how your app sends requests to your web server.

Follow this document https://gonative.io/docs/website-overrides-overview when you need.

### Permission

Some device hardware and functionality requires specific permissions from the user to access within your app. At times permission requirements can be configured to be prompted when the app is first opened or they can be prompted when required at runtime via the JavaScript Bridge.

Follow this document https://gonative.io/docs/permissions-overview when you need.

### Push notification 

GoNative supports a range of Push Notification providers. Our default provider is OneSignal and other providers can be added through custom development. Contact our team for more details.

Follow this document https://gonative.io/docs/push-notifications-overview when you need.

- We use OneSignal for notification so remember to have OneSignal account and also implement OneSignal for notification server

### Native plugins

GoNative’s expansive library of plugins supercharge your app with access to native device hardware, functionality, and third-party services.

Native Plugins are easily added to your iOS and Android apps without the need for mobile development. Plugins are accessed through the GoNative JavaScript Bridge, a powerful API that allows your website to communicate with and control your app.

Native Plugins may be purchased and added to your app during your initial license purchase or in the future as part of an app update. For pricing and to purchase visit https://gonative.io/pricing. To add a Native Plugin to an existing license use the License Management Link emailed to you during purchase.

Some Native Plugins require active subscriptions or licenses with third-party providers. GoNative is not responsible for the services provided by third parties or any future changes. For support of SDKs not found in our Native Plugin Library contact us for custom development.

Remember that if you want to use plugin, you have to purchase a license.

Follow this document https://gonative.io/docs/native-plugins-overview when you need.

### Build and test

- You can use online build system of GoNative to build and run app online to test
- Or you can download iOS or Android source code into your local machine then run and test. I reccomend download source.

Follow this document https://gonative.io/docs/gonative-build-platform when you need.

### License

Where you can buy license for app and plugins

## 3) Publish & Launch

Publish your app on the Apple App Store and/or the Google Play Store so users can find and download your app.

### Buy a license

Before build and deploy to appstore/chplay remember to buy a license and add it to our dashboard, you can access License page in your dashboard to buy license or you can also add an existing license.

### Apple Developer Account

- Ask client to create Apple developer account (Organization account for faster approval from Apple)
- Invite our Apple dev account into their organize
- After join organize, please create App for client. If they want to have test env for app, create 2 app - one for test one for prod. 
- Before publish app, full fill all data in App Store Dashboard.
<br/>
<br/>

----------------------------------------
<br/>

# GoNative APIs - Easily add powerful native features without writing native code

The GoNative JavaScript Bridge is an API embedded in your app that allows your website to dynamically control and configure your app, and access the mobile device native functionality and hardware.

There are two ways to use the JavaScript Bridge. You can use the JavaScript Bridge Library which provides an abstraction layer and helper JavaScript functions or alternatively you can use the GoNative Protocol to access the JavaScript Bridge directly.

Follow this document https://gonative.io/docs/gonative-javascript-bridge when you need.

### Device Info: https://gonative.io/docs/device-info

### Clipboard: https://gonative.io/docs/clipboard

### Prompt Share Dialogue: https://gonative.io/docs/prompt-share-dialogue

### Download File: https://gonative.io/docs/download-file

### App Settings: https://gonative.io/docs/app-settings

### Clear Webview Cache: https://gonative.io/docs/clear-webview-cache
<br/>
<br/>

----------------------------------------
<br/>

# Why GoNative?

## Build in minutes

Create your app in minutes using the GoNative App Builder. Preview in our browser-based simulators or download to test on a physical device.

## Get source code

The source code for your app can be downloaded at any time. GoNative’s iOS and Android codebase is also available on GitHub.

## Many plugins

As you can see there are many plugins for you to select and use
<br/>
<br/>

----------------------------------------
<br/>

# Development Process With GoNative Mobile App

- As you know, our current process when develop a web/mobile app is separating two Environments (Test env and Production env) which related to two Apps (Test app and Production app). It helps us a lot and reduce many complexity problems when setup, implement features and integrete third parties. 

- With Mobile development process, we have two bundle_app_id related to two apps. Example: com.app.helloWorld.test for Test app, com.app.helloWorld for Production app. One bundle_app_id can only stick with one app.

- However with GoNative, there faced a big problem: One GoNative License can only use for only one bundle_app_id, so our current process got stuck.
Someone will tell me why don't you add license for Production app and leave Test app as a free version. Hmmm, I tried it mate, and here is the frustrated thing:

<center><img src="https://drive.google.com/uc?export=view&id=1jQwxOATA9eiSt5iy_Pr_810aczgQZIjt" alt="Error with free version" data-canonical-src="https://drive.google.com/uc?export=view&id=1jQwxOATA9eiSt5iy_Pr_810aczgQZIjt" width="40%"/></center>

- Here is two main reasons why I don't use this method approach:
  - It will show Alert popup (Like above) many times to warn you when using test app.
  - With the free version, after a while of using the app, your app will close automatically.
- All these experiences leave our customers unsatisfied.

After many restless nights, I found a new process that can show us the light.

## GoNative development process

- We only need to create 1 app with 1 bundle_app_id
- For test app: You can checkout code to master, merge feature branch to master (If we change in native code or add new purchased plugin), then change url in appConfig.json => general.initialUrl to test site url, rebuild app and push to TestFlight/FirebaseAppTest.

<center><img src="https://drive.google.com/uc?export=view&id=1QTZ9u2_0-KwRNxZd9qLq6vRkSScvyOwb" alt="Error with free version" data-canonical-src="https://drive.google.com/uc?export=view&id=1QTZ9u2_0-KwRNxZd9qLq6vRkSScvyOwb" width="45%"/><img src="https://drive.google.com/uc?export=view&id=175Rrz8_qOVJPxrAuMgTwxbR-GxEVEtmO" alt="Error with free version" data-canonical-src="https://drive.google.com/uc?export=view&id=175Rrz8_qOVJPxrAuMgTwxbR-GxEVEtmO" width="45%"/></center>

- If everythings look good, you can checkout to production, merge feature branch to production (If we change in native code or add new purchased plugin) then change url in appConfig.json => general.initialUrl to production site url, rebuild app and push to TestFlight/FirebaseAppTest and then submit to AppStore/CHPlay.

- How can I use Test App when my latest app version is using production url? For example: My latest app version is 30 and it is production url version. You can find nearest previous version which is using test url to download and use. Or you can deploy a brand new version using test url.
<br/>
<br/>

----------------------------------------
<br/>

# Resources

- Example app: https://gonative.io/examples
- Plugins: https://gonative.io/plugins
- Pricing: https://gonative.io/pricing
- Document: https://gonative.io/docs
<br/>
<br/>

----------------------------------------
<br/>

# FAQ

### How can I use camera to capture image or get images from Gallery

- You can use capture attribute of input tag in html https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/capture or https://web.dev/media-capturing-images/
- Remember to grant camera permission and declare why you use camera in iOS XCode Project.

### How can I use QRCode in web?

- You can use QRCode package for Reactjs (an example: https://www.npmjs.com/package/qrcode.react)
- Remember to grant camera permission and declare why you use camera in iOS XCode Project.

### Should we use WebToNative instead of GoNative?

- It depends on your demand; if you only need to wrap your website into a web-view to show as an app with some native plugins without modifying complex things and a meager price, you can use WebToNative (Only $80 to have an app). However, customer support is poor and slow.
- If you need more than the above, you can consider GoNative (much more expensive than WebToNative, $800 to have an app). However, you have many valuable things: A various plugins library, a good UI/UX dashboard with hundreds of configurations in which you can do so much customization, and you own your source code into which you can inject your code into the source. A big plus is customer support.
- For me, I highly recommend you use GoNative. Everything has its price.
- Here is the compare table

- Customer support:
  - GoNative: Good. 
  - WebToNative: Bad and Slow. Some questions they did not give us answers
- Features:
  - WebToNative:
    - Both:
      - Mobile Push Notification: Send unlimited push notifications with OneSignal.com.
      - Earn From Ads: Wherever you are, whatever your app can do, AdMob can help you grow lasting revenue.
      - Launch Screen Animation: You can add lottie animation, it will be shown when user open the app.
      - Splash screen: Launch Screen when user open app
      - Downloads & Uploads: Download and Upload options are enabled for your app.
      - Media Playback: Your app will be able to record and play videos same as music and audio.
      - Pull To Refresh: Refresh your pages with just a swipe down gesture. You can also use this layout to indicate page loading.
      - App Linking & Sharing: Linking to other applications and even link to a web browser.
      - No Internet Connection UI: The app shows a beautiful No Connection screen when the user is not connected to internet.
    - Android:
      - Playstore Publishing Services.
      - HUAWEI Publishing Services.
      - Social Login.
      - Custom Sound for Notification.
      - Touch ID / Biometric Authentication.
      - Facebook App Events.
      - AppsFlyer.
      - Barcode Scanning.
      - Bottom Navigational Tab.
    - iOS:
      - App Store Publishing Services.
      - Social Login.
      - Touch ID / Face ID / Biometric Authentication.
      - Facebook App Events.
      - AppsFlyer.
      - Barcode Scanning.
      - Bottom Navigational Tab.
      - Native Contacts.
      - In-App Purchases (IAP).
      - In App Review.
      - Background Location.

  - Gonative: 
    - All things here [2) Configure & Customize](#2-configure--customize) and here [GoNative APIs - Easily add powerful native features without writing native code](#gonative-apis---easily-add-powerful-native-features-without-writing-native-code). Beside that, it has many native plugins list below
    - AdMob Native Ads: Google's AdMob platform displays native banner and interstitial ads which provide an enhanced user experience and result in increased monetization versus ads displayed through your website. [Read more](https://gonative.io/docs/admob-native-ads)
    - Native Media Player: Play audio natively on iOS and Android with playback controls and track information displayed on the device lock screen. Use for audiobook, podcast, e-learning, radio apps, etc. [Read more](https://gonative.io/docs/native-media-player)
    - Social Login: Provide a seamless native login experience for your users with any combination of Facebook Login, Google Sign-in and Sign in with Apple. The login process is facilitated through the respective native SDKs rather than the webview. If the user is already logged into an account their login completes automatically, avoiding the need to manually enter username and password details. [Read more](https://gonative.io/docs/social-login)
    - Facebook App Events: Collect analytics, measure Facebook Ad performance, and build audiences for Facebook Ad targeting. Supports standard events such as App Install and App Launch as well as custom events. [Read more](https://gonative.io/docs/facebook-app-events)
    - Native Contacts: Load contacts directly from the device address book to simplify form completion or data collection. Search for contacts via queries or retrieve all contacts in bulk. [Read more](https://gonative.io/docs/native-contacts)
    - Google Firebase Analytics: Harness the power of the Google Analytics platform and add native event tracking and usage analytics. Supports default app events such as app start and app usage, as well as custom events. [Read more](https://gonative.io/docs/firebase-analytics)
    - Local Settings: Save app settings and other data directly to the user's device using iOS Apple Keychain and Android SharedPreferences. If the user is logged into the device the data will persist throughout app upgrade and uninstall/reinstall. [Read more](https://gonative.io/docs/local-settings)
    - Haptics: Trigger haptic vibration effects to provide feedback to end users based on various events and actions within your app. Support for six different haptic effects that have been specifically designed to be comparable across iOS and Android devices. [Read more](https://gonative.io/docs/haptics)
    - Share into app : Allow your users to share data such as URL links from other apps installed on their device. Your app will appear in the list of available target apps and actions when they invoke the "Share" menu. [Read more](https://gonative.io/docs/share-into-app)
    - Document Scanner: Easily scan documents via the device camera using image processing to automatically enhance and optimize the scanned image. Streamline document uploads from customers and employees while reducing errors and missing information. [Read more](https://gonative.io/docs/document-scanner)
    - QR / Barcode Scanner: Scan QR Codes and Barcodes directly into your app via the device camera. Used for in-store retail shopping, warehouse management, data center operations, etc. [Read more](https://gonative.io/docs/qr-barcode-scanner)
    - Scandit QR / Barcode: Scan QR Codes and Barcodes directly into your app via the device camera. This plugin is similar to our basic version with additional functionality provided by Scandit. An active Scandit license is required. [Read more](https://gonative.io/docs/scandit-qr-barcode)
    - Background Location: Allow your app to run code in the background while subscribed to device location updates. Use the background process to perform data backup activities or send data/location to a remote server. [Read more](https://gonative.io/docs/background-location)
    - In-App Purchases: Accept payment within your app seamlessly using Apple and Google's IAP platform to facilitate in-app transactions such as one-time purchase, subscription, or promo code redemption. [Read more](https://gonative.io/docs/iap)
    - Secure Modal (Apple Pay): Some 3rd party JavaScript libraries such as the Apple Pay JS API require a secure iOS WKWebView window with external scripting blocked. GoNative's Modal Plugin allows the functionality provided by these libraries to work within your app. [Read more](https://gonative.io/docs/secure-modal)
    - Card.io: Simplify payment form completion using the device camera and machine vision to read any credit card. Hold your card in front of the card to capture cardholder name, card number and expiry date without typing. [Read more](https://gonative.io/docs/card-io)
    - Face ID/Touch ID Android Biometric: Provide your users with a seamless login experience using Apple's Face ID and Touch ID authentication and Android Fingerprint Authentication on supported devices. [Read more](https://gonative.io/docs/auth)
    - Calendar: Add events to the user's calendar from ics files and embedded calendar links. Prompt the user to add via a native interface form. Used for client service and shift scheduling apps. (iOS Only) [Read more](https://gonative.io/docs/native-plugins-overview)
    - App Review: Prompt your users to leave ratings and reviews for your Apple App Store and Google Play Store app listings. Build your app's profile and improve the discoverability of your app listing through positive ratings. [Read more](https://gonative.io/docs/native-plugins-overview)
    - Offline Downloads: Download document and media files to the user's device for online or offline access. Files are accessible through a built-in file manager UI as well as via the JavaScript Bridge. [Read more](https://gonative.io/docs/offline-download-manager)
    - Jailbreak/Root Detection: Improve app security and meet compliance requirements by detecting when your app is running on an insecure jailbroken iOS device or a rooted Android device. [Read more](https://gonative.io/docs/jailbreak-root-detection)
    - NFC Tag Scanner: Scan data from Near Field Communication (NFC) tags as part of in-store shopping experience, warehouse tracking, digital+physical game, or any similar use case. [Read more](https://gonative.io/docs/nfc-tag-scanner)
    - iBeacon: Add indoor location awareness and mapping capabilities to your app through the use of iBeacons and proximity scanning. [Read more](https://gonative.io/docs/ibeacon)
    - AppsFlyer: The AppsFlyer Native Plugin provides app installation and event recording functionality. You can record installs, updates, sessions, and in-app events. Recording these events can help you evaluate ROI and user quality. [Read more](https://gonative.io/docs/native-plugins-overview)
    - Kaltura Media Player: Play live and recorded video natively in your app using the Kaltura Player. Includes support for AirPlay and Chromecast streaming to compatible devices. [Read more](https://gonative.io/docs/kaltura-media-player)
    - Microsoft Intune: Add Microsoft Intune capabilities to your app to support Mobile Device Management (MDM) and Mobile Application Management (MAM) using the Microsoft Endpoint Manager. [Read more](https://gonative.io/docs/microsoft-intune)
    - Twilio: Add a native Twilio video chat interface to your app to provide your users a more seamless and integrated experience versus a web-based client. [Read more](https://gonative.io/docs/twilio)

  - As you can see, GoNative have much more feature and more detail than WebToNative in features.
- Source code:
  - GoNative allow us to download source code modify it by ourself if we want. And we can deploy to store by ourself
  - WebToNative did not allow us to export code and modify code. To publish app, we have to use their service.
- Documentation:
  - Gonative: Detail and easy to understand
  - WebToNative: Lack some info.
- Admin dashboard: 
  - Gonative: Very details and good UI/UX.
  - WebToNative: Very simple and not good.
