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

Deployment is using 4 jobs:

1. unit test
2. build
3. deploy staging (pages) to http://<username>.gitlab.io/<projectname>/
4. deploy production (AWS S3)

Read more about deployments with Gitlab here:

- About Gitlab environments: https://gitlab.com/help/ci/environments
- About Gitlab variables: http://docs.gitlab.com/ee/ci/variables/README.html
- Cycle analytics: https://gitlab.com/help/user/project/cycle_analytics.md
- Integration with Slack: https://api.slack.com/incoming-webhooks
- Deployment with AWS S3: https://about.gitlab.com/2016/08/26/ci-deployment-and-environments/

Deployment with Gitlab job to AWS S3 requires these secret variables:

- S3_BUCKET_NAME
- S3_BUCKET_FOLDER
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- AWS_DEFAULT_REGION (optional)

# Deployment with AWS S3

    $ npm run generate
    $ aws s3 cp ./dist s3://yourbucket/ --recursive
    
# Haproxy

- https://www.brianchristner.io/how-to-scale-a-docker-container-with-docker-compose/
- https://serversforhackers.com/load-balancing-with-haproxy
- http://blog.hypriot.com/post/docker-compose-nodejs-haproxy/
