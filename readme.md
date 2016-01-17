# This is a cloneable repo to get started with deployd#

## Installation ##

1) set env variable DPD_SERVER_ROOT so the server knows its own address
2) install nodejs
3) install dependancies
4) run the server:
`
export DPD_SERVER_ROOT=address.to.your.server.tld
cd teamchat-test
npm install 
node production.js
`
then point your browser to:
http://localhost:2403/ or your DPD_SERVER_ROOT

## code structure and hints ##
node_modules - dependancies
public - where the static assets are
dpd.js - this project relies on the deployd.com framework.  dpd.js presents tools for interacting with the REST api's deployd provides
resources 
    - these are all accessable at http://localhost:2403/dashboard
    - they provide REST endpoints at /
    - example resources/form/get.js is accessable from http://localhost:2403/form?query_key=value or from the front end or other reasorces by calling the method dpd.form.get({query_key:value})

# useful aliases #
alias debug='nodemon --debug dev.js --watch dev.js package.json'
alias ins='/usr/bin/open -a "/Applications/Google Chrome.app" "http://127.0.0.1:8080/?ws=127.0.0.1:8080"'
alias inspect='node-inspector --no-preload & ins'
