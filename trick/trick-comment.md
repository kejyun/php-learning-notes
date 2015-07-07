# 註解

## 搜尋關鍵字﹝Gotcha Keywords﹞

* TODO: 主題

表示這裡還有工作尚待完成，不要忘記了。

* BUG: [bugid] 主題

表示這裡有一個已知的臭蟲，並加以解釋，或許再給一個臭蟲編號。

* KLUDGE:

當您很笨拙的完成某件事情時，就明白的說出來，並說明您下次想採取 怎樣不同的方法去做，如果您還有時間的話。

* TRICKY:

告訴別人以下的程式碼是非常有技巧的，請不要不加思索的修改它。

* WARNING:

要注意某件事情。

* PARSER:

偶爾您必須設法解決程式語言剖析器所產生的問題。請加以註明。這個剖析器的問題終會被修正。

* ATTRIBUTE: value

這是個一般格式，說明該註解所內含的屬性。您可以創造您自己的屬性，它們也會被析取出來。

將搜尋關鍵字放在註解的最前面，亦即第一個符號。
註解也許會包含好幾行，然而第一行必須是獨立而有意義的簡要說明。
作者的名字與註解的日期也應該寫在註解裡面。
這兩項資訊雖然也可以在原始碼的倉儲裝置中找到，但是這或許需要一段時間才能查明這段註解到底是誰、在什麼時後所加上去的。
通常這會浪費許多時間去搜尋。 將日期資訊寫在註解裡面，可以讓其他程式設計師在做決定時有所依據。
將作者資訊寫在註解裡面，可以讓我們知道應該找誰問問題。

| 關鍵字   |      說明      |
|----------|:-------------:|
| @access |  變數可存取的權限 (Example: Public or Private) |
| @api |    爲第三方來源的變數   |
| @author | 函數建立者名稱 (Example: @author Barry <riceooks[at]gmail.com>) |
| @category |    函數的分類別名，可能某些工具會利用這個來分類你的方法，使好幾個方法歸為某一類，方便做辨識使用   |
| @copyright |    函數的版權宣告 (Example: @copyright 隨手寫有限公司 www.barryblogs.com)   |
| @deprecated |    代表不建議使用的函數，未來可能會移除這個方法使用到的某個變數，或整個方法都被刪除   |
| @example |    代表這個函數使用方式可以參考某個資料，可以使用檔案位置或網址 (Example: @example http://www.barryblogs.com/ )   |
| @filesource |    這個函數所需的來源   |
| @global |    函數內有使用的全域變數註解 (Example: @global Number $user_id)   |
| @ignore |    代表這個函數或區域可以被忽略，通常會加上說明   |
| @internal |    代表這個函數或區域可能只給予內部使用   |
| @license |    此函數可能是含有某個版權或許可 (Example: @license http://opensource.org/licenses/gpl-license.php GNU Public License)   |
| @link |    可能與某個網站有關係 (Example: @link http://www.barryblogs.com/)   |
| @method |    函數有使用的方法 (Example: @method Array @this->getCategories() or @method String getUserName())   |
| @package |    利用這個註解來達到細部分層結構 (Example: @package PSR\Documentation\API or @package PSR\Documentation\Doc)   |
| @param |    函數要帶入的參數 (Example: @param String&#124;Number $username)   |
| @property |    如果這是一個類別的函數，在類別建構時通常會指定初始化參數，而這個函數可能會使用到某些初始化後的參數，稱之為屬性 (Example: @property Resource&#124;Boolean $mysql_connect)   |
| @return |    函數最後的回傳值或形態 (Example: @return Array&#124;Object&#124;Boolean)   |
| @see |    函數參照或關聯的方法 (Example: @see Class User or @see <a href="http://www.barryblogs.com/">BarryBlogs</a>)   |
| @since |    函數內某個使用的變數由哪個版本變動 (Example: @since v1.3376a $user_nickname )   |
| @source |    這個比較特別，在函數中可以標示從 m 至 n 行 是做什麼事情 (Example: @source 14 21 Get user data)   |
| @static |    靜態變數的註解 (Example: @static String $lang = 'zh_TW')   |
| @subpackage |    利用這個註解來達到細部分層子結構，通常會同時使用 @package，可以參考上面的@package (Example: @package PSR,  @subpackage Documentation\API)   |
| @throws |    例外處理的註解，有多種例外處理的方式，每種方式都不同 (Example: @throws InvalidArgumentException if the provided argument is not of type 'array', @throws Exception other...)   |
| @todo |    計劃要進行的項目描述，一般應該會使用文字描述   |
| @uses |    代表某個元素可能與其它結構有利用關係 (Example: @uses MyClass::$items to retrieve the count from)   |
| @var |    變數(物件成員變數)的形態或描述 (Example: @var Boolean)   |
| @version |    函數的版本 (Example: v1.3258c)   |


## 範例

```php
<?php
    /**
     *      函數名稱
     *      函數描述(有些會含HTML代碼)
     *
     *      @access                 變數可存取的權限 (Example: Public or Private)
     *      @api                    爲第三方來源的變數
     *      @author                 函數建立者名稱 (Example: @author Barry <riceooks[at]gmail.com>)
     *      @category               函數的分類別名，可能某些工具會利用這個來分類你的方法，使好幾個方法歸為某一類，方便做辨識使用
     *      @copyright              函數的版權宣告 (Example: @copyright 隨手寫有限公司 www.barryblogs.com)
     *      @deprecated             代表不建議使用的函數，未來可能會移除這個方法使用到的某個變數，或整個方法都被刪除
     *      @example                代表這個函數使用方式可以參考某個資料，可以使用檔案位置或網址 (Example: @example http://www.barryblogs.com/)
     *      @filesource             這個函數所需的來源
     *      @global                 函數內有使用的全域變數註解 (Example: @global Number $user_id)
     *      @ignore                 代表這個函數或區域可以被忽略，通常會加上說明
     *      @internal               代表這個函數或區域可能只給予內部使用
     *      @license                此函數可能是含有某個版權或許可 (Example: @license http://opensource.org/licenses/gpl-license.php GNU Public License)
     *      @link                   可能與某個網站有關係 (Example: @link http://www.barryblogs.com/)
     *      @method                 函數有使用的方法 (Example: @method Array @this->getCategories() or @method String getUserName())
     *      @package                利用這個註解來達到細部分層結構 (Example: @package PSR\Documentation\API or @package PSR\Documentation\Doc)
     *      @param                  函數要帶入的參數 (Example: @param String|Number $username)
     *      @property               如果這是一個類別的函數，在類別建構時通常會指定初始化參數，而這個函數可能會使用到某些初始化後的參數，稱之為屬性 (Example: @property Resource|Boolean $mysql_connect)
     *      @return                 函數最後的回傳值或形態 (Example: @return Array|Object|Boolean)
     *      @see                    函數參照或關聯的方法 (Example: @see Class User or @see <a href="http://www.barryblogs.com/">BarryBlogs</a>)
     *      @since                  函數內某個使用的變數由哪個版本變動 (Example: @since v1.3376a $user_nickname )
     *      @source                 這個比較特別，在函數中可以標示從 m 至 n 行 是做什麼事情 (Example: @source 14 21 Get user data)
     *      @static                 靜態變數的註解 (Example: @static String $lang = 'zh_TW')
     *      @subpackage             利用這個註解來達到細部分層子結構，通常會同時使用 @package，可以參考上面的@package (Example: @package PSR,  @subpackage Documentation\API)
     *      @throws                 例外處理的註解，有多種例外處理的方式，每種方式都不同 (Example: @throws InvalidArgumentException if the provided argument is not of type 'array', @throws Exception other...)
     *      @todo                   計劃要進行的項目描述，一般應該會使用文字描述
     *      @uses                   代表某個元素可能與其它結構有利用關係 (Example: @uses MyClass::$items to retrieve the count from)
     *      @var                    變數(物件成員變數)的形態或描述 (Example: @var Boolean)
     *      @version                函數的版本 (Example: v1.3258c)
     */
    class ClassName extends AnotherClass
    {
    }
?>
```
