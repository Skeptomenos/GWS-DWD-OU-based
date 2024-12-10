# GWS-DWD-OU-based
Google Workspace Domain-wide-delegation OU-Based without secret key 

Setup steps

Enable and configure Google Workspace Marketplace SDK
https://console.cloud.google.com/apis/api/appsmarket-component.googleapis.com/googleapps_sdk
→ Enable OAuth Consent Screen and set to “internal” if needed
App Configuration
App Visibility: Private + Unlisted
Installation Settings: Admin Only Install
Select one App Integration
If you don’t need one, select Web App and enter a URL
Add needed API Scopes
Leave the default for email/profile
Add additional Scopes for access to Gmail, Drive etc.
Enter Developer Information
Store Listing
https://console.cloud.google.com/apis/api/appsmarket-component.googleapis.com/googleapps_sdk_publish
Fill all required fields for the store listing and publish the app
Google Admin Console
https://console.cloud.google.com/apis/api/appsmarket-component.googleapis.com/googleapps_sdk_publish
Click on the App-Listing link in the “Store Listing” Section of “Marketplace SDK”. You will not find the App over Workspace Admin.
Click “Admin install” and install the App for the needed OU/Group as an admin
The Installation can managed here https://admin.google.com/ac/apps/gmail/marketplace/apps?hl=en



Enable service account for Google Workspace Marketplace
Open the details of the service account that is used or that you have a credential file for.
At the bottom under Advanced settings click on Create Google Workspace Marketplace-compatible OAuth Client

Add Scopes
In case additional scopes for additional APIs need to be added the following steps need to be done.

Add Scopes in Marketplace SDK configuration in the GCP Project
https://console.cloud.google.com/apis/api/appsmarket-component.googleapis.com/googleapps_sdk

Authorize the new scopes in the Admin Console
https://admin.google.com/ac/apps/gmail/marketplace/apps

Other Information
The App will be added to the App-Launcher for the Users in the OU. It cannot be disabled. The link is taken out of “App Configuration” -> “App Url” and should be “meaningful”.


