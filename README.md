# EtimApi REST Client

This EtimApi REST Client can be used to see the EtimApi REST services in action.

This project is a PhpStorm port of this: https://bitbucket.org/3xt/etimapi-rest-client/src/master/

For further reference: https://etimapi.etim-international.com/

> Version v1.0 is deprecated. This version will stay active, but further development will take place on v2.0

## v2.0

- Great ways to search and filter the ETIM classifications.
- More consistent services and models
- Possibility to get a complete selection/release with one servicecall. Ability to use paging.

## v1.0

- Deprecated

## Prerequisites

- client_id/client_secret from ETIM International
- Installation of git
- Installation of PhpStorm
- Installation of the REST Client extension

## Getting Started

- Get a client_id/client_secret at [https://etimapi.etim-international.com/](https://etimapi.etim-international.com/)
- Download and install git [git](https://git-scm.com/downloads)
- Download and install PhpStorm. [https://www.jetbrains.com/phpstorm/](https://www.jetbrains.com/phpstorm/)
- Start PhpStorm. Search for and install plugin if not present [HTTP Client](https://www.jetbrains.com/help/phpstorm/http-client-in-product-code-editor.html)
- Open a command prompt and clone this repository with git

## Settings
Some variables are used from the settings file. 
* Create a http-client.env.json file in the root directory of the project --> "/http-client.env.json"
* Copy this into the http-client.env.json file:

```json
{
  "production": {
    "authUrl": "https://etimauth.etim-international.com",
    "baseUrl": "https://etimapi.etim-international.com",
    "client_id": "",
    "client_secret": "",
    "scope": "EtimApi"
  }
}
```
* Fill in the client_id/client_secret you received from ETIM International

## Start you first request
* Open one of the .http files in PhpStorm
* Switch the environment in the Status bar to "production"
* Click on "Send Request" in the "ClientCredentialsGrant". Or place your cursor between ### and ### and use the keyboard shortcut ctrl-r. This service will fetch an access-token that will be used in subsequential requests.
* Next click on "Send Request" above one of the service calls.
