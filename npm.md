# NPM Cheet sheet

## First setup
* Add npm-global
  * add `.npm-global` to home directory
  * run `npm config set prefix /home/$USER_NAME$/.npm-global/`
  * export `/home/$USER_NAME$/.npm-global/bin` to PATH
## Setup project
* `npm init --yes` for generating default `package.json`
## Installing packages locally
* briefly `npm install <package-name>`
  * installing dependency for production: `npm install <package-name> [--save-prod]`
  * installing dependency for development only: `npm install <package-name> --save-dev`
## Updating packages locally
* for updating application run npm update to refresh all packages, listed in `package.json`
* so there should not be any outdated packages, which can be tracked with `npm outdated`
## Uninstalling packages locally
* breifly `npm uninstall <package-name>
  * to remove it from `package.json` run `npm uninstall --save <package-name>`
## Installing packages globally
* just run `npm install -g <package-name>`
## Updating packages globally
* for previously installed global packages run `npm update -g <package-name>`
