# Laravel Instagram API 

Laravel 5.4 integration for the [Instagram private API](https://github.com/mgp25/Instagram-API/) package.


#Install

`composer require nakukryskin/laravel-instagram-api`

#Usage

Add provider into your `app.php` config:

```
'providers' => [
    ...
    
    Nakukryskin\InstagramApi\LaravelInstagramApiProvider::class,
    
]

```

Add alias into your `app.php` config:
```
'alias' => [
    ...
    
    'Instagram'    => Nakukryskin\InstagramApi\Facades\InstagramApi::class,
    
]

```

#Configuration

```shell
php artisan vendor:publish --provider="Nakukryskin\InstagramApi\LaravelInstagramApiProvider" --tag=config
```

Edit `config/instagram-api.php`.

#Calling

Methods same [Instagram Private API](https://github.com/mgp25/Instagram-API/) package.

Use 
```\Instagram::setUser($username, $password)``` 

instead 

```
$instagram = new Instagram($debug);
$instagram->setUser($username, $password);
```
