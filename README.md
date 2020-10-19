# Nähstube

Nähstube is a Online-Platform for self-sewn products.

![version-0.0.1](https://img.shields.io/badge/version-0.0.1-blue?style=flat)
![version-0.0.1](https://img.shields.io/badge/license-GPLv3-blue?style=flat)

## Installation

Installation instructions are coming soon when the MVP is released.

### Configuration

You can configure the platfrom via environment variables.

| Environment Variable  | Description                   | Required |
| :-------------------- | :---------------------------: | -------: |
|  NAEHSTUBE_SECRET_KEY | Secret key for the django app | Y        |
|  DATABASE_NAME        | Database name                 | Y        |
|  DATABASE_USER        | Database user                 | Y        |
|  DATABASE_PASSWORD    | Database password of the user | Y        |
|  DATABASE_HOST        | Database host                 | Y        |
|  DATABASE_PORT        | Database port                 | Y        |

## Usage

If you want to use this source code as the basis for your own platofrm, feel free to fork it. Please notice the license agreements and make contributions to the code base.

## Support

If you have any problem using this source code for your own platform or by using a platform based on this source code, please [open an issue](https://github.com/ityreh/naehstube/issues).

## Roadmap

The Roadmap describes upcoming features for the nexte releases.

### MVP Nähstube-1.0.0

* Navigation
* Admin
* Products
* Saisons
* Cart
* User
* Information

### Nähzauber Nähstube-1.1.0

* Crafting

### Saisons Nähstube-1.2.0

* Saisons

### vNext Nähstube-1.x.0

* Filter
* Rating
* ...

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

### Environment Setup

For local development you need a Python environment (e.g. virtualenv) with the required packages. In addition to that you need a PostgreSQL database with test data.

#### Virtualenv

    pip install virtualenv
    mkdir ~/.virtualenv
    virtualenv -p python3 ~/.virtualenv/naehstube
    source ~/.virtualenv/naehstube/bin/activate

#### Requirements

You can install the required packages with the requirements.txt file.

    pip install -r requirements/local.txt

#### PostgreSQL

You need to setup a PostgreSQL database server and configure the app accordingly as listed in the configuration section. When the setup is done you can make the migrations.

    python manage.py makemigrations --settings=config.settings.local
    python manage.py migrate --settings=config.settings.local

Do these migrations every time you create a new app or model.

### Django

#### Run on local test server

To run the platform on a local test server you can use manage.py with the local configuration.

    python manage.py runserver --settings=config.settings.local

#### Add a new app

If you want to add a new app, you can use the django-admin script inside the src folder.

    django-admin startapp my_app

## Authors and acknowledgement

This platform is made for my wife and a lot of the ideas that are implemented here come from her.

## License

[GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007](./LICENSE)

## Project status

The project is still in development.
