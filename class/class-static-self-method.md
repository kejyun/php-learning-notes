# static 與 self 區別


## 使用 static

```php
<?php

class Car
{
  public static function model(){
    static::getModel();
  }

  protected static function getModel(){
    echo "This is a car model";
  }
}

Class Taxi extends Car
{
  protected static function getModel(){
    echo "This is a Taxi model";
  }
}
```

執行 model 靜態函式

```
Car::model();
Taxi::model();
```

執行結果

```
This is a car model
This is a Taxi model
```

## 使用 self

```php
<?php

class Car
{
  public static function model(){
    self::getModel();
  }

  protected static function getModel(){
    echo "This is a car model";
  }
}

Class Taxi extends Car
{
  protected static function getModel(){
    echo "This is a Taxi model";
  }
}
```

執行 model 靜態函式

```
Car::model();
Taxi::model();
```

執行結果

```
This is a car model
This is a car model
```

## 結論

self 只會呼叫自己的 function，即便有繼承的狀況

static 則是如果有繼承時，會呼叫繼承的 function


## 參考資料
* [php面向对象中self和static的区别 - ThinkingPool - SegmentFault 思否](https://segmentfault.com/a/1190000005060322)
