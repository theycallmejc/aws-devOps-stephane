# AWS CodeDeploy Sample Web App

A static sample page packaged with an AWS CodeDeploy application specification and Linux lifecycle scripts.

## Project contents

- [`MyNimoRepo/index.html`](MyNimoRepo/index.html) is the sample web page.
- [`MyNimoRepo/appspec.yml`](MyNimoRepo/appspec.yml) copies the page to `/var/www/html/` and declares install, start, and stop hooks.
- `MyNimoRepo/scripts/` contains `install_dependencies`, `start_server`, and `stop_server`.

## Deployment notes

The AppSpec targets Linux and runs lifecycle hooks as `root`. Review the scripts, CodeDeploy agent setup, and target host configuration before deploying. This repository does not include account-specific AWS infrastructure.