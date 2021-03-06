# Laravel 5.x Scaffold Generator
## Usage

### Step 1: Add repo in composer.json

```
"repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/gomezdanielg/l5scaffold"
        }
    ],
```

### Step 2: Install Through Composer

```
composer require 'gomezdanielg/l5scaffold' --dev
```

### Step 3: Add the Service Provider

Open `config/app.php` and, to your **providers** array at the bottom, add:

```
Laralib\L5scaffold\GeneratorsServiceProvider::class
```

### Step 4: Run Artisan!

You're all set. Run `php artisan` from the console, and you'll see the new commands `make:scaffold`.

## Examples

Use this command to generator scaffolding of **Tweet** in your project:
```
php artisan make:scaffold Tweet \
	--schema="title:string:default('Tweet #1'), body:text"
```
or with more options
```
php artisan make:scaffold Tweet \
	--schema="title:string:default('Tweet #1'), body:text" \
	--ui="bs3" \
	--prefix="admin"
```

This command will generate:

```
app/Tweet.php
app/Http/Controllers/TweetController.php

database/migrations/201x_xx_xx_xxxxxx_create_tweets_table.php
database/seeds/TweetTableSeeder.php

resources/views/layout.blade.php
resources/views/tweets/index.blade.php
resources/views/tweets/show.blade.php
resources/views/tweets/edit.blade.php
resources/views/tweets/create.blade.php
```

After don't forget to run:


```
php artisan migrate
```
## Custom stub
Create a new folder inside **Stubs > views** with your UI name custom 
![image](http://i66.tinypic.com/10ndpgw.png)

Custom fields in `Stubs > views > **ui-name** > fields`

Custom pages in `Stubs > views > **ui-name** > pages`

<br>

:thought_balloon: **Send us your ideas.** (creating issues)


##Collaborators
 [Fernando Brito](https://github.com/fernandobritofl "fernandobritofl")
 <br/>[Sylvio Tavares](https://github.com/sylviot "Sylviot")
 <br/>[Raphael Heitor](https://github.com/raphaelheitor "raphaelheitor")
 <br/>[Alfred Nutile](https://github.com/alnutile "alnutile")
 <br/>[Sazzad Hossain Khan](https://github.com/itsazzad "itsazzad")
 <br/>[Alexander Makhaev](https://github.com/mankms "mankms")
 <br/>[Adam Brown](https://github.com/DeftNerd "DeftNerd")
 <br/>[TJ Webb](https://github.com/webbtj "webbtj")
 <br/>[Tsaganos Tolis](https://github.com/Dev-Force "Dev-Force")
 <br/>[Ryan Gurnick](https://github.com/ryangurn "ryangurn")
