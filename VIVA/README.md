# Viva Connections Desktop

This powershell script (`Viva-connections-desktop.ps1`) will allow SharePoint admins to create a personal app in Microsoft Teams that brings their modern SharePoint communication sites directly inside Teams.

The app enables users to discover and search relevant content, news, and sites from across the organization right from the Microsoft Teams app bar. The app also allows you to incorporate your organization’s brand and identity directly in Teams. This personal app will be available on Microsoft Teams desktop only and is not supported for the Teams mobile apps.

Please ensure that this script is run by a user who has **SharePoint admin privileges in the tenant** and they have access to the site they want pin as the default landing experience in Teams. Please ensure that you are using the latest [SharePoint Online PowerShell Module](https://www.powershellgallery.com/packages/Microsoft.Online.SharePoint.PowerShell/) while running this script

When you run this script, you will have to provide the following inputs:

1. **URL of the modern SharePoint Communication site** (starting with “https://”) that you want to be the landing experience for the app. It is highly recommended that this site be the [Home site](https://docs.microsoft.com/en-us/sharepoint/home-site) of the tenant. 
1. **Name:** The name of your app, as it should appear in Teams app bar
1. **App short description (80 characters):** A short description for your app which will appear in Teams app catalog
1. **App long description (4000 characters):** A long description for your app which will appear in Teams app catalog
1. **Privacy policy:** The privacy policy for custom Teams apps in your company (needs to start with https://). If you do not have a separate privacy policy, press Enter and the script will use the default SharePoint privacy policy from Microsoft.
1. **Terms of use:** The terms of use for custom Teams apps in your company (needs to start with https://). If you do not have separate terms of use, press Enter and the script will use the default SharePoint terms of use from Microsoft.
1. **Organization name:** Your organization name. This will be visible on the app page in Teams app catalog in “Created By” section.
1. **Organization website:** Your organization’s public website (needs to start with https://). This will be linked to your company’s app name on the app page in in Teams app catalog in “Created By” section.
1. **Icons:** You are required to provided two PNG icons which will be used to represent your app in Teams; a 192X192 pixel colored icon for Teams app catalog and a 32X32 pixel monochrome icon for Teams app bar.

Once you successfully provide the details, a Teams app manifest, which is a `.zip file`, will be created and saved on your device. The Teams administrator of your tenant will then need to upload this app manifest to Teams admin center > **Manage apps**.

Once the app is successfully uploaded in the Teams admin center, it can be managed like any other app.

We highly recommend that you pin this app by default for users in your tenant so that they can easily access their company’s intranet resources without having to discover the app in Teams app catalog. See '[Manage your apps in the Microsoft Teams admin center](https://docs.microsoft.com/en-us/microsoftteams/manage-apps)' article for more details

For more detailed documentation, please refer: https://docs.microsoft.com/en-us/SharePoint/home-site-app?branch=home-site-app&source=docs#set-up-the-home-site-app
