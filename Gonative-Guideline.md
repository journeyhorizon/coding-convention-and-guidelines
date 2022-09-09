# HOW TO GONATIVE - JOURNEY HORIZON GUIDELINE

Hello JHers, we know that, to develop a project with both web and mobile platform may cost our clients double budget and we need two teams (Mobile and Web) to manage a project at a same time (It may lead to complex process with small project and we have to spend a lot of time to sync between teams). That the reason why GoNative appear and resolve some of our problems.

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
- [Resources](#resources)
- [FAQ](#faq)
    - [How can I use camera to capture image or get images from Gallery](#how-can-i-use-camera-to-capture-image-or-get-images-from-gallery)
    - [How can I use QRCode in web?](#how-can-i-use-qrcode-in-web)


----------------------------------------


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


----------------------------------------


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


----------------------------------------


# Why GoNative?

## Build in minutes

Create your app in minutes using the GoNative App Builder. Preview in our browser-based simulators or download to test on a physical device.

## Get source code

The source code for your app can be downloaded at any time. GoNative’s iOS and Android codebase is also available on GitHub.

## Many plugins

As you can see there are many plugins for you to select and use


----------------------------------------


# Resources

- Example app: https://gonative.io/examples
- Plugins: https://gonative.io/plugins
- Pricing: https://gonative.io/pricing
- Document: https://gonative.io/docs


----------------------------------------


# FAQ

### How can I use camera to capture image or get images from Gallery

- You can use capture attribute of input tag in html https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/capture or https://web.dev/media-capturing-images/
- Remember to grant camera permission and declare why you use camera in iOS XCode Project.

### How can I use QRCode in web?

- You can use QRCode package for Reactjs (an example: https://www.npmjs.com/package/qrcode.react)
- Remember to grant camera permission and declare why you use camera in iOS XCode Project.

