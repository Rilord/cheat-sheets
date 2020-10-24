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
## Installing global packages 
* just run `npm install -g <package-name>`
## Updating global packages 
* for previously installed global packages run `npm update -g <package-name>`
* To find all outdated global packages run `npm outdates -g --depth=0`
* To update ALL global packages run `npm update -g`
## Uninstalling global packages 
* briefly run `npm uninstall -g <package-name>`

