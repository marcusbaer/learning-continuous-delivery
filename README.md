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

# Deployment with Gitlab

- Deployment with AWS S3: https://about.gitlab.com/2016/08/26/ci-deployment-and-environments/
- About Gitlab environments: https://gitlab.com/help/ci/environments
- Cycle analytics: https://gitlab.com/help/user/project/cycle_analytics.md
