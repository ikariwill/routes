# Routes
Simple routing for WordPress.

[![Build Status](https://img.shields.io/travis/Upstatement/routes/master.svg?style=flat-square)](https://travis-ci.org/Upstatement/routes)
[![Coverage Status](https://img.shields.io/coveralls/upstatement/routes.svg?style=flat-square)](https://coveralls.io/r/Upstatement/routes?branch=master)
[![Packagist Downloads](https://img.shields.io/packagist/dt/Upstatement/routes.svg?style=flat-square)]()


### Usage
```php
/* functions.php */
Routes::map('myfoo/bar', 'my_callback_function');
Routes::map('my-events/:event', function($params) {
    $event_slug = $params['event'];
    $event = new ECP_Event($event_slug);
    Routes::load('single.php', array('event' => $event));
});
```
