## laravel-binance
Laravel implementation of the Binance crypto exchange trading API

#### Install

```
composer require sabramooz/laravel-binance
```

Utilises autoloading in Laravel 5.5+. For older versions add the following lines to your `config/app.php`

```php
'providers' => [
        ...
        sabramooz\binance\BinanceServiceProvider::class,
        ...
    ],

 'aliases' => [
        ...
        'Binance' => sabramooz\binance\BinanceAPIFacade::class,
    ],
```

#### Usage

```php
    $binance = new \sabramooz\binance\BinanceAPI();
    dump($binance->getAvgPrice("BTCUSDT"));
    dump($binance->getAvgPrice("ETHUSDT"));
```
##### Result

```json
    array:2 [▼
      "mins" => 5
      "price" => "37009.43501853"
    ]
    array:2 [▼
      "mins" => 5
      "price" => "1407.75224237"
    ]
```

#### Binance API Doc
[https://binance-docs.github.io/apidocs/spot/en/#market-data-endpoints](https://binance-docs.github.io/apidocs/spot/en/#market-data-endpoints)
