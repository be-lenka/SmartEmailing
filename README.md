# SmartEmailing

Easy way to interact with SmartEmailing API from PHP

## Installation

The best way to install this component is using [Composer](http://getcomposer.org/):

```sh
$ composer require be-lenka/smartemailing
```

Then it is required to add the following lines to config.neon:

```neon
parameters:
	smartemailing:
		username: <smartemailing_username>
		token: <smartemailing_api_token>

services:
	- BeLenka\SmartEmailing(%smartemailing.username%, %smartemailing.token%)
```

## Usage

Insert a new contact into SmartEmailing lists:

```php
$this->smartEmailing->importContact($email, $name, $surname, $language, $contactLists, $properties, $customFields, $purposes, $settings);
```

Insert a order data into SmartEmailing lists:

```php
$this->smartEmailing->importOrders($data);
```

Get an exisitng contact by email:

```php
$this->smartEmailing->getContactsByEmail($email);
```

Get all contacts:

```php
$this->smartEmailing->getContacts();
```

Get an exisitng contact by user's ID:

```php
$this->smartEmailing->getContact($id);
```




