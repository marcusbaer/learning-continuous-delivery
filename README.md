# Example project

Project demonstrates somewhat.

# Deployments with Now.sh

Run the following command:

    $ now

# Deployments with Heroku

To deploy with Heroku some config is required. 

    $ heroku config:set NPM_CONFIG_PRODUCTION=false
    $ heroku config:set HOST=0.0.0.0
    $ heroku config:set NODE_ENV=production