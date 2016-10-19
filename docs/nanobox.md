# Slackin with Nanobox
This is the a nanobox deployable version of [Slackin](https://github.com/rauchg/slackin) and is pre-configured and nearly ready to run with [nanobox](https://nanobox.io/)!

## Up and Running

``` bash

# clone the code
git clone https://github.com/nanobox-quickstarts/nanobox-slackin.git

# cd into the slackin app
cd nanobox-slackin

# build runtime and compile application
nanobox build

# deploy runtime to dev environment
nanobox dev deploy

# add environment variables to dev environment*
nanobox dev evar add SLACK_COC="${SLACK_COC}",SLACK_CHANNELS="${SLACK_CHANNELS}",SLACK_SUBDOMAIN="${SLACK_SUBDOMAIN}",SLACK_API_TOKEN="${SLACK_API_TOKEN}",PORT=8080

# add a convenient way to access your app from the browser
nanobox dev dns add slackin.nanobox.dev

# start the dev environment and run the app server
nanobox dev run
```
*before running in production, you will need to [add the environment variables](https://docs.nanobox.io/app-config/environment-variables/#adding-environment-variables-in-the-dashboard) to your production app

Visit the app from your favorite browser at: `slackin.nanobox.dev:8080`

### Now What?
For more details about how this works or for more advanced topics related to running node applications on nanobox, visit [guides.nanobox.io/nodejs/](https://guides.nanobox.io/nodejs/)
