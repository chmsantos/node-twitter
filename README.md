Twitter Reply
=====

A twitter bot based on 'reply' for NodeJS.

##Usage:

####Prerequisites:

Create a twitter app:

- go to https://dev.twitter.com/
- sign in with an account or create one (¡WARNING: YOU MAY FLOOD TWITTER WITH TWEETS FROM THIS ACCOUNT. BE CAREFUL!)
- add a new application
- go to the settings for the app, and set it to "Read & Write" Access
- go to the application credentials page and generate an access token in the "Your access token" section

you'll use the tokens from this page later. Keep it open.

####Local Setup:

All that you need to do is create a new file named runtime.js inside the config folder, and update this:
    {
      "twitter" : {
        "consumer_key" : "<your consumer key>",
        "consumer_secret" : "<your consumer key>",
        "access_token_key" : "<your access token>",
        "access_token_secret" : "<your access token secret>"
      },
      "keywords" : "words to match in tweet",
      "match" : "a string or regex. (capture groups are allowed)",
      "replies" : [
        "some reply. Can reference parts of the tweet like [user.screen_name] or regex matches like $1"
      ],
      "max_replies_per_minute" : 6,
      "in_reply_to" : true
    }

This code is based on: Jesse Ditson's reply bot running on NodeJS