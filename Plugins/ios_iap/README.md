IOS_IAP插件
---------------
#### 1.支持平台：ios
#### 2.代码示列
```C++
// 会发送IAP_MSG通知
CCNotificationCenter::sharedNotificationCenter()->addObserver(this, callfuncO_selector(HelloWorld::onIAPCallback), "IAP_MSG", NULL);

C2dPlugins::C2dPlugin plugin = new C2dPlugins::C2dPugin();
plugin->szPluginName = "C2dPluginIAP";
plugin->invole("init");
plugin->invoke("buy","com.itspas.point2048");
    
```
#### 3.API
```C++
// 初始化IAP
const char* init(void);
// 购买物品
const char* buy(const char* product);
```