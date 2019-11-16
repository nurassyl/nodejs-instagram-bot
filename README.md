
# NodeJS + Puppeteer Instagram Bot
![](https://i.imgur.com/1ug6S0N.jpg)
Instagram Bot that authenticates and login into an Instagram account, then using a number of hashtags creates engagement by liking posts and following users.

If account can't give likes or follows due to suspicious activity (in other words, account was temporaly blocked), bot deactivates for 24hs

  

## Software PreRequisites

* NodeJS v12 or higher https://nodejs.org/es/download/current/

* pm2 http://pm2.keymetrics.io/ (only if you want the app to automatically restart in case of unexpected crashing)

  

## Config

Create a .env file with the USERNAME and PASSWORD of the account. If you don't like the standard hashtags in *settings/hashtags.json* you can also add an array of hastags

![](https://i.imgur.com/GHE6b0R.png)

  

## Scripts

*  `yarn` or `npm install` installs the required modules.

*  `yarn start` or `npm run start` runs the bot without automatic restart in case of unexpected crashing

*  `yarn start --not-follow` or `npm run start --not-follow` runs the app without automatic restart and without the follow functionality

*  `yarn start --not-like` or `npm run start --not-like` runs the app without automatic restart and without the like functionality

*  `yarn monitor:start` or `npm run monitor:start` runs the app with automatic restart in case of error

*  `yarn monitor:stop` or `npm run monitor:stop` stops pm2 monitoring

*  `yarn monitor:start --not-follow` or `npm run monitor:start --not-follow` runs the app with automatic restart and without the follow functionality

*  `yarn monitor:start --not-like` or `npm run monitor:start --not-like` runs the app with automatic restart and without the like functionality

  

## Additional info

* HIGHLY recommendable to test with a throwable instagram account. DO NOT test with an account you can't afford to have suspended for 24hs

* To reduce chances of a temporal block or suspension, the more human-like is the account's activity, the better. If possible, make publications with the account. If possible, have the account linked to a facebook and twitter accounts. If possible, before using the bot with a new account log manually in a chromium browser in the same computer

* This bot does not support two-factor authentication.
