# LIRI bot
### Overview

This tool is a command line node app that takes in parameters and returns specific data.

### Setup

1. Create the following files in a root project folder:
  * `key.js`
  * `liri.js`
  * `random.txt`

For beginners, new files are created by navigating to your root project folder via terminal and entering `touch` followed by the name of the file above with the file extension (example: `touch keys.js` creates the keys.js file).

2. Install the following npm dependencies in your project folder by entering the folling npm commands in your terminal:
  * `npm init -y` to initialize a `package.json` file for your project
  * `npm i node-spotify-api` [node-spotify-api](https://www.npmjs.com/package/node-spotify-api).
  * `npm i twitter` [Twitter for Node.js](https://www.npmjs.com/package/twitter).
  * `npm i dotenv` [dotenv](https://www.npmjs.com/package/dotenv).
  * `npm i request` [request](https://www.npmjs.com/package/request).

3. Make a `.gitignore` file (see below) and add the following lines to it. This will tell git not to track these files, and thus they won't be committed to Github.


```
node_modules
.DS_Store
.env
```
To create a `.gitignore` file, run the following in your project folder:

* `curl https://raw.githubusercontent.com/github/gitignore/master/Global/macOS.gitignore -o ~/.gitignore`

4. Next, setup your Spotify & Twitter Developer API credentials (google this for an easy setup).

[Twitter Apps](https://apps.twitter.com/)
[Spotify Developer](https://beta.developer.spotify.com/)

Then, create a file named `.env`, add the following to it, replacing the values with your API keys (no quotes) once you have them:

```js
# Spotify API keys

SPOTIFY_ID=your-spotify-id
SPOTIFY_SECRET=your-spotify-secret

# Twitter API keys

TWITTER_CONSUMER_KEY=your-twitter-consumer-key
TWITTER_CONSUMER_SECRET=your-twitter-consumer-secret
TWITTER_ACCESS_TOKEN_KEY=your-access-token-key
TWITTER_ACCESS_TOKEN_SECRET=your-twitter-access-token-secret

```

* This file will be used by the `dotenv` package to set what are known as environment variables to the global `process.env` object in node. These are values that are meant to be specific to the computer that node is running on, and since we are gitignoring this file, they won't be pushed to github &mdash; keeping our API key information private.

* In order to clone this repo, create your own `.env` file for it to work (this file is not shown in the because it is listed in the `.gitignore` file.

5. You will need API Keys for:
	*	[Twitter] (https://apps.twitter.com/app/new)
	* 	[Spotify] (https://developer.spotify.com/my-applications/#!/)
