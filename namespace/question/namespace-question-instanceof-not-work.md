# instanceof 無法運作

在我使用 instanceof 去判斷是否為閉包函式（Closure）時，判斷出來的結果都為 false

```php
<?php namespace App\Repositories;

class Container
{
    protected $binds;

    protected $instances;

    public function bind($abstract, $concrete)
    {
        // instanceof 判斷結果皆為 false
        if ($concrete instanceof Closure) {
            $this->binds[$abstract] = $concrete;
        } else {
            $this->instances[$abstract] = $concrete;
        }
    }
}
```


因為我有使用命名空間去建立類別，所以要解決這樣的問題有兩個方法

1. 在類別最上方使用 `use \Closure;` 正確地去引入閉包類別
2. 使用 `instanceof \Closure` 去判斷類別

```php
<?php
// 方法 1
use \Closure;

// 方法 2
if ($concrete instanceof \Closure) {
    $this->binds[$abstract] = $concrete;
}
```

當你使用命名空間去建立你的類別，且要使用其他命名空間的類別時，都要確保在最上面有使用 use 去引入你要用的類別命名空間，或者指定該類別正確的命名空間。

## 參考資料
* [instanceof Closure returns false](http://stackoverflow.com/questions/17305002/instanceof-closure-returns-false)
