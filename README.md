<h1 align="center">
  <br>
   <img src="https://app.functionize.com/views/images/logo/logo-small.png"/>
  <br>
</h1>
<p align="center">
<a href="https://gitlab.com/rahul28/Gitlab-CI-with-Functionize/commits/master"><img alt="pipeline status" src="https://gitlab.com/rahul28/Gitlab-CI-with-Functionize/badges/master/pipeline.svg" /></a>
<p align="center">
  This repository contains Example Of Intregrating <strong>Functionize Smart Testing Tool </strong>with <strong>Gitlab CI/CD</strong>
</p>

### Including Functionize TestsSuite in CodeBuild CI.

Requires Active Functionize.com Account.

Decalare Stage Name
```bash
stages:
  - deploy-functionizecli
```

Include This Snippet In any of the Stage/Phase, Where you want to run test-cases.
```bash
Functionize-cli Deployment:
  stage: deploy-functionizecli
- git clone https://functionize@bitbucket.org/functionize/functionizecli.git /opt/functionizecli
- cd /opt/functionizecli
- npm install
- npm install -g
- wget -O - https://bitbucket.org/functionize/functionizecli/raw/master/ThirdParty_run.sh | bash
```


## Parameters

You Need to Pass Some Parameters To make it work. Everything Can be get from app.functionize.com acccount.

| `Parameter`               | `Value`               |
|-------------------------|---------------------------|
| DEPLOYMENT_TIME | Timeout in Sec
| YOUR_SECRET_KEY | Client ID
| YOUR_API_KEY |  Client Secret
| PROJECT_DEPLOYMENT_ID | Orechestration_ID
