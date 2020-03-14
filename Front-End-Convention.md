## Front-End-convention
This is the Front end coding convention for Journey Horizon developers. Please read it kindly and carefully.


## Update Brand, Colors and Icons

### Set up favicon icons
1. Open https://realfavicongenerator.net/
2. Upload your original icon image
3. Configure platform specific icons
  Note: Remember to set the "Theme color" in the Android Chrome section
4. Configure the paths to use /static/icons/ as the root path of the icons
5. Generate the icons
6. Unzip the favicons.zip archive and replace the default icons and files in public/static/icons/ with the new icons
7. Replace the default HTML snippet in public/index.html with the snippet from the generator.
  Note: Remove the manifest link from the snippet as we have a default manifest with extra data compared to the generated one. You can edit the default file as you wish.
8. The map marker icon in the listing can be found in **public/static/icons/map-marker-32x32.png**. The dimensions should be 32x32 pixels, so the **favicon-32x32.png** file can be used to copy and rename the new one to **map-marker-32x32.png** to create a map icon.

```html
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="manifest" href="/site.webmanifest">
<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#5bbad5">
<meta name="apple-mobile-web-app-title" content="Journey Horizon">
<meta name="application-name" content="Journey Horizon">
<meta name="msapplication-TileColor" content="#00aba9">
<meta name="theme-color" content="#ffffff">
```

```html should be
<link rel="apple-touch-icon" sizes="180x180" href="/static/icons/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/static/icons/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/static/icons/favicon-16x16.png">
<link rel="mask-icon" href="/static/icons/safari-pinned-tab.svg" color="#5bbad5">
<meta name="apple-mobile-web-app-title" content="Journey Horizon">
<meta name="application-name" content="Journey Horizon">
<meta name="msapplication-TileColor" content="#00aba9">
<meta name="theme-color" content="#ffffff">
```

## Ref
https://www.sharetribe.com/docs/guides/how-to-change-ftw-icons/
