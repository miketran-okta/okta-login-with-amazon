# okta-login-with-amazon
This project provides instructions on how to support Login With Amazon with Okta

## Prerequisites

- An Amazon Developer Account
- An Okta tenet which can be setup <a href="https://developer.okta.com/signup/">here</a>

## Setup & Deployment

- Under Login with Aamzon, setup a new Security Profile
- Under Web Settings, fill out the Allowed Origins and the Allowed Return URLs

<img src="https://github.com/miketran-okta/okta-login-with-amazon/blob/master/LWA-1.png"/>

- In your Okta tenet, select Security -> Identity Providers
- Select Add Identity Provider -> Add OpenID Connect IdP

<img src="https://github.com/miketran-okta/okta-login-with-amazon/blob/master/LWA-2.png"/>

- Enter the Aamazon Client ID and Client Secret
- Under Scopes, select *profile*
- Under Issuer and JWKS Endpoint, enter the URL of your Okta tenet
- Under Authorization Endpoint, enter *https://www.amazon.com/ap/oa*
- Under Token Endpoint, enter *https://api.amazon.com/auth/o2/token*
- Under Userinfo Endpoint, enter *https://api.amazon.com/user/profile*

<img src="https://github.com/miketran-okta/okta-login-with-amazon/blob/master/LWA-3.png"/>

- Select Show Advanced Settings. Under IdP Username, ensure *idpuser.email* is provided
- Select Add Identity Provider
- Record the "IdP ID"

<img src="https://github.com/miketran-okta/okta-login-with-amazon/blob/master/LWA-4.png"/>

## Login

Access the following link with Idp ID

https://dev-123456.oktapreview.com/sso/idps/[Idp_ID]



