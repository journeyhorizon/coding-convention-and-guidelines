# How To Stripo - Journey Horizon Guideline

Hello JHers, as you know, creating an email template with pure HTML/CSS is a nightmare because we have to fix many bugs on Apple Mail, Outlook Mail, and some old Email clients. Especially when we work with transactional email, it takes a lot of time to implement, push settings, create a transaction and wait for the email to be sent to test. That is the reason why Stripo appears and resolves some of our problems.


**Table of content**:

- [How To Stripo - Journey Horizon Guideline](#how-to-stripo---journey-horizon-guideline)
- [What is Stripo](#what-is-stripo)
  - [Introduction](#introduction)
  - [Pricing](#pricing)
  - [How to access Stripo](#how-to-access-stripo)
  - [Upgrade Stripo account](#upgrade-stripo-account)
  - [Stripo features](#stripo-features)
    - [Modules Library](#modules-library)
    - [HTML & CSS Code Editor](#html--css-code-editor)
    - [Email Templates](#email-templates)
    - [Export Options](#export-options)
    - [AMP for Email](#amp-for-email)
    - [Customer Support](#customer-support)
    - [Brand Guidelines](#brand-guidelines)
    - [Stripo Translation](#stripo-translation)
    - [Custom Fonts](#custom-fonts)
    - [Email Annotations Builder](#email-annotations-builder)
    - [Data Service/Source](#data-servicesource)
    - [User Roles and Permissions](#user-roles-and-permissions)
- [Working with Stripo in Journey Horizon](#working-with-stripo-in-journey-horizon)
  - [Dashboard](#dashboard)
  - [Dig deeper with Stripo's HTML & CSS Code Editor](#dig-deeper-with-stripos-html--css-code-editor)
    - [1\. Editing one of the 550 prepared email templates](#1-editing-one-of-the-550-prepared-email-templates)
    - [2\. Coding your own one](#2-coding-your-own-one)
    - [3\. Starting one from scratch/Empty email](#3-starting-one-from-scratchempty-email)
    - [4\. General settings](#4-general-settings)
      - [Important to note:!Stripo How to Build Email with Stripo Email Background](#important-to-note)
      - [How to make general settings with Stripo:](#how-to-make-general-settings-with-stripo)
    - [5\. Setting headings](#5-setting-headings)
    - [How to set styles for Headings in emails with Stripo:](#how-to-set-styles-for-headings-in-emails-with-stripo)
    - [6\. Building header](#6-building-header)
      - [How to add logo to your emails with Stripo:](#how-to-add-logo-to-your-emails-with-stripo)
      - [Important to note:](#important-to-note-1)
      - [How to add a menu to your emails with Stripo:](#how-to-add-a-menu-to-your-emails-with-stripo)
      - [Important to note:](#important-to-note-2)
    - [7\. Working with text](#7-working-with-text)
      - [Important to mention:](#important-to-mention)
      - [How to add copy to your emails with Stripo:](#how-to-add-copy-to-your-emails-with-stripo)
      - [How to add links to text with Stripo:](#how-to-add-links-to-text-with-stripo)
      - [Important to note:](#important-to-note-3)
    - [8\. Personalizing copy](#8-personalizing-copy)
      - [How to add merge-tags in emails with Stripo:](#how-to-add-merge-tags-in-emails-with-stripo)
      - [Important to note:](#important-to-note-4)
    - [9\. Adding images](#9-adding-images)
      - [How to add an image in emails with Stripo:](#how-to-add-an-image-in-emails-with-stripo)
      - [Note:](#note)
      - [There are four ways of doing it:](#there-are-four-ways-of-doing-it)
        - [1\. Dropping/uploading image](#1-droppinguploading-image)
        - [2\. Pasting external URL](#2-pasting-external-url)
        - [3\. Using images from the personal gallery](#3-using-images-from-the-personal-gallery)
        - [4\. Using our bank of images](#4-using-our-bank-of-images)
    - [10\. Editing images](#10-editing-images)
      - [How to edit images with Stripo:](#how-to-edit-images-with-stripo)
    - [11\. Building banner](#11-building-banner)
      - [Important to mention:](#important-to-mention-1)
      - [How to build email banner with Stripo:](#how-to-build-email-banner-with-stripo)
      - [Please, be advised:](#please-be-advised)
      - [Important to note:](#important-to-note-5)
    - [12\. Image rollover effect](#12-image-rollover-effect)
      - [Important to note:](#important-to-note-6)
      - [How to build an image rollover effect with Stripo:](#how-to-build-an-image-rollover-effect-with-stripo)
    - [13\. Adding video in emails](#13-adding-video-in-emails)
      - [Way 1. Inserting URL link to your video](#way-1-inserting-url-link-to-your-video)
        - [How to set a custom thumbnail to video in emails:](#how-to-set-a-custom-thumbnail-to-video-in-emails)
        - [Important to note:](#important-to-note-7)
      - [Way 2. Embedding video](#way-2-embedding-video)
        - [We recommend sticking to the following order:](#we-recommend-sticking-to-the-following-order)
        - [How to embed this code in emails with Stripo:](#how-to-embed-this-code-in-emails-with-stripo)
      - [The very code to embed:](#the-very-code-to-embed)
      - [Customize the embed code:](#customize-the-embed-code)
    - [14.Adding CTA buttons](#14adding-cta-buttons)
      - [How to build a CTA button with Stripo.email:](#how-to-build-a-cta-button-with-stripoemail)
      - [Important to note:](#important-to-note-8)
    - [15\. Building products content modules](#15-building-products-content-modules)
        - [If you want to build one or two more modules similar to this one, you need to:](#if-you-want-to-build-one-or-two-more-modules-similar-to-this-one-you-need-to)
    - [16\. Building countdown timers for emails](#16-building-countdown-timers-for-emails)
      - [How to build and add countdown timer in emails with Stripo:](#how-to-build-and-add-countdown-timer-in-emails-with-stripo)
    - [17\. Adding spacer](#17-adding-spacer)
      - [How to set spacer in emails with Stripo:](#how-to-set-spacer-in-emails-with-stripo)
    - [18\. Inserting social networking](#18-inserting-social-networking)
      - [How to add social media icons with Stripo:](#how-to-add-social-media-icons-with-stripo)
      - [Important to note:](#important-to-note-9)
    - [19\. Building email footer](#19-building-email-footer)
      - [How to build email footer with Stripo:](#how-to-build-email-footer-with-stripo)
    - [20\. Background color and image](#20-background-color-and-image)
      - [Setting background color to a structure](#setting-background-color-to-a-structure)
      - [How to set a background color for a structure:](#how-to-set-a-background-color-for-a-structure)
      - [How to set a background image for entire email:](#how-to-set-a-background-image-for-entire-email)
      - [Important to note:](#important-to-note-10)
    - [21\. Writing subject line](#21-writing-subject-line)
      - [How to write a subject line for your emails with Stripo:](#how-to-write-a-subject-line-for-your-emails-with-stripo)
    - [22\. Settings for email rendering on mobile devices](#22-settings-for-email-rendering-on-mobile-devices)
      - [How to set preferences for mobile view:](#how-to-set-preferences-for-mobile-view)
    - [23\. Building AMP emails](#23-building-amp-emails)
      - [Important:](#important)
    - [24\. Optional email elements](#24-optional-email-elements)
      - [Interactive elements in emails](#interactive-elements-in-emails)
      - [Important to mention:](#important-to-mention-2)
      - [Gmail Promotion Annotations Builder](#gmail-promotion-annotations-builder)
      - [AMP-powered emails](#amp-powered-emails)
    - [25\. Previewing and testing your emails](#25-previewing-and-testing-your-emails)
      - [How to preview your email with Stripo:](#how-to-preview-your-email-with-stripo)
      - [How to send test email with Stripo:](#how-to-send-test-email-with-stripo)
      - [How to preview your emails across all popular environments](#how-to-preview-your-emails-across-all-popular-environments)
    - [26\. Exporting email to your ESP](#26-exporting-email-to-your-esp)
      - [How to export your email from Stripo:](#how-to-export-your-email-from-stripo)
      - [Important:](#important-1)
      - [Undo button](#undo-button)
      - [Versioning](#versioning)
      - [Copying and moving elements](#copying-and-moving-elements)
      - [Storing modules](#storing-modules)
      - [Storing and reusing existing templates](#storing-and-reusing-existing-templates)


--------------------------
<br/>

# What is Stripo

## Introduction

- Website url: https://stripo.email/
- Stripo is an Email Design Platform: free Drag-n-Drop online email template tool has everything you need for creating email messages of any complexity fast, with no limits and no coding skills

## Pricing

- It has 5 Pricing plans depending on your demand and business size.
- Here is each plan:

    <img src="https://drive.google.com/uc?export=view&id=1AyF_BEzdwCk3sSsWehxqD9iTZLwn1hdi" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=1AyF_BEzdwCk3sSsWehxqD9iTZLwn1hdi" width="75%"/>

<br/>

## How to access Stripo

Our company has **Stripo account** (Medium Plan), you can access it in<br/>
`JH Wiki => Projects => JH-General-Info`<br/>
(Here is the link: [JH general link](https://sites.google.com/journeyh.io/wiki/projects/jh-general-info))<br/>
You can login and use it. [How to create email template in our company Stripo account](#Link-here)

- Access Stripo in this link: https://stripo.email/
- On the topbar of Stripo Home Page, click "**Sign in ->**" button (On most right of topbar)

    <img src="https://drive.google.com/uc?export=view&id=1YnKvs2ostr2nrCxrCmVob3-jQ4Kw2uaK" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=1YnKvs2ostr2nrCxrCmVob3-jQ4Kw2uaK" width="100%"/>

- You will need to full fill credential to login. If you don't have an account, you can sign up by click **Get started** link

    <img src="https://drive.google.com/uc?export=view&id=1CZ1gnSgF2GoCXIZ1ZFfCPqUCdblKKYjr" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=1CZ1gnSgF2GoCXIZ1ZFfCPqUCdblKKYjr" width="75%"/>

- To sign up, you enter data into this form, 

    <img src="https://drive.google.com/uc?export=view&id=1xEjV6a2ZOMMkM3xTeKejGHKmvwvEjKVx" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=1xEjV6a2ZOMMkM3xTeKejGHKmvwvEjKVx" width="75%"/>

- Then you will recieve a verify email to verify your account. Follow email instruction.

## Upgrade Stripo account

You can first test with a free plan (Export to HTML source 4 times a month, send to test email 10 times a day, using free templates and limit to create a small number of templates). You can upgrade to a higher plan if your demand is high.

- After you log in to Stripo, you will see on the topbar menu a button called "**Upgrade**", you can click it to open the upgrade dialog. Or you can click on the avatar thumbnail on most right of the topbar to open a menu, there is another "**Upgrade**" button inside it.

    <img src="https://drive.google.com/uc?export=view&id=1hYCCZqFRn__8ytUDLGEeEUVPg6HvBC1I" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=1hYCCZqFRn__8ytUDLGEeEUVPg6HvBC1I" width="50%"/>

- In upgrade dialog, you can select "**Billed Anually**" for better price, but if you only need to test to have a finally decision, you can select "**Billed Monthly**". Then select a plan you want.

    <img src="https://drive.google.com/uc?export=view&id=10WvZf1XfdFhN0-YNqQLYKqjeS-Gtn6v1" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=10WvZf1XfdFhN0-YNqQLYKqjeS-Gtn6v1" width="50%"/>

- Enter payment info into the form and submit (Pay button) and Boom, your account is upgraded.

    <img src="https://drive.google.com/uc?export=view&id=12ueOK5QZK55uAlUVAupm2C9_nOCN0prA" alt="Stripo Pricing Plans" data-canonical-src="https://drive.google.com/uc?export=view&id=12ueOK5QZK55uAlUVAupm2C9_nOCN0prA" width="50%"/>

## Stripo features

Before doing some email creation practice with Stripo, we will discover some Features that Stripo supports to know what they can do, and then we can easily apply them to our process.

### Modules Library

With our email template creator, you build email elements once — reuse across multiple campaigns. Speed up email production by 16 times!
[Read more](https://stripo.email/blog/stripo-content-modules-what-are-they-and-why-do-you-need-them/)

### HTML & CSS Code Editor

In addition to the Drag-n-Drop email builder, Stripo offer the HTML & CSS code editor. Use it to code emails from scratch, or edit and add custom elements to the emails that you create with our Drag-n-Drop builder. Use D-n-D and HTML & CSS code editors simultaneously with no switching. See the results of your work instantly.
[Read more](https://stripo.email/blog/how-stripo-helps-email-marketers-and-designers/)

This feature is the main thing we always use when we work with Stripo, so try to master it. When you can use this editor easily, email is not a nightmare, it is a pink dream. We will go details how to use it in [this section]()

### Email Templates

Stripo's newsletter builder offers over 1100 fully responsive HTML email templates, thoroughly crafted by designers. Customize and use any for your future campaigns.
[Read more](https://stripo.email/templates/)

If you don't have any idea about how email look and feel, this is a library for you to get inspired. Or you may learn how they create layout and structure code, how they resolve a problem.

### Export Options

Push emails to an ESP of your choice with 1 click. Download emails as PDF, and HTML files, or as an Image. Export emails to Outlook and Gmail for sending out to your contact base.
[Read more](https://stripo.email/integrations/)

This is one of the most essential features that make me choose Stripo as our best suitable email tool. It can export to HTML files and we will use it to implement Transactional email, Built-in email, SES email,...

### AMP for Email

Real-time, and dynamic content to make emails more useful for clients, new level of email gamification to improve user engagement. All this with little to no coding skills in our email body generator.
[Read more](https://stripo.email/amp-examples/)

This is new format of email, it can create a dynamic email, you can do a lot of magic things in this format like Carousel, Accordion, Animation button,... You email will become a real web site. However, It only support on Gmail web, Gmail iOS, Gmail android, Yahoo mail web. So consider when using it.

### Customer Support

Got a problem? Professionals on Stripo's customer support team will help you out. Connect them via chat, email, and over the phone. Mon-Fri, 8AM-12AM, UTC+2.
[Read more](https://support.stripo.email/en)

If we have any problems or question, ask them. They are the team who understand most about Stripo

### Brand Guidelines

Store email design styles and brand assets in one place to stay brand consistent across all emails and to onboard new designers faster.
[Read more](https://stripo.email/guideline/)

### Stripo Translation

Translate emails from one language to another in the editor. Help proofreaders see translations in the context, right in email templates for a better user experience.
[Read more](https://stripo.email/blog/stripo-translate-or-how-to-produce-emails-in-different-languages-fast/)

### Custom Fonts

To stay on-brand across emails, use custom fonts. Uploading them will take you under 5 minutes.
[Read more](https://stripo.email/blog/add-use-custom-fonts-stripo/)

### Email Annotations Builder

With Stripo's Gmail annotations generator, you provide recipients with the sale start/end dates, product image, and promo code right in the Inbox before they open emails!
[Read more](https://stripo.email/gmail-promo/)

### Data Service/Source

Connect AMP emails to Stripo's Data Service and Data Source for collecting users’ feedback from email surveys, and using real-time/dynamic content in emails.
[Read more](https://stripo.email/blog/working-with-data-source-in-stripo/)

### User Roles and Permissions

Let your teammates work on emails with you. Assign different roles with respective levels of access to each of them.
[Read more](https://support.stripo.email/en/articles/3173877-understanding-of-roles-and-permissions)


--------------------------
<br/>

# Working with Stripo in Journey Horizon

## Dashboard

- You should create email in your project folder.

## Dig deeper with Stripo's HTML & CSS Code Editor

Here is video playlist of Stripo:

[Playlist: Introduction to Stripo: What it is, and how to use it](https://www.youtube.com/watch?v=L1ILbMjdFFU&list=PLgXmUKpFR5RgMlIiEPA_UgU_ho-rem35R)

[Playlist: Сreate Emails Fast](https://www.youtube.com/watch?v=AZ7W6tgBVIg&list=PLgXmUKpFR5Rj8UZNdeWc-uglItUG8CAP1)

[Playlist: How-to Videos](https://www.youtube.com/watch?v=8gqqANVWdjU&list=PLgXmUKpFR5RifIVgiXCJLngMK3jQT2oQD)

[Playlist: Export Options, or How to Push Emails to your ESP](https://www.youtube.com/watch?v=pkk_Gja902k&list=PLgXmUKpFR5RgrnNWLythPlTSelxV2HosE)

[Playlist: EMAIL TIPS & TRICKS](https://www.youtube.com/watch?v=SEY2zX1QVxA&list=PLgXmUKpFR5RhnFEhmuNqR5UqceHlBC2tZ)

[Playlist: AMP4EMAIL](https://www.youtube.com/watch?v=mdFQewNmxe8&list=PLgXmUKpFR5RiBLExvuYXWoAWy5dUDIfM8)

**You can watch videos or read all the long text below**

We are going to deepen in details to show how to create your first email with the Stripo email template builder.

There are three ways to build your first email template with Stripo:

    1.  Editing one of the 5500 prepared email templates.
        
    2.  Coding your own one.
        
    3.  Starting one from scratch.
    

To use any of the aforementioned options, in the “Emails” tab, you need to hit the “New template” button.

![Stripo How to Build an Email Three Options](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-an-Email-Three-Options.png "Stripo How to Build an Email Three Options")

And choose the way that you find the most convenient for yourself :

### 1\. Editing one of the 550 prepared email templates

This is the easiest and probably the most convenient way of building emails. You only need to choose the template you like, customize it down so that it fits your brand design best, insert your URLs and replace our images with yours. That’s it. Your email is ready!

![Stripo How to Build Email Way 1 Editing Prepared Emails](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Way-1-Editing-Prepared-Emails.png "Stripo How to Build Email Way 1 Editing Prepared Emails")

Works best for email marketers that need to create a number of emails per day.

### 2\. Coding your own one

Stripo offers an open HTML code editor where professional coders can build an email that is totally unique. This option is also useful when you need to import a custom email template into Stripo and adapt it to the editor/make it editable.

![Stripo How to Build Emails Way 2 Coding](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Emails-Way-1-Coding.png "Stripo How to Build Emails Way 2 Coding")

Suits the worldly-wise designers best.

### 3\. Starting one from scratch/Empty email

The option means that you will need to drag and drop structures into your template, then fill them in with content blocks or modules.

![Stripo How to Build Email Way 3 Starting from Scratch](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Way-3-Starting-from-Scratch.png "Stripo How to Build Email Way 3 Starting from Scratch")

I decided to create a new email by using this way.

### 4\. General settings

First of all, this way you stick to the unified design style across all elements in email. You set font colors for the copy in email, you set forms and fonts for buttons, the colors for the links, paddings in containers, line spacing, email background color and content background color, email width.

#### Important to note:![Stripo How to Build Email with Stripo Email Background](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-with-Stripo-Email-Background.png "Stripo How to Build Email with Stripo Email Background")

Email content background stands for the background applied to the entire email area. When opened on desktop devices, it covers all email message areas, while on mobile devices it gets hidden (the red background in the example above).

The content background stands for the color within the email applied to all containers with products’ cards, contact information, etc. (the photo of a girl, shown in the example above).

Email width is 600px, by default. This is, currently, the most common size.

By making these settings, you significantly reduce the time that you’d spend on polishing email design. As you set once, and these parameters are applied to all content elements in emails.

If any style, that you apply to a separate row/container/block, differs from the styles set in the General settings sections, it will prevail over the general style.

#### How to make general settings with Stripo:

*   in the settings panel, click the “Appearance” tab;
    

![Stripo How to Build Email Setting General Settings](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Setting-General-Settings.png "Stripo How to Build Email Setting General Settings")

*   choose the “General settings” tab;
    
*   set the parameters that you like or the ones that comply with your brand book.
    

We strongly recommend choosing fonts, colors, buttons, paddings prior to starting working on the email. Yet, email and content background colors should be set after the email is ready. This way, you see if they really fit in well.

### 5\. Setting headings

The general styles cover only the “normal” text in your emails. Hence, you should separately set the font, its size, and style for headings that would be used across emails.

![Stripo How to Build Email Headings in Emails](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Headings-in-Emails.png "Stripo How to Build Email Headings in Emails")

In this example, Litmus applied H1 to announce its webinar.

If you like, use bold or italic type, or even set a different font to make headings stand out.

### How to set styles for Headings in emails with Stripo:

*   in the settings panel, click the “Appearance tab”;
    

![Stripo AtoZ Manual Setting HEadings](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-AtoZ-Manual-Setting-HEadings.png "Stripo AtoZ Manual Setting HEadings")

*   then select the “headings” tab;
    
*   set the font size and color for each heading (H1, H2, H3).
    

### 6\. Building header

[Email header](https://stripo.email/blog/email-header-best-practices/) — is the first element of emails that recipients see. It normally contains the brand logo and menu.

So, first of all, we need to decide what our header will look like. There are many types of a header design.  
Yet, the most popular one with eCommerce is when the logo on top, and menu below.

![Stripo How to Build Email Building Regular Menu](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Building-Regular-Menu.png "Stripo How to Build Email Building Regular Menu")

As long as this is the type of header that Stripo uses in its newsletters, we’re going to recreate one here.

The header type requires two separate rows: one for the logo, and the other one for the menu.

#### How to add logo to your emails with Stripo:

*   pull a 1-column structure in your “empty template”;
    
*   click the “image” button, or drag and drop the “image” block;
    

![Building Emails A to Z_Uploading Logo Image](https://stripo-cdn.stripo.email/photos/shares/Blog/Building-Emails-A-to-Z_Uploading-Logo-Image.png "Building Emails A to Z_Uploading Logo Image")

*   on the left, in the settings panel, the system will ask you to drop your image of JPG, PNG, or GIF format. You can also paste an external URL link to your logo;
    
*   insert a hyperlink that takes readers to your website;
    
*   add alt text to the logo;
    
*   set the logo size — my logo’s width is 144 px;
    

![Stripo How to Build Email Editing Logo](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Editing-Logo.png "Stripo How to Build Email Editing Logo")

*   center alignment is set by default. If you need to change it, click “left” or “right” alignment.  
    

#### Important to note:

if you want to set a background for the row where your logo and menu are located, then make sure to use a URL to the logo image in the PNG format with a transparent background.

Why apply links to the logo? — Quite often, recipients click on it to get to your website faster.

Why add alt text to the logo? — First of all, to pass the anti-spam filters, second of all; second of all, to provide users with information on what the image is about, in case they do not see images in emails; third of all, to comply with the email accessibility best practices.

#### How to add a menu to your emails with Stripo:

*   click the “Content” tab in the settings panel;
    
*   rag the 1-column structure and put it below the logo;
    
*   now open the “Blocks” tab;
    
*   pull a menu block and drag it into your template;
    

![A to Z_Menu Block](https://stripo-cdn.stripo.email/photos/shares/Blog/A-to-Z_Menu-Block.png "A to Z_Menu Block")

*   add extra menu items if you like. By default, Stripo offers three of them;
    

![Stripo How to Build Emails with Stripo Adding Extra Menu Items](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Emails-with-Stripo-Adding-Extra-Menu-Items.png "Stripo How to Build Emails with Stripo Adding Extra Menu Items")

*   now in the settings panel, you need to choose whether to use icons, links, or both. “Icons” stand for the images in the menu; while “links” stand for the names of the menu tabs;
    
*   once you select the links type, which I did, you will see that the color and font of your links, that you previously set in the “General settings” section, are already applied to the menu links. I made them bold by clicking the “B” icon in the settings panel;
    

![Stripo How to Build Email with Stripo Working with Links in the Menu](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-with-Stripo-Working-with-Links-in-the-Menu.png "Stripo How to Build Email with Stripo Working with Links in the Menu")

*   now you need to name each menu item;
    
*   insert necessary URL links;
    

![Stripo How to Build Email with Stripo Giving Names to the Menu Items](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-with-Stripo-Giving-Names-to-the-Menu-Items.png "Stripo How to Build Email with Stripo Giving Names to the Menu Items")

*   do the same to all menu items;
    
*   if you want to hide some elements for mobiles, just click the “Hide on mobile” icon;
    

![Stripo How to Build Email Menu Mob View](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Menu-Mob-View.png "Stripo How to Build Email Menu Mob View")

*   finished with naming menu items? Then take a look at what you’ve received. In my opinion, the menu looked small, so I decided to set a bigger font for it — I set “18”.
    

#### Important to note:

there are some other types of the menu, including interactive ones, that you might like to use.

Your browser does not support HTML5 video tag.

> Please, [find more details here](https://stripo.email/blog/add-menu-email-stripo/).

### 7\. Working with text

Normally, there goes a banner after the navigation menu bar.

But at Stripo, we prefer specifying the goal of our email here and greeting recipients first, as the Korean Cosmetics does.

![Stripo How to Build Email Working with the Text](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Working-with-the-Text.png "Stripo How to Build Email Working with the Text")

#### Important to mention:

please, be advised that Stripo allows using custom fonts, which are not on our list of fonts.

> Please refer to [this manual](https://stripo.email/blog/add-use-custom-fonts-stripo/) for more details on how to add custom fonts with Stripo.

The custom font that you’ve installed in your account with Stripo, can be applied to any copy in the email, except for the text placed over banners.

#### How to add copy to your emails with Stripo:

*   drop the 1-column structure into your HTML email template;
    
*   pull a “Text” block into it, or click the “text” button right in this structure;
    

![Stripo How to Build an HTML Email Template with Stripo Adding Text](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-an-HTML-Email-Template-with-Stripo-Adding-Text.png "Stripo How to Build an HTML Email Template with Stripo Adding Text")

*   enter your greetings;
    
*   double click the very text;
    
*   set headings where necessary. In our example, for the greetings, I chose headings 2 — and as long as we’ve set parameters for Headings in the “General Settings” tab at the beginning, Stripo automatically used them (Arial, 24px) for our email;
    

Your browser does not support HTML5 video tag.

*   enter your text in the next line;
    
*   highlight it;
    
*   set alignments;
    

![Stripo How to Build an Email Template with Stripo Setting Alignment](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-an-Email-Template-with-Stripo-Setting-Alignment.png "Stripo How to Build an Email Template with Stripo Setting Alignment")

*   add links where necessary.
    

#### How to add links to text with Stripo:

If you need to add links to text, but not only to CTA buttons, you need to:

*   highlight a necessary word/words;
    
*   in the setting panel on top, click the “Link” icon;
    
*   in the settings panel on the left/right, the system will ask you to paste your URL and once again will remind you what word the link is connected with.
    

![Stripo How to Build an Email Template Manual AtoZ Adding Links to Text](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-an-Email-Template-Manual-AtoZ-Adding-Links-to-Text.png "Stripo How to Build an Email Template Manual AtoZ Adding Links to Text")

You may or may not underline links in emails — do as you like.

#### Important to note:

We recommend that you enable word break in your emails if you do not wrap links in buttons or if some words are way too long. For instance, when your email is written in German, you’d better enable the word break option. This will help you avoid horizontal scrolling on mobile devices. Just toggle this button for activation.

![Stripo How to Build Email Template with Stripo Toggling Line Breaks](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Template-with-Stripo-Toggling-Line-Breaks.png "Stripo How to Build Email Template with Stripo Toggling Line Breaks")

This is a screenshot of a reset password link that is not hidden in a button. If the word break were not activated here, then horizontal scrolling would appear.

![Stripo How to Build Email with Stripo Breakin Lines for Links](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-with-Stripo-Breakin-Lines-for-Links.png "Stripo How to Build Email with Stripo Breakin Lines for Links")

Today, there’s nothing worse than a non-responsive email.

### 8\. Personalizing copy

Emails with personalized copy — addressing by names —  bring in 14% more profit than those without personalization.

Add merge-tags to greetings, like in the example below, to email footer to specify recipient’s email address, always address by names in triggered emails.

![Stripo How to Build Email Template with Stripo Addressing by Names](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Template-with-Stripo-Addressing-by-Names.png "Stripo How to Build Email Template with Stripo Addressing by Names")

Stripo email template builder allows adding the merge-tags to any copy in the email template.

#### How to add merge-tags in emails with Stripo:

*   in the email template you are working with, place the mouse cursor in the necessary place;
    
*   in the settings panel above the template you are working with, you’ll find the “Merge tags” button;
    
*   in the dropdown menu, select the ESP you are working with;
    

![Stripo How to Build Email Template with Stripo Adding Merge-Tags](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Template-with-Stripo-Adding-Merge-Tags.png "Stripo How to Build Email Template with Stripo Adding Merge-Tags")

*   choose the parameter you want to use.
    

If done right, it will look like this:

![Stripo How to Build Email Template with Stripo Inserted Merge-Tags](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Template-with-Stripo-Inserted-Merge-Tags.png "Stripo How to Build Email Template with Stripo Inserted Merge-Tags")

Your ESP will replace this parameter with the first name of each recipient. If the first name (or any other parameter) is not specified, then your ESP will leave this field empty.

#### Important to note:

If you need to add merge-tags to email subject line, make necessary settings in your ESP, or just copy your 

### 9\. Adding images

Imagery is the basis of all emails. No matter how compelling your copy is, there definitely should be images as they appeal to emotions by showing our products in their best.

#### How to add an image in emails with Stripo:

*   pull a new structure with a necessary number of columns into your HTML email template;
    
*   in the settings panel, find the basic “Banner”/“Image” block and drop it into the template;
    
*   once you drop the content block in, click on it right in the email;
    
*   in the settings panel, you will be asked to insert an image.
    

#### Note:

If you need to build a banner, please, use the “Banner” block. For other purposes, please use the “image”

#### There are four ways of doing it:

##### 1\. Dropping/uploading image

Here, you can really just drag and drop the image you are about to use for your campaign or upload it from your computer by clicking the “arrow” and selecting the very image from your computer.

![Stripo How to Build THML Email Template with Stripo Uploading Banner Image](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-THML-Email-Template-with-Stripo-Uploading-Banner-Image.png "Stripo How to Build THML Email Template with Stripo Uploading Banner Image")

##### 2\. Pasting external URL

If you do not have the banner image saved to your computer, you are welcome to insert links to this image on the web.

In the “External link” field, paste the link to your image.

![Stripo How to Build HTML Email Template with Stripo Pasting External Links to Images](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-HTML-Email-Template-with-Stripo-Pasting-External-Links-to-Images.png "Stripo How to Build HTML Email Template with Stripo Pasting External Links to Images")

If you are going to use this image just once, in the dropdown menu, choose the “Leave as external link” option (as shown in the example above) and click the “Tick”.  
  
If you are going to use this image for other email campaigns, then click the “Project” tab above, then insert the link and choose the “Download to the gallery” option, and click the “Tick”.

![Stripo How to Build Email Working with Image](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-Email-Working-with-Image.png "Stripo How to Build Email Working with Image")

##### 3\. Using images from the personal gallery

When you upload images or download them to the gallery as shown in the example above, your images are stored in your personal gallery. You just need to switch to the Email tab.

![Stripo How to Build HTML Email Template _Working with Personal Image Gallery](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-How-to-Build-HTML-Email-Template-_Working-with-Personal-Image-Gallery.png "Stripo How to Build HTML Email Template _Working with Personal Image Gallery")

Images here are sorted by the dates, the most recent → the oldest ones.

If the list of images is too long, you may search by its name.

To use one in your current HTML email template, you need to click on the selected image and it will automatically appear in your email.

##### 4\. Using our bank of images

First of all, I want to say that all the images, available with Stripo, are totally free.

Second of all, we offer over 100,000 images.  
Click the “Bank” tab, then enter the name or the category of images you are searching for.

Once you’ve selected an image and clicked on it, it will immediately appear in the template you are working with. This way, you may check if it fits in your email.

If you like what you see, then click the “use” button.

![How to Build HTML Email Template with Stripo_Addimg Images from the Bank](https://stripo-cdn.stripo.email/photos/shares/Blog/How-to-Build-HTML-Email-Template-with-Stripo_Addimg-Images-from-the-Bank.png "How to Build HTML Email Template with Stripo_Addimg Images from the Bank")

### 10\. Editing images

In the previous paragraph, we showed how to upload images and store them.

But how can you edit them with Stripo?

In this section, we’re showing how to edit images that you use for product cards, for signatures, for logo, for presenting panelists and upcoming events, etc.

I.e. all images that you use for any purpose in emails, including custom thumbnail image for video.

How to work with images to build a banner, we’ll show in the next section.

#### How to edit images with Stripo:

*   once you’ve uploaded the image, in the settings panel, to the right from the image snippet, click the “edit” button;
    

**![Stripo AtoZ Manual Editing Images](https://stripo-cdn.stripo.email/photos/shares/Blog/Stripo-AtoZ-Manual-Editing-Images.png "Stripo AtoZ Manual Editing Images")**

*   in a new pop-up window, your image will be opened with the Pixie editor;
    
*   here, you can apply filters, resize and crop images, draw over them, put any text over them, add stickers, frames, apply backgrounds;
    
*   when you’ve done with editing, click “save” in the Pixie editor — only then the changes you’ve made to the image will be applied.
    

### 11\. Building banner

It is said that [banner](https://stripo.email/blog/create-banner-stripo-email-template-builder-within-minutes/) is the face of your newsletters. Hence, you need to work thoroughly on it.

Normally, as a banner we understand an image that evokes emotions in your target audience, along with complementary copy over this particular image.

#### Important to mention:

Stripo offers a banner generator, that enables its users to build sophisticated banners right in the editor without any third-party tools.

#### How to build email banner with Stripo:

*   drag a 1-column structure into your HTML email template;
    
*   pull the “Banner” block into this structure;
    

*   click this block in the template to activate the settings panel;
    
*   upload image that you’re about to use;
    
*   in the settings panel, the system will suggest that you crop the image if needed;
    
*   set image orientation. It can be vertical, square and horizontal. The latter is the most popular one;
    

*   apply filters. I prefer the greyscale one;
    
*   paste the link that will take recipients to the place related to the value offer described on the banner;
    
*   enter alt text — this text will be shown to recipients if images for some reason cannot be displayed;
    

*   if you need to place any copy over the banner image, you need to click the “T” button on the settings panel above. Once it gets light, you need to left-click this image again;
    
*   the very moment, you’ll see the “Caption” inscription on the banner;
    
*   erase this inscription and enter your text here;
    
*   set font size, font color, and the font type;
    

*   among the banner fonts, choose the one that fits your email best;
    
*   toggle the “additional picture” button in the settings panel. It can be anything you like: sticker, frame, logo, background to make your copy more noticeable, etc. Yes, you can place text over it :)
    

#### Please, be advised:

Once your banner image is added, you can make all the editing steps in any order you like. For instance, insert an additional image, add text and only then apply fonts.

To build a banner like this one, you need to:

*   upload image;
    
*   set image orientation;
    
*   insert additional image over it;
    
*   place copy over both images.
    

#### Important to note:

The font size, style, and color, that you’ve set in the General Settings tab, are not applied to banners.

Currently, Stripo offers over 40 banner fonts. They are decorative. Yet, you should not be afraid to use any of them, because our banner generator works like Photoshop — images, text, frames are edited as separate layers. Yet, they all combine into one single image during the export. This means that any text placed over banners are considered image elements by email clients. Consequently, they do not get replaced with the default ones.

> If you are interested in more ideas for banners and wanna know how to build them with Stripo easily, please, read [this article on a dedicated topic](https://stripo.email/blog/create-banner-stripo-email-template-builder-within-minutes/).

### 12\. Image rollover effect

[Image rollover effect](https://stripo.email/blog/12-bullet-proof-ideas-include-image-rollover-effect-emails/) helps you entertain and engage customers. Moreover, it saves you precious space in emails, as you can hide product details behind its photo. You can also play games with recipients by making them “search” for the coupon, etc. There are many reasons why you need to add image rollover effect to your emails.

Your browser does not support HTML5 video tag.

But how can you actually build one? This technique was developed by our coders and has been adjusted to our system and what’s more important — to major email clients.

It works [even in Gmail](https://stripo.email/blog/12-bullet-proof-ideas-include-image-rollover-effect-emails/).

#### Important to note:

Image rollover effect works on desktop devices. Other users will see the primary image only.

It can be applied to any image you add in email except for the banner one.

#### How to build an image rollover effect with Stripo:

*   upload image;
    
*   in the settings panel, toggle the “Rollover effect” button;
    
*   upload the second image — edit it if needed;
    
*   insert URL link — it will be tied to both images;
    
*   enter the “Alternate text”.
    

Your browser does not support HTML5 video tag.

Please, find best practices and inspiring ideas [here](https://stripo.email/blog/12-bullet-proof-ideas-include-image-rollover-effect-emails/).

### 13\. Adding video in emails

According to numerous studies, potential customers are [65% more likely to buy](https://stripo.email/blog/email-marketing-metrics-kpis-increase-using-email-editor/) from us after watching a video. Moreover, videos are one of the hottest trends for 2019.

Stripo provides its users with two ways of adding videos in emails:

1.  Inserting URL link to your video.
    
2.  Embedding video.
    

#### Way 1. Inserting URL link to your video

This is a totally safe way of delivering videos because it works perfectly well in all email clients and on all devices.

How to insert URL link to your video:

*   pull the 1-column structure in your HTML email template;
    
*   pull in a basic “Video” block;
    
*   left-click the container in the email;
    
*   in the settings panel, you will only need to insert the link to your video on Youtube or Vimeo;
    

*   our system will automatically fill out the “Alternate text” field;
    
*   select the color of the “play button” — it can be white, traditional red and black.
    

Our system automatically generates the thumbnail/preview image for your videos. But you may also want to set a custom one.

##### How to set a custom thumbnail to video in emails:

*   toggle the “custom thumbnail” button in the settings panel;
    

*   upload an image;
    
*   edit it if necessary.
    

You may even insert an animated GIF as the thumbnail image if you like. It will certainly draw more attention to the video.  

Your browser does not support HTML5 video tag.

##### Important to note:

The play button will be displayed over the custom image, as well.

#### Way 2. Embedding video

Embedded video is the kind of videos that are played right in emails. Recipients are not required to go to another website to watch the video.

Yes, it cannot be played by all email clients. In fact, only Apple Mail, native iOS mail, Thunderbird and Outlook for Mac do support this kind of content.

Stripo provides its users with a universal code — by using which you provide all of your users with the video you want to share.

##### We recommend sticking to the following order:

1.  Embed this code in an email template.
    
2.  Customize the given code by inserting your URL links.
    

##### How to embed this code in emails with Stripo:

*   pull the 1-column structure in your HTML email template;
    
*   drop a basic HTML block;
    

*   in the email template, left-click the “Insert your HTML in the code editor” to open the Code editor;
    
*   in this editor, instead of the “Insert your HTML code editor" paste the embed code;
    

Your browser does not support HTML5 video tag.

*   customize the embed code.

#### The very code to embed:

Copy

    <video class="adapt-img" controls="controls" poster="https://tlr.stripocdn.email/content/guids/CABINET_0bd21bea47f1cfb916fb84d59a107495/images/92621531318217276.jpg" width="100%" height="313"> 
                                    <source src="http://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4"> 
                                    <source src="http://www.w3schools.com/html/mov_bbb.webm" type="video/webm"> 
                            <!-- fallback --> 
                            <a href="https://www.youtube.com/watch?v=ryqOEPk51Lg/" class="esd-frame-element esd-hover-element esdev-disable-select"><img class="adapt-img" src="https://tlr.stripocdn.email/content/guids/CABINET_0bd21bea47f1cfb916fb84d59a107495/images/48461531318273724.jpg" alt="" width="100%" height="313"></a> 
                           </video>
    

The part of the code that goes above the “_fallback_” is for those recipients whose devices and email clients support this interactivity. While the part below is for those whose email clients do not support interactivity — they are redirected to Youtube, Vimeo or any other video hosting site.

By using this code, you make sure that all of your users will see the video you want to share.

#### Customize the embed code:

*   upload the image, you are going to use as the thumbnail one, to any site (I use Pinterest for these purposes) — it will serve as the preview image for those clients who use Apple devices.  
    Certainly, the MP4 video will generate its own thumbnail image, but this image will not render on iPhone X and devices with Retina displays. The play button will automatically appear on it. Paste this link after the _"Poster"_ attribute;
    
*   convert your video to MP4 format by using any video hosting site (I use [Streamable](https://streamable.com/). It’s free). In the code, replace the link that goes after the _"source src"_ attribute with your URL;
    
*   convert your MP4 video to the WebM format — and insert the link in the respective line of the code. This video will be played on those devices which support videos of this format;
    
*   and upload the second image you are going to use as the thumbnail one. Draw the _“play”_ button over it. It can be actually a screenshot of your video on Youtube — will be displayed in all email clients that do not support interactivity in emails yet;
    
*   then upload your video to Youtube (Vimeo, your website, etc.) — paste this URL in the "_href"_ attribute after the quotation marks instead of the existing link. Once the recipient hit the _“play”_ button, he or she will be directed to the respective website.
    

### 14.Adding CTA buttons

Button, in fact, is a URL link beautifully designed. It should be visible, and its copy needs to be clear and concise

Your browser does not support HTML5 video tag.

#### How to build a CTA button with Stripo.email:

*   pull the basic button block into your template and drop it next to the product it is related to;
    

*   tap the button block in your HTML email template to activate the settings panel;
    
*   insert a necessary URL link;
    
*   enter your button label;
    

*   set text style, such as font, its type, and font size;
    
*   set button color, font color;
    
*   set a border radius if you like oval buttons;
    
*   choose alignment;
    
*   set the button border if you like;
    

*   set internal paddings. They are responsible for the whitespace inside your button. Due to the [button layout method chosen by Stripo](https://stripo.email/blog/button-choose-layout-method/), it does not matter where exactly in the button your customers click. Whitespace is also clickable, yet it makes the buttons more appealing and clear;
    

*   set external paddings — they are responsible for the whitespace outside the button, but within the container, it is located in.

#### Important to note:

If you'd like to apply a hover effect to your buttons, you need to:

*   go to the Appearance tab;
*   enter the "Button" tab;
*   toggle the "Highlight hovered buttons" button;
*   set parameters for the buttons and their fonts when highlighted.

These settings will be applied to all the buttons in your template. If you want to apply the hover effect just to some of them, set the same color both for "Button color" and "Highlighted button color" to the buttons you do not want to apply the hover effect to. It will work only if you set one text colo for both "Text color" and "Highlighted text color".

Hover effect works in most email clients on desktop devices. It does not distort your email appearance on mobile devices and in email clients that do not support hoverable buttons.

### 15\. Building products content modules

Well, this module is a complex one, as it contains a number of blocks and elements.

Normally, such modules consist of the product snippet, brief description, price and CTA button.

Some brands, like M&M’s, add some introduction prior to showcasing products, while others add products’ promo right under the banner or the video — it’s totally at your discretion.

So, how to build a product content module with Stripo:

*   pull a 2-column structure into your template;
    
*   in any column, click the “image” icon in the structure to add product snippet;
    

*   upload the necessary image;
*   edit this snippet if necessary (we’ve described above how to edit images with Stripo) ;
    
*   drag a text block into the second column;
    
*   enter your text and set the necessary design style if it differs from the text style you set in the “General Settings” tab;
    
*   drag the “button” block and drop it under your text;
    
*   set its style — you are welcome to apply a hover effect to this button. Please, find the manual in the “Adding CTA buttons” section.
    

##### If you want to build one or two more modules similar to this one, you need to:

*   drop the 2-column structure in your template;
*   in the module we’ve just built, copy container with details;
    

*   and simply move it to a new structure;
    

*   edit information in it;
*   add new images;
    
*   done.
    

There is another way to build product content modules with Stripo — [smart elements](https://stripo.email/blog/smart-elements-reducing-time-creating-similar-letters-automating/). You configure them just once, and next time, when building a new template, you just insert proper links and Stripo automatically retrieves and inserts correct data into the respective fields.

### 16\. Building countdown timers for emails

Countdown timers in emails build a sense of urgency, notify recipients about the duration of the sale, or let them know how soon a certain event will start.

Countdown timers in emails [increase revenue by 9%](https://www.neurosciencemarketing.com/blog/articles/urgency-timer.htm).

You can build, design and add a timer to your HTML email template right in the editor.

#### How to build and add countdown timer in emails with Stripo:

![](https://i.ytimg.com/vi/qcqDNXR6k58/maxresdefault.jpg)

*   pull the 1-column structure into your template;
    
*   drop the Basic Timer block in it;
    

*   left-click this container in email template to activate the settings panel to work with the timer;
*   set the end date and exact time;
    

*   set the time zone;

*   set timer background color that fits your email design best;
*   make changes to the numbers’ size and color if necessary. Initially, Stripo applies the parameters that you specified when making general settings;
    
*   toggle the “Display days” button if you want recipients to see how many days are left. Otherwise, they will see just hours and minutes. “5 days 20 hours” are easier to percept than “140 hours”;
    

*   change date style if necessary. By default, we use “:” (colon) to separate days from hours, minutes, seconds. You can also set “-” and “/”;

*   toggle the “number labels” button to display names “days”, “hours”, “minutes” and “seconds” under respective numbers;

*   set color, font type and size to the labels;
*   toggle the “Expired Timer Image” button;
    
*   upload the image (as explained in the respective paragraph) that will be shown to customers once the timer expired. This is optional, yet we strongly recommend doing it — this will you will inform recipients the coupon is expired and they cannot use it any longer;
    

*   insert URL link that will take recipients either to your website or to a particular page on your site when you describe the value offer in the details. This link will be applied to the “Expired timer image” as well;
    
*   specify the alt text for accessibility.
    

> Please, find more ideas and inspirational examples in our blog post [How to add a countdown timer in your email](https://stripo.email/blog/add-countdown-timer-email/).

### 17\. Adding spacer

Spacer, aka divider, does not drive conversions, or anything else. This is just a decorative element, which makes emails look structured and leads to a better and easier perception of email content.

#### How to set spacer in emails with Stripo:

*   drag the 1-column structure into your HTML email template;
    
*   drop the “Spacer” block;
    

*   double-click to activate the settings panel;
    
*   set its color;
    
*   to set the “thickness” of your spacer — you need to set the “number” in the “Line” section — increase/decrease numbers;
    
*   you also need to choose the style of your line. It can be solid, dashed and dotted;
    

*   set width — the width here is measured in %, not in pixels!
    

*   specify spacer alignment. By default, center-alignment is set. If you like, please change it in the “alignment” section;
    
*   toggle the “responsive spacer” button for a spacer to render properly on mobile devices;
    
*   if necessary, set paddings.
    

### 18\. Inserting social networking

Social networking icons, aka social media icons, can be located anywhere: in the menu, in the footer or somewhere in the middle of email — wherever you find it suitable.

#### How to add social media icons with Stripo:

*   pull the “Social” basic block in your template;
    

*   double click it in your template to activate the settings panel;
    
*   by default, you will see 4 icons. If they are not enough, click the “plus” button to add extra icons in your email;
    

*   in the settings panel, next to the social media icon, toggle the “more” button to start working with this particular social network;
    
*   insert respective URL links;
    
*   enter Title and Alt text;
    

*   set style for these icons;
    

*   set their size;
    
*   and finally set the paddings and indents between the icons.
    

#### Important to note:

[In this post](https://stripo.email/blog/add-social-media-icons-email-signature/), we show how to synchronize information you’ve specified in your personal account with editor — once you properly set the contact information in your account, you will only need to pull the “Social” basic black into the template, Then our system will retrieve information and will insert proper links into respective fields.

Your browser does not support HTML5 video tag.

### 19\. Building email footer

[Email footer](https://stripo.email/blog/email-footer-design-best-practices/) normally contains contact information, like your website address, the reason why you’ve reached out to recipients, links to your social media accounts hidden behind the [social media icons](https://stripo.email/blog/add-social-media-icons-email-signature/), the [unsubscribe link](https://stripo.email/blog/7-tips-effective-email-unsubscribe-pages/) and name of the person who is responsible for the newsletter email. The latter is optional, yet all the elements that precede it, are mandatory.

#### How to build email footer with Stripo:

This is a compound element of emails. To build one, you need to:

*   drag a structure with a necessary quantity of columns;
    
*   enter copy into these columns/blocks;
    
*   edit copy;
    
*   insert the respective link to the unsubscribe option;
    
*   add social media icons.
    

> Get inspired by the ideas for an effective email in [this blog post](https://stripo.email/blog/10-best-email-signature-design-examples/).

### 20\. Background color and image

Backgrounds applied to individual containers/stripes (aka rows) help you drag recipients' attention to certain elements. Backgrounds applied to entire emails make your design look complete and unified.

In this example, we are going to apply a background color to a structure.

#### Setting background color to a structure

My brand name in the logo is written in white. As, by default, all emails have transparent backgrounds, the chances are my recipients will not be able to read what my logo says. Which is why I need to set a background color just to this structure.

#### How to set a background color for a structure:

*   click any element in this structure in the template;
    
*   on the left in the settings panel, click the “to container” button;
    
*   click the “to structure” button;
    
*   in the “background color of structure” field, enter or select the color you like.
    

Your browser does not support HTML5 video tag.

Note: you do it the same way to set background color for entire email.

#### How to set a background image for entire email:

The background image will be shown on desktop devices only. It won’t be displayed on mobiles.

*   in the General settings tab, toggle the “Background image” button;
    

*   add an image — in the “Adding Images” section, we described how to insert/add/upload images to templates with Stripo;
    
*   set its position;
    
*   click the “repeat” button if you want your image to be applied to entire email no matter how long it is.
    

#### Important to note:

Some email clients, like Outlook, may not show the background image. Hence, we recommend also setting the background color, that is similar to the background image, to entire email.

### 21\. Writing subject line

About one-third of [recipients judge by the subject line](https://stripo.email/blog/best-catchy-email-subject-lines/) whether to open emails or not.

You can set one in your ESP, or do it with Stripo.

#### How to write a subject line for your emails with Stripo:

*   above the template you are working with, click the “Settings” icon;
    
*   in the dropdown menu, enter your subject line and preheader text;
    

Your browser does not support HTML5 video tag.

*   [add emojis to Email subject](https://stripo.email/blog/use-emojis-emails/), if you like.
    

### 22\. Settings for email rendering on mobile devices

Yes, in the General Settings tab, you’ve already set your preferences. Yet, they are applicable to desktop only. You need to specify your preferences for mobiles, also. Why would you?

Because, for instance, your font size is 14 px, but it will seem small for mobiles, 16 px is more preferable here.

But, say, for info area/footer, 12px will be enough.

And it’s critical to allow “full-width” for buttons on mobiles.

Don’t let your customers miss the buttons :)

#### How to set preferences for mobile view:

*   In the settings panel, click the “Appearance” tab;
*   click the “mobile view” tab;
    

*   set your preferences for headings size, for text size in different content areas, and text size in buttons.

### 23\. Building AMP emails

In March 2019, Gmail rolled out its AMP for email. Now AMP emails are widely supported by many famous emails clients on desktops and even on mobiles by [Gmail app on Android, and iOS](https://stripo.email/blog/gmail-rolled-out-its-dev-preview-of-amp-emails-on-ios-and-android/) and by Mail.ru.

Your browser does not support HTML5 video tag.

Normally, building AMP emails is a time-consuming process. But Stripo offers its drag-n-drop AMP blocks: [AMP carousel](https://stripo.email/blog/how-to-build-amp-carousel-for-your-emails-with-stripo/) and [AMP accordion](https://stripo.email/blog/how-to-build-amp-accordion-for-your-emails-with-stripo-without-any-coding-skills/).

How to build an AMP email Stripo:

*   drag a necessary block into your template;
*   fill it in with your content.

#### Important:

AMP blocks are inactive in your template. To check how it works, you need to enter the Preview mode.

> If you want to add any other AMP element in your template, please refer to [this blog post](https://stripo.email/blog/how-to-build-amp-emails-with-stripo/) to find out how to do it with Stripo.

### 24\. Optional email elements

To make your emails more effective or to make their design more vivid, you are welcome to add some of the following elements:

#### Interactive elements in emails

Interactive elements are the trend for 2019. They double conversion not only for being entertaining, but also for being informative and functional.

In our “[6 Examples of Interactive Content in Emails](https://stripo.email/blog/interactive-email-newsletters/)” blog post, we showed in little detail how to build and add interactivity in your emails with Stripo.

Your browser does not support HTML5 video tag.

Due to advanced techniques, you can build with us:

*   [image rollover effect](https://stripo.email/blog/12-bullet-proof-ideas-include-image-rollover-effect-emails/);
*   CSS-animated buttons (please, see the manual on how to build one in the adding CTA buttons section);
*   [countdown timers](https://stripo.email/blog/add-countdown-timer-email/);
*   [embedded surveys](https://stripo.email/blog/8-ways-send-better-survey-invitation-emails/).

Due to our open HTML code editor and to the HTML basic block, you can embed any type of interactive element that you’ve built with a third-party tool.

#### Important to mention:

Please, be advised that some elements that you build with a third-party tool, can be non-responsive. To check this, you will need to test your emails.

#### Gmail Promotion Annotations Builder

This feature allows informing recipients about the size of the coupon, about the duration of the sale and even allows providing recipients with preview images without having them open our emails. Works on mobile devices.

You can easily build the annotation code by using our [Promotion Annotations Builder](https://stripo.email/gmail-promo/).

#### AMP-powered emails

[AMP-powered emails](https://stripo.email/blog/coming-soon-stripo-supports-amp-powered-emails/) will enable your recipients to add products to cart, to choose and buy tickets online, and many more things.

Google just released its AMP for emails, but you already can [build AMP-emails with Stripo](https://stripo.email/blog/how-to-build-amp-emails-with-stripo/).

### 25\. Previewing and testing your emails

Always preview and test your emails prior to sending out to recipients.  

#### How to preview your email with Stripo:

*   click the preview” button above the template to see mobile and desktop preview of your email.
    

If you've built an AMP email, you will be able to preview it also.

Just click the proper tab.

If your AMP HTML code contains an error, even like a missing error, our AMP code validator will warn you.

Just click this red button to find out what exact error your code has.

#### How to send test email with Stripo:

*   click the “test” button;
*   in the pop-up window, enter your and your colleagues’ email addresses — separate them with commas;
    
*   click “send”.
    

Your browser does not support HTML5 video tag.

> [In this blog post](https://stripo.email/blog/preview-and-send-test-email-in-stripo/), we showed in the details why and how to preview, test and get your email shareable link with Stripo to get colleagues and clients’ approval.

#### How to preview your emails across all popular environments

Now that you've previewed mobile and desktop versions of your emails, now that you've sent a test email to yourself to detect and fix all little issues that may occur, you should also see this email exactly how your subscribers will to ensure you deliver an email with a proper layout. 

Due to our integration with Email on Acid, you can now preview your emails across 90+ popular combinations of email clients and devices directly in Stripo.

To preview your email in all these environments, please:

*   click the "test" button above your HTML email template;
*   in the dropdown menu, click "Run email test";

*   in a new window, you will see the screenshots of your email in all these environments.

Please note that you can choose — select and deselect — email clients and devices for your tests.

Stripo also allows you to see all the previous tests.

> For more information on how to preview/test your emails with our embedded email testing tool, please refer to [our blog post](https://stripo.email/blog/stripo-integration-with-email-on-acid-how-to-use-our-email-testing-tool/).

### 26\. Exporting email to your ESP

Once your email is completely finished, I mean — tested and polished, you can easily send it to your ESP.

Stripo is integrated with about 50 ESPs, and email clients [Gmail](https://stripo.email/blog/export-email-templates-gmail/) and [Outlook](https://stripo.email/blog/animated-gifs-in-html-emails-in-ms-outlook/).

This means that you can transfer your emails to any of them with just 1 click.

If these options are not enough, download your email as HTML-file, and theт import into ESP you currently use.

And what is also important, Stripo enables you to download your email as [PDF-file](https://stripo.email/blog/how-to-save-an-email-as-a-pdf/).

#### How to export your email from Stripo:

*   click the “Export” button above the template;

*   in the dropdown menu, click the option that fits you;
    
*   done.
    

#### Important:

When exporting email to an ESP for the first time, you will be asked to enter login and password to your account with this ESP.

We do it to provide synchronization of account of the ESP you use with your account with Stripo. Yet, we do not store, nor can see your password with those systems.

Little tips to significantly reduce email production time when working with Stripo

----------------------------------------------------------------------------------

There are many of them, here I just want to mention a few of them:

#### Undo button

This simple button helps you cancel a previous/a few previous actions.

It prevents us from building email element once again from scratch.

#### Versioning

It allows seeing who and when made changes to our emails. And what is more important — allows restoring any version of your email.

It prevents us from building email from scratch (in case we do not like the last changes made to email).

Once you click this “magic” button, you see all the versions of the email, all dates and names of those who made the changes.

#### Copying and moving elements

This is a very convenient and fast way to use similar elements in emails.

For instance, you designed a spacer that perfectly fits your email and you want to use it across this email. There’s no need to build it again and again. You just click the copy icon in the “Command panel”

then you “move” the copied element. This is it.

Your browser does not support HTML5 video tag.

#### Storing modules

You can save to your personal library all kinds of content for further use — elements, blocks, containers, modules and stripes.

To save one, you just need to make this element active, then click the “save” button in the “Command Panel”. The system will ask you to give a name to this element in the settings panel for easy search.

By saving modules this way, you can build entire emails just by dragging modules into your template.

Your browser does not support HTML5 video tag.

We recommend storing and reusing the following elements: headers, footers, contact information, and containers with smart elements. The former will remain unchanged, the latter will require you to insert a new link.

> In [this blog post](https://stripo.email/blog/stripo-content-modules-what-are-they-and-why-do-you-need-them/), you will find more information on how to store and reuse content modules.

#### Storing and reusing existing templates

This is probably my favorite part. If you need to send similar emails daily, and you just update some information in them, like copy or banner — just copy your previous email. And edit elements that need to be edited. Voila!Your browser does not support HTML5 video tag.
