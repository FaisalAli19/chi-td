---
id: getting-started
title: Getting Started
sidebar_label: Getting Started
---

> COMPATIBILITY NOTE <br /> CHI requires Node.js >= 8.

These instructions will get you a copy of the project up and running on your local machine for development.

Clone the repository from here: https://github.com/FaisalAli19/CHI.git or Download the Zip file to your machine.

After cloning the repository successfully, navigate to the root of the project using `cd CHI`

## Installing dependencies

Run the following command from the root directory of the application.

```
npm install
```

## Configuring development environment

Create a .env file in the root directory of the project and add the following keys.

```
SENDGRID_KEY=
EMBEDLY_KEY=
AWS_KEY=
AWS_ACCESS_KEY_ID=
AWS_SECRET=
AWS_SECRET_ACCESS_KEY=
AWS_BUCKET=
CLOUDFRONT=
BITLY=
GIPHY_KEY=
NOUNPROJECT_KEY=
NOUNPROJECT_SECRET=
NLU_ID=
NLU_PASSWORD=
TONE_ANALYZER_ID=
TONE_ANALYZER_PASSWORD=
SPEECH_TO_TEXT_ID=
SPEECH_TO_TEXT_PASSWORD=
FACEBOOK_CLIENT_ID=
FACEBOOK_CLIENT_SECRET=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
TWITTER_CONSUMER_KEY=
TWITTER_CONSUMER_SECRET=
BUCKET_DIR='files/'
THUMB_DIR='thumbnails/'
MAX_FILE_SIZE=51457280
PORT=3000
SERVER_TYPE='dev'
```

## Running development server

> After you have ensured that all the environment variables are configured in the .env file

Running live reload server

```
npm run watch
```

Running server

```
npm start
```

Once you see the `Express server listening on port: 3000` message, open `http://localhost:3000` in a web browser.
