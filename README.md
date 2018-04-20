# Droplet
=========

This is the default droplet for droplet.mokolabs.com. This droplet contains a static, single-page web app which can be accessed from droplet.mokolabs.com.

Background: we've deployed a couple of small sites on Digital Ocean using dokku. But, by default, dokku will show the first app it finds at droplet.mokolabs.com, so we created this static site as a placeholder.

## Getting started

### Clone the app
1. `cd Sites/` (or wherever you like to store projects locally)
2. `git clone git@github.com:mokolabs/droplet.git droplet`

## Deploy the app
The app is hosted on a dokku-managed droplet on Digital Ocean.

1. `git remote add droplet dokku@droplet.mokolabs.com:00_default` to add droplet remote
2. `git push droplet master` to deploy the changes
