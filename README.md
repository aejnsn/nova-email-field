# Laravel Nova Email Field
An email input and mailto link field for Laravel Nova

[![Latest Version on Packagist](https://img.shields.io/packagist/v/inspheric/nova-email-field.svg?style=flat-square)](https://packagist.org/packages/inspheric/nova-email-field)
[![Total Downloads](https://img.shields.io/packagist/dt/inspheric/nova-email-field.svg?style=flat-square)](https://packagist.org/packages/inspheric/nova-email-field)

## Installation

Install the package into a Laravel app that uses [Nova](https://nova.laravel.com) with Composer:

```bash
composer require inspheric/nova-email-field
```

## Usage

Add the field to your resource in the ```fields``` method:
```php
use Inspheric\Fields\Email;

Email::make('Email')
    ->rules('email', /* ... */),
```

The field extends the `Laravel\Nova\Fields\Text` field, so all the usual methods are available.

It is recommended that you include the standard `email` validation rule, as it is not automatically added.

### Options

Make the field display as a mailto link on the detail page:

```php
Email::make('Email')
    ->clickable(),
```

## Appearance
### Index
![index-field](https://raw.githubusercontent.com/inspheric/nova-email-field/master/docs/index-field.png)

The field is displayed as a plain `<span>` element.

### Detail
![detail-field](https://raw.githubusercontent.com/inspheric/nova-email-field/master/docs/detail-field-plain.png)

The field is displayed as a plain `<span>` element.

### Detail (clickable)
![detail-field-clickable](https://raw.githubusercontent.com/inspheric/nova-email-field/master/docs/detail-field-clickable.png)

The field is displayed as an `<a href="mailto:...">` element.

### Form
![form-field](https://raw.githubusercontent.com/inspheric/nova-email-field/master/docs/form-field.png)

The field is displayed as an `<input type="email">` element.