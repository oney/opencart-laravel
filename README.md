opencart-laravel
=================

Embed Laravel illuminate framework to Opencart

### Introduction 
I love using Opencart, but lack of ActiveRecord(ORM), Validator and Service causes me pain and make codes in disorder. I also program RoR and Laravel, so transplanting [Laravel illuminate](https://github.com/laravel/framework) to Opencart seems a good idea.
Thanks [majid8911](http://stackoverflow.com/users/1695427/majid8911) give me [this repo](https://github.com/mattstauffer/IlluminateNonLaravel). It helped me a lot to complete this transplantation.

### Installation
Download files and copy/upload to your Opencart root directory. It won't override any file. And open [http://localhost:8888/index.php?route=account/test](http://localhost:8888/index.php?route=account/test), this controller completely implements ControllerAccountRegister class.  Please checkout `catalog/controller/account/test.php` file to see how it works.

### Need help
I only add some models and validators to demonstrate how to use eloquent model and validator in Opencart. Please help me supply others, you can raise a pull request to do it.

### Development
In any controller you want to use illuminate framework, you need to add require load.php file and use class name like that

```
<?php
require_once(DIR_SYSTEM.'laravel/load.php');

use App\Service\RegisterService;

class ControllerAccountTest extends Controller
{
```

You can add `require_once(DIR_SYSTEM.'laravel/load.php');` to the bottom of `system/startup.php` file. It will autoload at every controllers.

You can take a look at `system/laravel` directory, all things in there.

Please collect me if codes have any mistake
