Opauth-Cpro-Common
=============
[Opauth][1] strategy for cPRO authentication.

Implemented based on http://developer.github.com/v3/oauth/ using OAuth2.

Opauth is a multi-provider authentication framework for PHP.

Demo: http://opauth.org/#github

Getting started
----------------
1. Install Opauth-Cpro-Common:
   ```bash
   cd app/Plugin/Opauth/Strategy 
   git clone https://github.com/uwcirg/opauth-cpro-common.git CproCommon
   ```

2. Register the cPRO application/intervention at the appropriate
   cPRO Portal URL, i.e. `https://mpower.cirg.washington.edu/client`
   - Enter Authorized URL: (i.e. the callback URL for the
     application/intervention being install i.e.
     `http://fqdn/application-path/truenth/oauth2callback`
   
3. Configure Opauth-Cpro-Common strategy with `client_id` and `client_secret` 
   returned from the portal `/client` request.

4. Direct user to `http://fqdn/application-path/truenth` to authenticate


Strategy configuration
----------------------

Required parameters:

```php
<?php
'GitHub' => array(
	'authorize_url' => 'PORTAL AUTHORIZE URL',
	'access_token_url' => 'PORTAL TOKEN URL',
	'base_url' => 'PORTAL API URL',
	'client_id' => 'YOUR CLIENT ID',
	'client_secret' => 'YOUR CLIENT SECRET'
)
```

Optional parameters:
`scope`, `state`

License
---------
Opauth-Cpro-Common is MIT Licensed  
Copyright © 2015 University of Washington 

[1]: https://github.com/uzyn/opauth
