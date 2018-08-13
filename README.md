droplet.mokolabs.com
====================

This is the default app for droplet.mokolabs.com. This app contains a static, single-page web app which can be accessed from droplet.mokolabs.com.

Background: I have deployed a couple of small apps on Digital Ocean using dokku. But, by default, dokku will display the first available app it finds at droplet.mokolabs.com. But, since it's really not good practice for an app to available from two domains (droplet.mokolabs.com and the canonical domain for the app itself), droplet.mokolabs.com should load a different app.

So I created this placeholder app which contains a static index.html file. Then, by deploying the app to dokku with an app name of `00-default`, dokku will always load this app first and it will become the homepage for droplet.mokolabs.com.

## Getting started

### Clone the app
1. `cd Sites/` (or wherever you like to store projects locally)
2. `git clone git@github.com:mokolabs/droplet.mokolabs.com.git 00-default`

## Deploy the app
The app is hosted on a dokku-managed droplet on Digital Ocean.

### Create the app with dokku
1. Login to the droplet via Terminal.
2. Run `dokku apps:create 00-default` to create an app named `00-default`

### Push the app to dokku
1. `git remote add droplet dokku@droplet.mokolabs.com:00-default` to add droplet remote
2. `git push droplet master` to deploy the changes
