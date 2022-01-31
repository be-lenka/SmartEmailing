# SmartEmailing

Easy way to interact with SmartEmailing API from PHP

## Installation

The best way to install this component is using [Composer](http://getcomposer.org/):

```sh
$ composer require belenka/smartemailing
```

Then it is required to add the following lines to config.neon:

```
parameters:
	smartemailing:
		username: <smartemailing_username>
		token: <smartemailing_api_token>

services:
	- BeLenka\SmartEmailing(%smartemailing.username%, %smartemailing.token%)
```

## Usage

Insert a new contact into SmartEmailing lists:

```
$this->smartEmailing->importContact($email, $name, $surname, $language, $contactLists, $properties, $customFields, $purposes, $settings);
```

Insert a order data into SmartEmailing lists:

```
$this->smartEmailing->importOrders($data);
```

Get an exisitng contact by email:

```
$this->smartEmailing->getContactsByEmail($email);
```

Get all contacts:

```
$this->smartEmailing->getContacts();
```

Get an exisitng contact by user's ID:

```
$this->smartEmailing->getContact($id);
```




