## Notification !

Attention! This is a product remade by KENLIEPLAYS, specifically Facebook-Chat-Api (Mod by: Fca-Horizon-Remake (deleted) which includes previous author UIRI and main author: HarryWakazaki, the current author is not responsible for any liabilities!). If there are errors, try using another product!

## Support For : 

+ Support English, VietNamese !,
+ All bot if using listenMqtt first.

# API for Messenger ChatBot.

Facebook now has and allows users to create API for chatbots 😪 Check it out here => [Here](https://developers.facebook.com/docs/messenger-platform).

### This API may cause you to pay for an account like you've never had before, so be careful =)).

Note! If you want to use this API, please check the documentation here [Here](https://github.com/Schmavery/facebook-chat-api).

## Download 

If you want to use it, please download it by:
```bash
npm i fca-kenlie-plays
```
or
```bash
npm install fca-kenlie-plays
```

It will download to your node_modules (your library) - Note that Replit won't show it, just search 😪

### Download the latest version or update.

If you want to use the latest version or update, go to the terminal or command prompt and enter :
```bash
npm install fca-kenlie-plays@latest
```
Hoặc
```bash
npm i fca-kenlie-plays@latest
```

## If you want to test the API 

The benefit of this is that you won't waste time paying for an account and you'll have an account 😪
Please use with a test account => [Facebook Whitehat Accounts](https://www.facebook.com/whitehat/accounts/).

## How to use

```javascript
const login = require("fca-kenlie-plays"); // Retrieve from the library 

// Login
login({email: "Gmail Account", password: "Your Facebook password"}, (err, api) => {

    if(err) return console.error(err); // In case of error

    // Create an automated bot that mimics you:
    api.listenMqtt((err, message) => {
        api.sendMessage(message.body, message.threadID);
    });

});
```

The result is that it will mimic you like the picture below:
<img width="517" alt="screen shot 2016-11-04 at 14 36 00" src="https://cloud.githubusercontent.com/assets/4534692/20023545/f8c24130-a29d-11e6-9ef7-47568bdbc1f2.png">

If you want to use advanced features, use the types of bots listed above!

## List

You can read the full API at => [here](DOCS.md).

## Installation for Mirai: 

You need to go to the Mirai.js file, then find the line
```js
    var login = require('tùy bot'); 
    /* It may be :
        var login = require('@maihuybao/fca-Unofficial');
        var login = require('fca-xuyen-get');
        var login = require('fca-unofficial-force');
        var login = require('fca-horizon-remake');
    ...   
    */
```

And replace it with:

```js
    var login = require('fca-kenlie-plays')
```

Then just run normally!

## Self-study

If you want to self-study or create a bot for yourself, go here to read its functions and how to use it => [Link](https://github.com/Schmavery/facebook-chat-api#Unofficial%20Facebook%20Chat%20API)

------------------------------------

### Save login information.

To save, you need an Apstate type (Cookie, etc,..) to save or use a login code as above to login!

And this mode is already available in some bots, so you can rest assured!

__Guide with Appstate__

```js
const fs = require("fs");
const login = require("fca-kenlie-plays");

var credentials = {email: "FB_EMAIL", password: "FB_PASSWORD"}; // account information

login(credentials, (err, api) => {
    if(err) return console.error(err);
    // login
    fs.writeFileSync('appstate.json', JSON.stringify(api.getAppState(), null,'\t')); //tạo appstate
});
```

Or easier (professional), you can use => [c3c-fbstate](https://github.com/c3cbot/c3c-fbstate) You can also get Fbstate and rename it to Apstate! (appstate.json)

------------------------------------

## FAQS

FAQS => [Link](https://github.com/Schmavery/facebook-chat-api#FAQS)