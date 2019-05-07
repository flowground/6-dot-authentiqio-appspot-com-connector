# ![LOGO](logo.png) Authentiq **flow**ground Connector

## Description

A generated **flow**ground connector for the Authentiq API (version 6).

Generated from: https://api.apis.guru/v2/specs/6-dot-authentiqio.appspot.com/6/swagger.json<br/>
Generated at: 2019-05-07T17:34:44+03:00

## API Description

Strong authentication, without the passwords.

## Authorization

This API does not require authorization.

## Actions

### Revoke an Authentiq ID using email & phone.<br/>
> <br/>
> If called with `email` and `phone` only, a verification code <br/>
> will be sent by email. Do a second call adding `code` to <br/>
> complete the revocation.

*Tags:* `key` `delete`

#### Input Parameters
* `email` - _required_ - primary email associated to Key (ID)
* `phone` - _required_ - primary phone number, international representation
* `code` - _optional_ - verification code sent by email

### Register a new ID `JWT(sub, devtoken)`<br/>
> <br/>
> v5: `JWT(sub, pk, devtoken, ...)`<br/>
> <br/>
> See: https://github.com/skion/authentiq/wiki/JWT-Examples

*Tags:* `key` `post`

### Revoke an Identity (Key) with a revocation secret

*Tags:* `key` `delete`

#### Input Parameters
* `PK` - _required_ - Public Signing Key - Authentiq ID (43 chars)
* `secret` - _required_ - revokation secret

### Get public details of an Authentiq ID.

*Tags:* `key` `get`

#### Input Parameters
* `PK` - _required_ - Public Signing Key - Authentiq ID (43 chars)

### HEAD info on Authentiq ID

*Tags:* `key` `head`

#### Input Parameters
* `PK` - _required_ - Public Signing Key - Authentiq ID (43 chars)

### update properties of an Authentiq ID.<br/>
> (not operational in v4; use PUT for now)<br/>
> <br/>
> v5: POST issuer-signed email & phone scopes in<br/>
> a self-signed JWT<br/>
> <br/>
> See: https://github.com/skion/authentiq/wiki/JWT-Examples

*Tags:* `key` `post`

#### Input Parameters
* `PK` - _required_ - Public Signing Key - Authentiq ID (43 chars)

### Update Authentiq ID by replacing the object.<br/>
> <br/>
> v4: `JWT(sub,email,phone)` to bind email/phone hash; <br/>
> <br/>
> v5: POST issuer-signed email & phone scopes<br/>
> and PUT to update registration `JWT(sub, pk, devtoken, ...)`<br/>
> <br/>
> See: https://github.com/skion/authentiq/wiki/JWT-Examples

*Tags:* `key` `put`

#### Input Parameters
* `PK` - _required_ - Public Signing Key - Authentiq ID (43 chars)

### push sign-in request<br/>
> See: https://github.com/skion/authentiq/wiki/JWT-Examples

*Tags:* `login` `post`

#### Input Parameters
* `callback` - _required_ - URI App will connect to

### scope verification request<br/>
> See: https://github.com/skion/authentiq/wiki/JWT-Examples

*Tags:* `scope` `post`

#### Input Parameters
* `test` - _optional_ - test only mode, using test issuer

### delete a verification job

*Tags:* `scope` `delete`

#### Input Parameters
* `job` - _required_ - Job ID (20 chars)

### get the status / current content of a verification job

*Tags:* `scope` `get`

#### Input Parameters
* `job` - _required_ - Job ID (20 chars)

### HEAD to get the status of a verification job

*Tags:* `scope` `head`

#### Input Parameters
* `job` - _required_ - Job ID (20 chars)

### this is a scope confirmation

*Tags:* `scope` `post`

#### Input Parameters
* `job` - _required_ - Job ID (20 chars)

### authority updates a JWT with its signature<br/>
> See: https://github.com/skion/authentiq/wiki/JWT-Examples

*Tags:* `scope` `put`

#### Input Parameters
* `job` - _required_ - Job ID (20 chars)

## License

**flow**ground :- Telekom iPaaS / 6-dot-authentiqio-appspot-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
