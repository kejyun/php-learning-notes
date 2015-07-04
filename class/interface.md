# 介面（Interface）

## 介面可以做的事

* 可以擁有常數(const)成員
* 可以有抽象方法(Interface所有方法都是抽象的,只是 不用宣告abstract關鍵字)
* 類別可以定義多個介面
* 介面可以衍生自另一個介面

#### 可以擁有常數(const)成員

```php
/**
 * 人（介面）
 */
interface Person
{
    // 可以擁有常數(const)成員
    const IS_AGE_PUBLIC = false;    // 年齡是絕不對外公開的
}
```

#### 可以有抽象方法(Interface所有方法都是抽象的,只是 不用宣告abstract關鍵字)

```php
/**
 * 人（介面）
 */
interface Person
{
  /**
   * 吃飯抽象方法
   */
  public function eat();

  /**
   * 睡覺抽象方法
   */
  public function sleep();
}
```

#### 類別可以定義多個介面

***人類（介面）***

```php
/**
 * 人類（介面）
 */
interface Human
{
  /**
   * 「笑」抽象方法
   */
  public function laugh();
}
```
***人（介面）***
```php
/**
 * 人（介面）
 */
interface Person
{
  /**
   * 「吃飯」抽象方法
   */
  public function eat();

  /**
   * 「睡覺」抽象方法
   */
  public function sleep();
}
```

***類別實作多個介面***


```php
/**
 * 女生類別
 */
class Girl implements Person, Human
{
  /**
   * 笑
   */
  public function laugh()
  {
      // 笑笑笑～
  }

  /**
   * 吃飯
   */
  public function eat()
  {
      // 吃吃吃～
  }

  /**
   * 睡覺
   */
  public function sleep()
  {
      // 睡睡睡～
  }
}
```

#### 介面可以衍生自另一個介面

***人類（介面）***

```php
/**
 * 人類（介面）
 */
interface Human
{
  /**
   * 「笑」抽象方法
   */
  public function laugh();
}
```

***人（介面）延伸人類（介面）***

```php
/**
 * 人（介面）延伸人類（介面）
 */
interface Person extends Human
{
  /**
   * 「吃飯」抽象方法
   */
  public function eat();

  /**
   * 「睡覺」抽象方法
   */
  public function sleep();
}
```

## 介面不可以做的事

* 不可以宣告屬性(attribute)成員
* 不可以實例化(instance)
* 不可以實作方法內容



#### 不可以宣告屬性(attribute)成員

```php
/**
 * 人（介面）
 */
interface Person
{
  // 不可以宣告屬性(attribute)成員
  // ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘

  // 人介面的個人屬性
  public $height;     // 身高是公開的
  protected $weight;  // 體重是保護的
  private $age;       // 年齡是秘密

  // 人介面共有的靜態屬性
  public static $INTEREST;        // 興趣是公開的
  protected static $APPEARANCE;   // 外表是保護的
  private static $CHARACTER;      // 性格是秘密的
}
```


#### 不可以實例化(instance)

```php
/**
 * 人（介面）
 */
interface Person
{
  /**
   * 「吃飯」抽象方法
   */
  public function eat();

  /**
   * 「睡覺」抽象方法
   */
  public function sleep();
}

// 不可以實例化(instance)
// ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘
$taiwan_person = new Person();
```

#### 不可以實作方法內容

```php
/**
 * 人（介面）
 */
interface Person
{
  // 不可以實作方法內容
  // ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘

  /**
   * 吃飯
   */
  public function eat()
  {
      // 吃吃吃～
  }

  /**
   * 睡覺
   */
  public function sleep()
  {
      // 睡睡睡～
  }
}
```

## 介面（Interface）使用時機

當「多個類別（Class）」之間有共同的方法（function），但方法實做的方式有差異，可以將這些共用「方法」寫成「介面（Interface）」，讓其他的「子類別（Class）」去實做這個介面


## 參考資料
* [PHP: Object Interfaces - Manual](http://php.net/manual/en/language.oop5.interfaces.php)
