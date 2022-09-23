# WMZPageController - 分页控制器,替换UIPageController方案,具备完整的生命周期（可传入子控制器/子视图）,多种指示器样式,多种标题样式,可悬浮,功能齐全,支持底部多级联动,支持嵌套多个菜单多页面

 [![Platform](https://img.shields.io/badge/platform-iOS-red.svg)](https://developer.apple.com/iphone/index.action) 
 [![CocoaPods Compatible](https://img.shields.io/cocoapods/v/WMZPageController.svg)](https://img.shields.io/cocoapods/v/WMZPageController.svg)
 [![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://mit-license.org) 

# ⚠️⚠️  使用悬浮样式如果子视图有滚动视图需要实现协议 WMZPageProtocol  如果没有则不需要实现
# ⚠️⚠️  1.5.0版本后改动比较大,如需稳定请指定1.4.6
# ⚠️⚠️   
     //自定义整体距离顶部的位置(如果默认算的不准确 或者需要修改) block内会传回当前的值 可对比自行返回最终需要的
      WMZPagePropStatementAndPropSetFuncStatement(copy, WMZPageParam, PageCustomFrameY,        wCustomNaviBarY)
     //自定义整体距离底部的位置(如果默认算的不准确 或者需要修改) block内会传回当前的值 可对比自行返回最终需要的
     WMZPagePropStatementAndPropSetFuncStatement(copy, WMZPageParam, PageCustomFrameY,        wCustomTabbarY)
     //自定义底部滚动视图的高度(如果默认算的不准确 或者需要修改)可作为改变悬浮菜单栏的位置 block内会传回当前的值 可对比自行返回最终需要的
     WMZPagePropStatementAndPropSetFuncStatement(copy, WMZPageParam, PageCustomFrameY,        wCustomDataViewHeight)

演示
==============
### 动画样式 
| 动画样式                | 作用   (默认值)                                 |
|-----------------------|-----------------------------------------------------|
| AQY样式               | ![AQY.gif](https://upload-images.jianshu.io/upload_images/9163368-2aeb8a149df8c985.gif?imageMogr2/auto-orient/strip)|
| PDD样式               | ![PDD.gif](https://upload-images.jianshu.io/upload_images/9163368-529d34c16e7711f2.gif?imageMogr2/auto-orient/strip)|
| TT样式              | ![Toutiao.gif](https://upload-images.jianshu.io/upload_images/9163368-07204254c59bb15c.gif?imageMogr2/auto-orient/strip)|
| JD样式              | ![Jingdong.gif](https://upload-images.jianshu.io/upload_images/9163368-cc1f472eabfe9fcf.gif?imageMogr2/auto-orient/strip)|
| QQ样式              | ![QQ.gif](https://upload-images.jianshu.io/upload_images/9163368-f700c66170ba6f16.gif?imageMogr2/auto-orient/strip)|
| 圆角框             | ![圆角框 .gif](https://upload-images.jianshu.io/upload_images/9163368-1f533b85c219800b.gif?imageMogr2/auto-orient/strip)|

### 标题样式 
| 标题样式                | 作用   (默认值)                                 |
|-----------------------|-----------------------------------------------------|
| 红点               |  ![红点.gif](https://upload-images.jianshu.io/upload_images/9163368-f709ed263ba883d4.gif?imageMogr2/auto-orient/strip)|
| 富文本               |![富文本.gif](https://upload-images.jianshu.io/upload_images/9163368-302e498ed3929558.gif?imageMogr2/auto-orient/strip) |
| 固定宽度             |![固定宽度.gif](https://upload-images.jianshu.io/upload_images/9163368-7d730925c56b7200.gif?imageMogr2/auto-orient/strip)  |
| 图文              |![带图片.gif](https://upload-images.jianshu.io/upload_images/9163368-383d923b19d3e1c4.gif?imageMogr2/auto-orient/strip) |
|固定右边              |![](https://upload-images.jianshu.io/upload_images/9163368-7daf3d6d8092d256.gif?imageMogr2/auto-orient/strip)|
|自定义标题样式              |![自定义标题样式.gif](https://upload-images.jianshu.io/upload_images/9163368-246160d93223dfe4.gif?imageMogr2/auto-orient/strip)|
|自定义导航栏              |![自定义导航栏.gif](https://upload-images.jianshu.io/upload_images/9163368-668a88c126835a04.gif?imageMogr2/auto-orient/strip)|


### 悬浮样式
| 悬浮样式                | 作用   (默认值)                                 |
|-----------------------|-----------------------------------------------------|
| 悬浮导航栏透明度不变化+刷新在中间              |  ![悬浮导航栏透明度不变化.gif](https://upload-images.jianshu.io/upload_images/9163368-c816c09bfe3919c9.gif?imageMogr2/auto-orient/strip) |
| 悬浮导航栏透明度变化+刷新在顶部               |![悬浮导航栏透明度变化+刷新在顶部.gif](https://upload-images.jianshu.io/upload_images/9163368-13ae25b5672ab495.gif?imageMogr2/auto-orient/strip)|
| 固定底部           |![固定底部.gif](https://upload-images.jianshu.io/upload_images/9163368-fa4865fbe88fd591.gif?imageMogr2/auto-orient/strip)|
| 头部放大          |![头部放大.gif](https://upload-images.jianshu.io/upload_images/9163368-225597fd7c577407.gif?imageMogr2/auto-orient/strip)|
| 自定义复杂嵌套悬浮UI            |![自定义复杂嵌套悬浮UI.gif](https://upload-images.jianshu.io/upload_images/9163368-face20117ca38861.gif?imageMogr2/auto-orient/strip) |

### 嵌套
| 样式                | 作用   (默认值)                                 |
|-----------------------|-----------------------------------------------------|
| wb              | ![wb.gif](https://upload-images.jianshu.io/upload_images/9163368-49338e075eab60f9.gif?imageMogr2/auto-orient/strip) |
| 三层（王者营地）           | ![三层.gif](https://upload-images.jianshu.io/upload_images/9163368-f867d9200d5daf76.gif?imageMogr2/auto-orient/strip)|
| 双重           |![双重 .gif](https://upload-images.jianshu.io/upload_images/9163368-a9e27bc2ca8121c3.gif?imageMogr2/auto-orient/strip)|
| 顶掉父菜单         | ![顶掉父菜单.gif](https://upload-images.jianshu.io/upload_images/9163368-3aa3ac02faa59cb9.gif?imageMogr2/auto-orient/strip)

###特殊使用
| 样式                | 作用   (默认值)                                 |
|-----------------------|-----------------------------------------------------|
| 作为tabbar使用              | ![tabbar.gif](https://upload-images.jianshu.io/upload_images/9163368-c3d9cb4339d6082a.gif?imageMogr2/auto-orient/strip) |
| 淘宝首页效果           | ![taobao.gif](https://upload-images.jianshu.io/upload_images/9163368-ef84ae02f9d8bebf.gif?imageMogr2/auto-orient/strip)|
| 美团外卖商家详情效果(子控制器多级联动)           |![meituan.gif](https://upload-images.jianshu.io/upload_images/9163368-caec9456b1383756.gif?imageMogr2/auto-orient/strip) |
| 菜单标题跟随内容滑动         | ![菜单标题跟随内容滑动.gif](https://upload-images.jianshu.io/upload_images/9163368-92ae59f2e362cbc3.gif?imageMogr2/auto-orient/strip)

特性
==============
- 链式语法 结构优雅
- 支持顶部悬浮
- 支持多种指示器样式
- 支持富文本标题
- 支持图文混合标题
- 支持完整的生命周期
- 替换系统UIPageController的方案,减少内存,避免UIPageController的bug
- 支持传入UIView/UIViewController作为子视图/子控制器
- 菜单栏可以单独使用（详情见Demo）
- 可独立使用WMZPageView,无需继承WMZPageController
- 适配横竖屏

替换UIPageController是用UIScrollView替换,手势滑动从而实现完整生命周期

悬浮（子控制器/子视图实现WMZPageProtocol协议）
==============
    /// 悬浮 两者一样 下面的只是为了减少非tableview的警告
    - (UIScrollView*)getMyScrollView;
    /// 悬浮 数组 可滚动视图的数组 适用底部多个scrollView的情况
    - (NSArray <UIScrollView*>*)getMyScrollViews;
    /// 子控制器需要固定的尾部视图
    - (UIView*)fixFooterView;

生命周期（子控制器/子视图实现WMZPageProtocol协议）
==============
#### 传入的是UIView
    /// 生命周期 和VC的生命周期用法一致
    - (void)pageViewWillAppear;
    - (void)pageViewWillDisappear;
    - (void)pageViewDidAppear;
    - (void)pageViewDidDisappear;

#### 传入的是UIView传入的是UIViewController
    ///系统生命周期方法
    - (void)viewWillAppear:(BOOL)animated
    - (void)viewDidAppear:(BOOL)animated
    - (void)viewWillDisappear:(BOOL)animated
    - (void)viewDidDisappear:(BOOL)animated
    （两者都会触发 只实现一个即可）
    - (void)pageViewWillAppear;
    - (void)pageViewWillDisappear;
    - (void)pageViewDidAppear;
    - (void)pageViewDidDisappear;

用法
==============

### 链式写法 (WMZPageParam内含几十种配置属性)

     WMZPageParam *param =  PageParam()
     .wTitleArrSet(@[@"推荐",@"LOOK直播",@"画",@"现场",@"翻唱",@"MV",@"广场",@"游戏"])
     .wViewController = ^UIViewController * _Nullable(NSInteger index) {
        return NSClassFromString(@"TestVC").new;
     }
     .wNaviAlphaSet(NO)
     .wFromNaviSet(YES)
     .wTopSuspensionSet(YES)

### 常规写法
       WMZPageParam *param = WMZPageParam.new;
       param.wTitleArr =  @[@"推荐",@"LOOK直播",@"画",@"现场",@"翻唱",@"MV",@"广场",@"游戏"]
       param.wViewController = ^UIViewController * _Nullable(NSInteger index) {
            return NSClassFromString(@"TestVC").new;
       };
       param.wTopSuspension = YES;

###  title传入字典对应的属性
        /// 例如
       @[
          @{WMZPageKeyName:@"标题",WMZPageKeySelectName:@"选中标题",WMZPageKeyBadge:@(YES)},
          @{WMZPageKeyName:@"标题",WMZPageKeySelectName:@"选中标题",WMZPageKeyBadge:@(YES)}
          @{WMZPageKeyName:@"标题",WMZPageKeySelectName:@"选中标题",WMZPageKeyBadge:@(YES)}
        ]
        // 红点提示  @(YES) 或者 带数字 @(99) @"99+"  wCustomRedView使用这个属性可以调整角标的位置和样式
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyBadge;
       /// 标题  NSString/NSAttributedString  支持传入富文本
       /// 如果此处传入富文本则WMZPageKeySelectName 也需要传入 此时设置的选中标题title font uicolor会失效
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyName;
       /// 选中后标题 NSString/NSAttributedString  支持传入富文本
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeySelectName;
       /// 指示器颜色 UIColor
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyIndicatorColor;
       /// 字体颜色 UIColor
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleColor;
       /// 选中字体颜色 UIColor
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleSelectColor;
       /// 图片 NSString/UIImage
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyImage;
       /// 选中后图片 NSString/UIImage
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeySelectImage;
       /// 选中背景颜色 [UIColor redColor] (如果是数组则是背景色渐变色) @[[UIColor redColor],[UIColor orangeColor]]
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyBackgroundColor;
       /// 标题背景颜色 UIColor
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleBackground;
       /// 图文距离 @(5)
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyImageOffset;
       /// 仅点击页面不加载 @(YES)
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyOnlyClick;
       /// 自定义标题宽度(优先级最高)   @(100)
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleWidth;
       /// 自定义标题高度(优先级最高)   @(100)
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleHeight;
       /// 自定义标题x间距(优先级最高)  @(100)
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleMarginX;
       /// 自定义标题y坐标(优先级最高)  @(100)
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyTitleMarginY;
       /// 当前子控制器不悬浮固定在顶部  @(NO)  NO表示不悬浮
       FOUNDATION_EXPORT WMZPageBTNKey const WMZPageKeyCanTopSuspension;
   
###  param的配置属性见Demo的WMZPageParam类

###  titleArr传入自定义model数组 
     Model *model = Moded.new
     model.name = @"标题";
     self.param.wTitleArr = @[model,model,model]
     self.param.wCustomTitleContentSet(^NSString * _Nullable(id  _Nullable model, NSInteger index) {
        return model.name;
     })
 
### 依赖
无任何依赖 

安装
==============

### CocoaPods
1. 将 cocoapods 更新至最新版本.
2. 在 Podfile 中添加 `pod 'WMZPageController'`。
3. 执行 `pod install` 或 `pod update`。
4. 导入 #import "WMZPageController.h"。

### 手动安装

1. 下载 WMZPageController 文件夹内的所有内容。
2. 将 WMZPageController 内的源文件添加(拖放)到你的工程。
3. 导入 #import "WMZPageController.h"

系统要求
==============
该库最低支持 `iOS 9.0` 和 `Xcode 9.0`。

许可证
==============
WMZPageControlller 使用 MIT 许可证，详情见 [LICENSE](LICENSE) 文件。


个人主页
==============
使用过程中如果有什么bug欢迎给我提issue 我看到就会解决
[我的简书](https://www.jianshu.com/p/32e997b74d74)

### 常见问题（开始收录）
     1 问：设置了wTopSuspension为什么没有底部没有滑动？
       答：先看看子控制器有没有实现WMZPageProtocol协议返回可滚动的视图,再看看子控制器是否自己实现了didscroll等的滑动代理方法把库内的方法覆盖掉了
     2 问:怎么设置标题的风格,红点等怎么展示
       答:在传值wTitleArr的时候 把标题字符串换成字典
     3 问:距离顶部或者距离底部 没有达到需求,有留白或者空出等情况
       答:可以使用这三个属性进行调整,属性内会返回当前的值,调整的时候只需要根据情况返回适当增加或者减少的值 即可
        //自定义整体距离顶部的位置 适用于整体距离顶部的距离
        WMZPagePropStatementAndPropSetFuncStatement(copy, WMZPageParam, PageCustomFrameY,        wCustomNaviBarY)
        //自定义整体距离底部的位置 适用于整体距离底部的距离
        WMZPagePropStatementAndPropSetFuncStatement(copy, WMZPageParam, PageCustomFrameY,        wCustomTabbarY)
        //自定义底部滚动视图的高度 适用于没有悬浮到需要的位置的时候
        WMZPagePropStatementAndPropSetFuncStatement(copy, WMZPageParam, PageCustomFrameY,        wCustomDataViewHeight)
     4 在父控制住self.view addSubview 了自定义的View 看不见 需要延迟0.1秒加载
     5 更新标题数据用updateTitle  更新标题和视图层用updateMenuData 都需要设置param的相关数据后调用
     6 菜单栏不想悬浮要一起滑动 
        .wCustomDataViewHeightSet(^CGFloat(CGFloat nowY) {
            return nowY + (menu的高度 默认55);
        })

下一步计划
==============
- 从WMZPageController抽出,无需继承也可使用 （已完成，可使用WMZPageView）
- 适配横竖屏旋转（已完成）
- 优化下拉缩放
- swift版本开发

更新日记
==============
- 20220923 v1.5.5 修复一些bug 
- 20220819 v1.5.4 修复一些bug 
- 20220531 v1.5.3 修复 issues84 新增自定义标题文本wCustomTitleContent 可传入自定义model自行赋值
- 20220118 v1.5.2 修复 issues77 issues78
- 20220118 v1.5.1 支持适配横竖屏 wDeviceChange(default NO) 
- 20220117 v1.5.0 改版不需要继承WMZPageController也能使用（使用WMZPageView）,同时适配旧版本
- 20211230 v1.4.6 修复退出后台挂起后可能导致拉不下来的问题 fix#68
- 20211208 v1.4.5 修复自定义导航栏下的偏移问题
- 20211026 v1.4.4 修复多重嵌套手势问题 新增wMenuAddSubView 可在菜单栏增加自定义视图 
- 20211021 v1.4.2 修复多重嵌套下纵向手势滚动问题以及动态增加方法里和固定视图冲突问题
- 20211015 v1.4.1 支持侧滑/全屏/全部页面返回 新增两种动画JDAnimal NewAQY 修复KVO崩溃问题
- 20210814 v1.4.0 新增支持UIView传入/修复嵌套手势问题/新增下拉头视图缩放 
- 20210526 v1.3.8 修复嵌套里头视图无法滑动的问题 新增自定义手势冲突属性
- 20210426 v1.3.7 修复没有滚动视图无法滚动的问题以及其他问题
- 20210422 v1.3.6 主要是消除一系列的警告
- 20210128 v1.3.5 优化
- 20210127 v1.3.4 新增动态更新 修复右边按钮只能点击一次的问题 优化
- 20201218 v1.3.3 新增动态增删方法 优化
- 20201022 v1.3.2 iPhone12适配 修复bug 优化结构 
- 20201009 v1.2.7 修复bug
- 20200920 v1.2.6 淘宝demo优化 新增自定义顶部距离 自定义整体高度 自定义底部距离
- 20200904 v1.2.5 淘宝demo增加圆角示范,优化加入的控制器,传入字体增加UIFont对象
- 20200820 v1.2.4 修复bug/新增swift使用示范 
- 20200801 v1.2.1 修复bug 
- 20200726 v1.2.0 新增淘宝分页效果/美团商家分页效果 
- 20200605 v1.1.9 新增自定义红点和特殊样式1
- 20200511 v1.1.8 修复bug
- 20200424 v1.1.7 修复细节问题 
- 20200409 v1.1.6 修复偏移问题 
- 20200328 v1.1.5 修复设置导航栏translant和tabbar设置translant的布局问题; 新增wFixFirst属性 固定在所有控制器的底部的尾视图
- 20200202 v1.1.4 修复bug 
- 20200107 v1.1.3 修复bug 新增可固定底部
- 20191213 v1.1.0 建议更新 新增可添加tableviewCell功能
- 20191213 v1.0.5 增加demo说明 新增自定义菜单接口
- 20191209 v1.0.4 修复bug
- 20191207 v1.0.3 修复悬浮问题
- 20191104 v1.0.1 修复一些问题
