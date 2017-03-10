# MultipleFlavor

###目前現況
切割三個 productFlavors 出來如下：
```gradle
productFlavors {
    prod {

    }
    dev {

    }
    mock {

    }
}
```  
測試的 class  
1. dev [FlavorObject](https://github.com/TADSG/MultipleFlavor/blob/master/app/src/dev/java/tw/andyang/multipleflavor/FlavorObject.java)
2. prod [FlavorObject](https://github.com/TADSG/MultipleFlavor/blob/master/app/src/prod/java/tw/andyang/multipleflavor/FlavorObject.java)
3. mock [FlavorObject](https://github.com/TADSG/MultipleFlavor/blob/master/app/src/mock/java/tw/andyang/multipleflavor/FlavorObject.java)

目前的 productFlavors 使用上當 class 有相異時需要將 class 檔案放置到各個 productFlavors 中，若無相異則放置到 main 中

###問題  
當今天只有一個 productFlavors 檔案要不同時，另外兩個 productFlavors 必須放置一份相同的檔案這會這會增加維護的複雜度
e.g 忘了複製一份

###需求  
相同檔案的 productFlavors 可以不要複製兩份共用一份檔案
