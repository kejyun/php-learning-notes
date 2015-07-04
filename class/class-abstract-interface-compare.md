# 類別（Class）、抽象類別（Abstract Class）與介面（Interface）比較


|   | 類別（Class）| 抽象類別（Abstract Class）| 介面（Interface）|
|---|---|---|---|
|宣告屬性（attribute）| ✓ | ✓ | ✖ |
|常數（const）| ✓ | ✓ | ✓ |
|實例化（new class）| ✓ | ✖ | ✖ |
|抽象方法（abstract function）| ✖ | ✓ | ✓ |
|實作方法內容（functoin()）| ✓ | ✓ | ✖ |
|類別是否可繼承多個| ✖ | ✖ | ✓ |


## 抽象類別（Abstract Class）使用時機

當「多個類別（Class）」之間有共同的方法（function）或屬性（attribute）時，可以將這些共用的地方寫成「抽象類別（Abstract Class）」，讓其他的「子類別（Class）」去繼承


## 介面（Interface）使用時機

當「多個類別（Class）」之間有共同的方法（function），但方法實做的方式有差異，可以將這些共用「方法」寫成「介面（Interface）」，讓其他的「子類別（Class）」去實做這個介面
