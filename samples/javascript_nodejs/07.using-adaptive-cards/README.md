# using adaptive cards sample
Bot Framework v4 using adaptive cards bot sample

This sample shows how to send an Adaptive Card.

## Prerequisites
- [Node.js][4] version 10.14 or higher
    ```bash
    # determine node version
    node --version
    ```

# To try this sample
- Clone the repository
    ```bash
    git clone https://github.com/Microsoft/botbuilder-samples.git
    ```
- In a terminal, navigate to `samples/javascript_nodejs/07.using-adaptive-cards`
    ```bash
    cd samples/javascript_nodejs/07.using-adaptive-cards
    ```
- Install modules
    ```bash
    npm install
    ```
- Start the bot
    ```bash
    npm start
    ```

# Testing the bot using Bot Framework Emulator **v4**
[Microsoft Bot Framework Emulator][5] is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the Bot Framework Emulator version 4.2.0 or greater from [here][6]

## Connect to the bot using Bot Framework Emulator **v4**
- Launch Bot Framework Emulator
- File -> Open Bot Configuration
- Navigate to `samples/javascript_nodejs/07.using-adaptive-cards` folder
- Select `using-adaptive-cards.bot` file

# Adaptive Cards
The Bot Framework provides support for Adaptive Cards.  See the following to learn more about Adaptive Cards.
- [Adaptive card][26]
- [Send an Adaptive card][27]

## Adding media to messages
A message exchange between user and bot can contain media attachments, such as cards, images, video, audio, and files.

# Deploy this bot to Azure
## Prerequisites
- [Azure Deployment Prerequisites][41]

## Provision a Bot with Azure Bot Service
After creating the bot and testing it locally, you can deploy it to Azure to make it accessible from anywhere.  To deploy your bot to Azure:

```bash
# login to Azure
az login
```

```bash
# set you Azure subscription
az account set --subscription "<azure-subscription>"
```

```bash
# provision Azure Bot Services resources to host your bot
msbot clone services --name "<your_bot_name>" --code-dir "." --location westus --sdkLanguage "Node" --folder deploymentScripts/msbotClone --verbose
```

### Publishing Changes to Azure Bot Service
As you make changes to your bot running locally, and want to deploy those change to Azure Bot Service, you can _publish_ those change using either `publish.cmd` if you are on Windows or `./publish` if you are on a non-Windows platform.  The following is an example of publishing

```bash
# run the publish helper (non-Windows) to update Azure Bot Service.  Use publish.cmd if running on Windows
./publish
```

### Getting Additional Help Deploying to Azure
To learn more about deploying a bot to Azure, see [Deploy your bot to Azure][40] for a complete list of deployment instructions.

# Further reading

- [Bot Framework Documentation][20]
- [Bot Basics][32]
- [Add media to messages][23]
- [Rich card types][24]
- [Activity processing][25]
- [Azure Bot Service Introduction][21]
- [Azure Bot Service Documentation][22]
- [Azure CLI][7]
- [msbot CLI][9]
- [Azure Portal][10]
- [Language Understanding using LUIS][11]
- [Restify][30]
- [dotenv][31]

[1]: https://dev.botframework.com
[4]: https://nodejs.org
[5]: https://github.com/microsoft/botframework-emulator
[6]: https://github.com/Microsoft/BotFramework-Emulator/releases
[7]: https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest
[9]: https://github.com/Microsoft/botbuilder-tools/tree/master/packages/MSBot
[10]: https://portal.azure.com
[11]: https://www.luis.ai
[20]: https://docs.botframework.com
[21]: https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0
[22]: https://docs.microsoft.com/en-us/azure/bot-service/?view=azure-bot-service-4.0
[23]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-add-media-attachments?view=azure-bot-service-4.0&tabs=javascript
[24]: https://docs.microsoft.com/en-us/azure/bot-service/rest-api/bot-framework-rest-connector-add-rich-cards?view=azure-bot-service-4.0
[25]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-concept-activity-processing?view=azure-bot-service-4.0
[26]: http://adaptivecards.io
[27]: https://docs.microsoft.com/en-us/azure/bot-service/nodejs/bot-builder-nodejs-send-rich-cards?view=azure-bot-service-3.0&viewFallbackFrom=azure-bot-service-4.0#send-an-adaptive-card
[30]: https://www.npmjs.com/package/restify
[31]: https://www.npmjs.com/package/dotenv
[32]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-basics?view=azure-bot-service-4.0
[40]: https://aka.ms/azuredeployment
[41]: ./PREREQUISITES.md
