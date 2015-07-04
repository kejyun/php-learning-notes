# 抽象類別（Abstract Class）

## 抽象類別可以做的事

* 可以宣告屬性(attribute)成員
* 可以擁有常數(const)成員
* 可以實作方法內容
* 子類別只可以繼承一個抽象類別

#### 可以宣告屬性(attribute)成員

```php
/**
 * 人（抽象類別）
 */
abstract class Person
{
  // 人抽象類別的個人屬性
  public $height;     // 身高是公開的
  protected $weight;  // 體重是保護的
  private $age;       // 年齡是秘密

  // 人抽象類別共有的靜態屬性
  public static $INTEREST;        // 興趣是公開的
  protected static $APPEARANCE;   // 外表是保護的
  private static $CHARACTER;      // 性格是秘密的
}
```

#### 可以擁有常數(const)成員

```php
/**
 * 人（抽象類別）
 */
abstract class Person
{
    // 可以擁有常數(const)成員
    const IS_AGE_PUBLIC = false;    // 年齡是絕不對外公開的
}
```

#### 可以實作方法內容

```php
/**
 * 人（抽象類別）
 */
abstract class Person
{
    // 可以實作方法內容

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

#### 子類別只可以繼承一個抽象類別

***抽象類別***

```php
/**
 * 人（父類別）
 */
abstract class Person
{
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

***子類別繼承抽象類別***

```php
/**
 * 女生類別
 */
class Girl extends Person
{
}
// 台灣女孩
$taiwan_girl = new Girl();

// 台灣女孩「吃吃吃～」
$taiwan_girl->eat();

// 台灣女孩「睡睡睡～」
$taiwan_girl->sleep();
```


## 抽象類別不可以做的事

* 不可實作抽象方法
* 不可以實例化(instance)


#### 不可實作抽象方法

```php
/**
 * 人（父類別）
 */
abstract class Person
{
  // 不可實作抽象方法

  /**
   * 吃飯抽象方法（無法實作）
   * ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘
   */
  abstract public function eat()
  {
      // 吃吃吃～
  }

  /**
   * 睡覺抽象方法（無法實作）
   * ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘
   */
  abstract public function sleep()
  {
      // 睡睡睡～
  }
}
```

#### 不可以實例化(instance)

```php
/**
 * 人（父類別）
 */
abstract class Person
{
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

// 不可以實例化(instance)
// ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘
$taiwan_person = new Person();
```

## 抽象類別（Abstract Class）使用時機

當「多個類別（Class）」之間有共同的方法（function）或屬性（attribute）時，可以將這些共用的地方寫成「抽象類別（Abstract Class）」，讓其他的「子類別（Class）」去繼承
