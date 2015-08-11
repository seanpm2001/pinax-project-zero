# Pinax Project Zero

[![Join us on Slack](http://slack.pinaxproject.com/badge.svg)](http://slack.pinaxproject.com/)

This project lays the foundation for all other [Pinax starter projects](https://github.com/pinax/pinax-projects/blob/master/README.md#projects). It provides the project directory layout and [bootstrap-based theme](https://github.com/pinax/pinax-theme-bootstrap).

The source code for this project template has moved to the [zero branch](https://github.com/pinax/pinax-projects/tree/zero) of [pinax-projects](https://github.com/pinax/pinax-projects/).

##### Prerequisites

* pip
* npm


##### Getting Started

You can get started with this project by doing the following:

```
pip install virtualenv
virtualenv mysiteenv
source mysiteenv/bin/activate
pip install Django==1.8.3
django-admin.py startproject --template=https://github.com/pinax/pinax-project/zipball/zero mysite -n webpack.config.js
cd mysite
chmod +x manage.py
pip install -r requirements.txt
npm install
./manage.py migrate
./manage.py loaddata sites
./manage.py runserver
```

##### Static Media

Static media is managed by `webpack`, and is configured out of the box to watch
and rebuild on change by running:

```
npm run watch
```

We recommend running that in a separate terminal window than `manage.py runserver`
if and when you are editing `js` or `less` files.
