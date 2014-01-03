# github-streaker

Let a robot remind you to make a GitHub commit that day if you have not already. Keep that streaking going.

## Installation

### Production

```
heroku create
heroku addons:add scheduler
heroku addons:add sendgrid
heroku config:set TO=you@youremail.com
heroku config:set GITHUB_USERNAME=your_github_username
git push heroku master
```

Then go to <https://addons-sso.heroku.com/apps/your_app_name/addons/scheduler:standard> and set the UTC time to the appropriate time you'd like. For example, I want my reminder to check at 6pm Los Angeles time so I set it to 2am UTC.

![](image here)

### Development

```
cp .env.example .env
```

Configure with your credentials.

```
node ./tasks.js
```
