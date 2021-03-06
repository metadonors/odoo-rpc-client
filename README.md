# Odoo RPC Client for PHP

Odoo RPC Client is a PHP library providing an easy way to interact with your Odoo models. Is is inspired by the great [OdooRPC](https://github.com/OCA/odoorpc) Python library.

It supports access to all data models methods including custom api methods with an API similar to the server-side API.

Here is how it works

```php
use OdooRPCClient\Client;

$odoo = new Client('http://localhost');

$odoo->login('odoo_database_name','username','password');

// current user
print_r($odoo->env->user);

$ids = $odoo->env['res.partner']->search();
$partner_ids = $odoo->env['res.partner']->browse($ids);

foreach($partner_ids as $partner)
{
    echo $partner->name . "\n";
    echo $partner->company_id->name . "\n";
}


```

# Documentation

Is coming soon...

# Roadmap 

It is planned to support:

- Supporting Internationalization
- Odoo databases administration

# Supported Odoo server versions

OdooRPCClient is tested on all major releases of Odoo (starting from 8.0).

# Bug Tracker

Bugs are tracked on [GitHub Issues](https://github.com/metadonors/odoo-rpc-client/issues). In case of trouble, please check there if your issue has already been reported. If you spotted it first, help us smash it by providing detailed and welcomed feedback.

# Credits

The awesome [OdooRPC](https://github.com/OCA/odoorpc) for inspiration.

## Contributors

- Fabrizio Arzeni 

Do not contact contributors directly about support or help with technical issues.


