# ![LOGO](logo.png) NPR Identity Service **flow**ground Connector

## Description

A generated **flow**ground connector for the NPR Identity Service API (version 2).

Generated from: https://api.apis.guru/v2/specs/npr.org/identity/2/swagger.json<br/>
Generated at: 2019-05-07T17:43:17+03:00

## API Description

The entry point to user-specific information

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Update the following status of the logged-in user for a particular aggregation

> After a successful call, this returns a User document with an updated list of affiliations.

*Tags:* `identity`

#### Input Parameters
* `Authorization` - _required_ - Your access token from the Authorization Service. Should start with `Bearer`, followed by a space, followed by the token.

### Update the logged-in user's favorite station(s)

> Right now, only the primary station can be changed. Previously selected stations will not be deleted, but the new station will be moved to first in the array.

*Tags:* `identity`

#### Input Parameters
* `Authorization` - _required_ - Your access token from the Authorization Service. Should start with `Bearer`, followed by a space, followed by the token.

### Get the latest state information about the logged-in user

> After a successful login, the client should send a `GET` call approximately once an hour to refresh the user data.

*Tags:* `identity`

#### Input Parameters
* `Authorization` - _required_ - Your access token from the Authorization Service. Should start with `Bearer`, followed by a space, followed by the token.

### Copy listening data from a temporary user account to the logged-in user's account

> This can and should only be used by clients who have access to the `temporary_user` grant type.<br/>
>     Third-party developers do not have access to this grant type by default, and will not need this endpoint.

*Tags:* `identity`

#### Input Parameters
* `Authorization` - _required_ - Your access token from the Authorization Service. Should start with `Bearer`, followed by a space, followed by the token.
* `temp_user` - _required_ - The temporary user's ID before the user registered or logged in

## License

**flow**ground :- Telekom iPaaS / npr-org-identity-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
