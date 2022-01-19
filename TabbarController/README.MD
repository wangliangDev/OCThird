
## [](https://github.com/ChenYilong/CYLTabBarController)

It is an iOS UI module library for adding animation to iOS tabbar items and icons with Lottie, and adding a bigger center UITabBar Item. [CN]【中国特色 TabBar】一行代码实现 Lottie 动画TabBar，支持中间带+号的TabBar样式，自带红点角标，支持动态刷新。【iOS13 & Dark Mode & iPhone XS MAX supported】

[CN]特点 </p>[EN]Features |[CN]解释 </p>[EN]Explanation
:-------------:|:-------------:
[CN]一行代码支持Lottie动画TabBar样式 </p> [EN] It only needs one line of code to have an animated TabBar with Lottie. |[CN][使用方法]( https://github.com/ChenYilong/CYLTabBarController/issues/341) </p>  [EN][How to add animation of Lottie with one line of code.]( https://github.com/ChenYilong/CYLTabBarController/issues/341)  </p> ![https://github.com/ChenYilong](https://tva1.sinaimg.cn/large/006y8mN6ly1g6upmqhqjrg30o209r4qp.gif) </p>  ![https://github.com/ChenYilong](https://tva1.sinaimg.cn/large/006y8mN6ly1g6uqohfiw2g30cd03hdop.gif)
[CN]低耦合，易删除</p>[EN]Loose coupling  | [CN]1、TabBar设置与业务完全分离，最低只需传两个数组即可完成主流App框架搭建。</p>[EN]1. This library is independent of your business codes which only needs two array parameters to be passed.   </p> [CN]2、 PlusButton 的所有设置都在单独的一个类（ `CYLPlusButton` 的子类）中实现：删除该特定的类，就能完全将 PlusButton 从项目中删除掉。</p>[EN]2.PlusButton is also independent. If you delete the code of this class, you remove the PlusButton feature from your UI on screen completely.  
[CN]`TabBar` 以及 `TabBar` 内的 `TabBarItem` 均使用系统原生的控件</p>[EN]`TabBar` and `TabBarItem` those parts of this library both are system objects. | [CN]因为使用原生的控件，并非 `UIButton` 或 `UIView` 。好处如下：</p>[EN]Advantages of quitting choosing `UIButton` or `UIView`: </p> 1. 无需反复调“间距位置等”来接近系统效果。</p>[EN]There is not need to adjust those object to make them close to a system  object appearance. </p> 2. 在push到下一页时 `TabBar`  的隐藏和显示之间的过渡效果跟系统一致（详见“ [集成后的效果](https://github.com/ChenYilong/CYLTabBarController#集成后的效果) ”部分，给出了效果图）</p>[EN]2. A push animation is same to a system objects appearance. </p> 3. 原生控件，所以可以使用诸多系统API，比如：可以使用 ` [UITabBar appearance];` 、` [UITabBarItem appearance];` 设置样式。（详见“[补充说明](https://github.com/ChenYilong/CYLTabBarController#补充说明) ”部分，给出了响应代码示例）</p>[EN]3.It is convenient to use the system API such as ` [UITabBar appearance];`,` [UITabBarItem appearance];`, etc.
 自动监测是否需要添加“加号”按钮，</p>并能自动设置位置</p>[EN] It is able to check if need to add a PlusButton automatically. |[CYLTabBarController](https://github.com/ChenYilong/CYLTabBarController) 既支持类似微信的“中规中矩”的 `TabBarController` 样式，并且默认就是微信这种样式，同时又支持类似“微博”或“淘宝闲鱼”这种具有不规则加号按钮的 `TabBarController` 。想支持这种样式，只需自定义一个加号按钮，[CYLTabBarController](https://github.com/ChenYilong/CYLTabBarController) 能检测到它的存在并自动将 `tabBar` 排序好，无需多余操作，并且也预留了一定接口来满足自定义需求。</p>“加号”按钮的样式、frame均在自定义的类中独立实现，不会涉及tabbar相关设置。
  支持动态更新 | 可动态删除PlusButton ，可以动态更新样式 </p> ![https://github.com/ChenYilong](https://tva1.sinaimg.cn/large/006y8mN6ly1g6uq38ulz8g30al02w0u1.gif)
即使加号按钮超出了tabbar的区域，</p>超出部分依然能响应点击事件 | 红线内的区域均能响应tabbar相关的点击事件，</p>![https://github.com/ChenYilong](https://tva1.sinaimg.cn/large/006y8mN6ly1g6uqi6prqsj30j60g8js7.jpg)
允许指定加号按钮位置 | 效果如下：</p>![iTeaTime(技术清谈)](https://tva1.sinaimg.cn/large/006y8mN6gy1g92nics1hvj30a906u3ym.jpg) </p>Airbnb-app效果：</p>![iTeaTime(技术清谈)](https://tva1.sinaimg.cn/large/006y8mN6gy1g92nir57tmg308w0fsapi.gif)
支持让 `TabBarItem` 仅显示图标，并自动使图标垂直居中，支持自定义TabBar高度 | 效果可见Airbnb-app效果，或者下图</p>![enter image description here](https://cloud.githubusercontent.com/assets/7238866/10777333/5d7811c8-7d55-11e5-88be-8cb11bbeaf90.png)
 支持角标自定义View | ![enter image description here](https://ws4.sinaimg.cn/large/006tKfTcly1fgl0yxcaboj30yi06at8t.jpg) 
 支持多TabBar嵌套，并指定PlusButton位置 | ![enter image description here](https://ws4.sinaimg.cn/large/006tNc79ly1fmn3005isfg308r0iltl6.gif)
支持CocoaPods |容易集成
支持Swift项目导入 | 兼容
支持横竖屏 | －－
