# Requent [![Build Status](https://travis-ci.org/heera/requent.svg?branch=master)](https://travis-ci.org/heera/requent) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/heera/requent/master/LICENSE)

An elegant, light-weight GQL (Graph Query Language) like interface for Eloquent with zero configuration. It maps a request to eloquent query and transforms the result based on query parameters. It also supports to transform the query result explicitly using user defined transformers which provides a more secured way to exchange data from a public API with minimul effort.

## Installation

Add the following line in your "composer.json" file within "require" section and run `composer install` from terminal:

    "sheikhheera/requent": "1.0.*"

Once the installation is finished then you can start using it without any configurations. The following example is the most basic usage:

```php
<?php

namespace App\Http\Controllers;

use App\Http\Controllers\Controller;
use Requent\Requent;
use App\User;

class HomeController extends Controller
{
	public function fetch($id = null)
	{
		return app(Requent::class)->resource(User::class)->fetch($id);
	}
}
```
