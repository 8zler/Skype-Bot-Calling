# Skype-Bot-Calling
## Make your own Skype Bot that handle call from client

### 1. Download the SkypeBot Template
### 2. Add the SkypeBot Template to Visual Studio
#### Copy the .zip you've just download to %USERPROFILE%\Documents\Visual Studio 2015\Templates\ProjectTemplates\Visual C#
### 3. Open Visual Studio
#### Create a new project using the SkypeBot Template
### 4.Register your bot with https://dev.botframework.com/bots/new
#### Fill the required fields and create a Microsoft ID and Password by clicking the button "Create Microsoft ID and Password"
#### On this new page, set a name to your app, and copy/paste somewhere the App Id that have been generated
#### Click on "Generate a password for your app"
#### Copy/paste somewhere the password that appears on your screen
### 5. Open "Web.config" on Visual Studio
#### Identify MicroSoftAppId and MicrosoftAppPassword variable
##### Set the MicrosoftAppId value with the ID you've pasted somewhere before
##### Set the MicrosoftAppPassword value with the password you've pasted somewhere before
### 6. Download ngrok
#### It's a tool that provides you a public URL that creates a tunnel to your local host.
#### Once you've downloaded ngrok, run it with the ngrok.exe
#### A new terminal is now opened, so type : "ngrok -host-header=localhost 3999"
#### You can see on the terminal two forwading URL, copy/paster somewhere the https URL that is like this : https://xxxxxxx.ngrok.io
### 7. Go back to Web.config
#### Identify Microsoft.Bot.Builder.Calling.CallbackUrl variable
#### Set the value to the https URL you've pasted somewhere before and add "/api/calling/callback" so you have something like this : https://xxxxxxx.ngrok.io/api/calling/callback
### 8. Go to https://dev.botframework.com/bot and select the bot you've created before
#### Edit the details and set the "Messaging endpoint" to https://xxxxxxx.ngrok.io/api/messages
#### Save the modification
### 9. On the Channel section Edit the Skype Channel
#### In the Calls section, activate the 1:1 audio calls and set the "Calling Webhook" to https://xxxxxxx.ngrok.io/api/calling/call
