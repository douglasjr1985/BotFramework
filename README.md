#Microsoft Bot Framework Hello World

These files get you started with a Microsoft Bot Framework "Hello World" chatbot on Heroku node.

The app is based on the MBF document <a href="https://docs.botframework.com/en-us/node/builder/overview/">version</a> and an earlier SarahSays <a href="https://blogs.msdn.microsoft.com/sarahsays/2016/06/01/microsoft-bot-framework-part-1/">version</a>.

One needs a Microsoft Account (I've had a Hotmail account since ages), then an <a href="https://portal.azure.com/">Azure Portal</a> account.

Then go to <a href="http://www.botframework.com">Microsoft Bot Framework</a> and sign in with your Microsoft Account. Register a bot. When you click Edit to edit the bot configuration, click "Manage Microsoft App and password" and make sure that the <a href="https://apps-dev.microsoft.com">Application Registration Portal</a> picks up your Bot Framework AppId. The APR has the ApplicationId for the bot (in the app.js, it is MY_APP_ID). Click "Generate New Password" to do just that. Copy as it is "MY_APP_PASSWORD in app.js.

Enter these two keys on the Heroku Settings page Reveal Config Vars.

For node on Heroku, one needs to set the port up as done in app.js and explained on StackOverflow.

The Heroku Domain on the config page point is the end point that goes on the Microsoft Bot Framework configuration (something like https://your_heroku_personal_app_name.herokuapp.com/api/messages) with messages/app (for app.js) tagged on to give https://your_heroku_personal_app_name.herokuapp.com/api/messages.

"Test connetion to your bot" at MBF gives the response "Accepted" if the Heroku account is recognised (but it does not mean that the bot is working properly, notably message replies).

Web and Skype integration at MBF are straightforward. We no longer have a working version of Hello World. However, the MBF version of the FIDICbot is at http://fidicbotmbf.herokuapp.com/ and on Skype @FIDICbot.

We suppose KiK integration will be OK although KiK does not seem to be accepting the creation of new bots these days.

We use Smooch for multichannel integration for the main FIDICbot integration on SMS, Telegram, Messenger and LINE. WeChat is proving complicated (getting an Official Account is OK; getting the OA authenicated so that one can at least have WeChat integration for WeChat users outside China is difficult).

The MBF version of FIDICbot for Skype has a read.me that serves as the online <a href="https://github.com/boswellp/MBF-FIDICbot/blob/master/README.md">help page</a>. This help page references the FIDIC.tips help page for the main (Smooch-hosted) version of FIDICbot (for SMS, Messenger, Telegram, LINE and <a href="http://fidic.pw">fidic.pw</a>) at <a href="http://fidic.tips/fidicbot">FIDIC.tips/FIDICbot</a>.
