<img src="https://i.morioh.com/201102/4013dde6.webp" width="300" height="100">

# Laravel 8 Authentication with Laravel UI

    Step 1: Set Up Laravel Project.
    Step 2: Set Up Database Details in ENV.
    Step 3: Install Laravel UI.
    Step 4: Step up Auth Scaffolding.
    Step 5: Run npm install && npm run dev command.
    Step 6: Migrate your database.
    Step 7: Configuration

## Step 1: Set Up Laravel Project

    composer create-project --prefer-dist laravel/laravel AnyAppName
  
## Step 2: Set Up Database Details in ENV

   .env

	DB_CONNECTION=mysql
	DB_HOST=127.0.0.1
	DB_PORT=3306
	DB_DATABASE=database_name
	DB_USERNAME=database_user_name
	DB_PASSWORD=database_password

## Step 3: Install Laravel UI

	composer require laravel/ui

## Step 4: Step up Auth Scaffolding 

   use anyone for you requirements

  1. Without Auth:

        php artisan ui bootstrap

        php artisan ui vue

        php artisan ui react

  2. With Auth:

        php artisan ui bootstrap --auth

        php artisan ui vue --auth

        php artisan ui react --auth

## Step 5: Run npm install && npm run dev command

	npm install && npm run dev

## Step 6: Migrate your database

    php artisan migrate

Now our Laravel 8 authentication system is ready. you can run serve 

    php artisan serve
	

## Step 7: Configuration

## 1. resources/js/components/Example.js

    import React from 'react';

    import ReactDOM from 'react-dom';

    function Example() {

        return (
            <div className="container">
                <div className="row justify-content-center">
                    <div className="col-md-8">
                        <div className="card">
                            <div className="card-header">Example Component</div>
                            <div className="card-body">I'm an example component!</div>
                        </div>
                    </div>
                </div>
            </div>
        );
    }

    export default Example;

    if (document.getElementById('example')) {

        ReactDOM.render(<Example />, document.getElementById('example'));
    }

## 2. resources/js/components/app.js

    require('./bootstrap');
	require('./components/Example');

## 3. resources/views/app.blade.php

    <!DOCTYPE html>
    <html lang="{{ str_replace('_', '-', app()->getLocale()) }}">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Laravel</title>
        <!-- Styles -->
        <link href="{{ asset('css/app.css') }}" rel="stylesheet">
    </head>
    <body>

        <!-- React root DOM -->
        <div id="example">
        </div>

        <!-- React JS -->
        <script src="{{ asset('js/app.js') }}" defer></script>
    </body>
    </html>

## 4. routes/web.php


    Route::get('/', function () {
        return view('app');
    });


![](https://avatars.githubusercontent.com/u/75734516?s=48&v=4) 
:+1:
