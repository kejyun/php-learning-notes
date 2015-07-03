# 類別（Class）

## 類別可以做的事

* 可以宣告屬性(attribute)成員
* 可以擁有常數(const)成員
* 可以實例化(instance)
* 可以實作方法內容(從虛擬類別、介面繼承或定義的虛擬方法,都必需實作)
* 子類別只可以繼承一個父類別

#### 可以宣告屬性(attribute)成員

```php
/**
 * 女生類別
 */
class Girl
{
    // 可以宣告屬性(attribute)成員

    // 女生類別個人的屬性
    public $height;     // 身高是公開的
    protected $weight;  // 體重是保護的
    private $age;       // 年齡是秘密

    // 女生類別共有的靜態屬性
    public static $INTEREST;        // 興趣是公開的
    protected static $APPEARANCE;   // 外表是保護的
    private static $CHARACTER;      // 性格是秘密的
}
```

#### 可以擁有常數(const)成員

```php
/**
 * 女生類別
 */
class Girl
{
    // 可以擁有常數(const)成員
    const IS_AGE_PUBLIC = false;    // 年齡是絕不對外公開的
}
```

#### 可以實例化(instance)

```php
// 可以實例化(instance)
$taiwan_girl = new Girl();
```

#### 可以實作方法內容(從虛擬類別、介面繼承或定義的虛擬方法,都必需實作)

```php
/**
 * 女生類別
 */
class Girl
{
    // 可以實作方法內容(從虛擬類別、介面繼承或定義的虛擬方法,都必需實作)
    /**
     * 化妝
     */
    public function makeUp()
    {
        // 做一些化妝的動作
    }

    /**
     * 八卦
     */
    public function gossip()
    {
        // 聊聊聊～
    }

    /**
     * 逛街
     */
    public function shopping()
    {
        // 買買買～
    }
}
```

#### 子類別只可以繼承一個父類別

***父類別***

```php
/**
 * 人（父類別）
 */
class Person
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

***子類別繼承父類別***

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

## 類別不可以做的事

* 不可以有抽象方法(abstract method)

#### 不可以有抽象方法(abstract method)

```php
/**
 * 女生類別
 */
class Girl
{
    // 不可以有抽象方法(abstract method)
    /**
     * 旅遊抽象方法（無法實作）
     * ✘✘✘✘✘✘✘ ◢▆▅▄▃-崩╰(〒皿〒)╯潰-▃▄▅▆◣ ✘✘✘✘✘✘✘
     */
    abstract public function travel();
}
```
