# KhepriConnectorPhp

In the composer.json, on the require section add:

> "require": {

> "khepri/connector": "dev-master"

>  }

You need to update your composer

>  $ composer update

Here is a simple sample use case

>  <?php

>  require './vendor/autoload.php';

>  // Khepri URL (sandbox environment)

>  $khepri_url = 'http://sb.khepri.tech';

>  // Initialize the client with your  API-Key. You can find it on your Khepri account.

>  $api_key = 'MY_API_KEY';

>  // you can create your instance with your khepri account here we select the instance 1

>  $instance_id = 1;

>  // init

>  KhepriAPI::init($khepri_url, $api_key);

>  // Simple ask

>  $answer = KhepriAPI::ask($instance_id);

>  // Simple success

>  $chk = KhepriAPI::success($instance_id, $answer->solution);
