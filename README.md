![XYSideViewController](images/icon.png)

## XYSideViewController
一个侧拉菜单控制器(仿QQ侧拉栏)

**Email : firehsia1204@gmail.com**

**欢迎Issue 欢迎邮件 欢迎Star** 

![demoGif](images/demoGif.gif)

## 版本记录
1.0.3 --- 代码重构

1.0.2 --- 修复初始状态侧拉菜单位置bug

1.0.1 --- 初始版本

## Installation

1. OC版本 
 
		直接将XYSideViewController文件夹下OC文件添加到工程
	
	Swift版本
	
		直接将XYSideViewController文件夹下Swift文件添加到工程

2. cocopods
 
 > pod 'XYSideViewController', '~> 1.0.4'
 
 > 注: 请在PodFile 后面添加 use_frameworks!
 
 >  若找不到该库 请先执行 `pod repo update`  再 `pod install`
 
 
## OC版本

1. 初始化```XYSideViewController```作为```window.rootViewController```
 
	```
	XYSideViewController *rootViewController = [[XYSideViewController alloc] initWithSideVC:leftViewController currentVC:tabBarViewController];
	self.window.rootViewController = rootViewController;
	```
	
	- SideVC :  左侧控制器
	 
	- currentVC : 主控制器
 
2. 侧拉栏属性
 
   - sideContentOffset 
    
  		- 可侧拉最大偏移量  
  		
  		- 默认值:  3/4 * 屏幕宽
   - currentVCPanEnableRange
     
  		- pan侧拉手势范围  
 	  
  		- 默认值: 50
   - isSide 
    
   		- 侧拉开关
   		
   		- 默认值: 开启
   - currentNavController

     	- 获取主VC当前的导航控制器
     
   - (void)closeSideVC 
    
     	- 关闭侧拉栏
   - (void)openSideVC 

   		- 打开侧拉栏
  
3. UIViewController+XYSideCategory
   - sideViewController 
    
   		- 获取侧拉控制器
   - ```- (void)XYSidePushViewController:(UIViewController *)viewController animated:(BOOL)animated``` 
  
 	 	- 左侧控制器push
   - ```- (void)XYSideOpenVC``` 

   		- 打开侧拉栏
  
  
## Swift版本
1. 初始化
 
	 ```
	 let rootVC = XYSideViewControllerSwift(sideVC, currentMainVC)
	  
	 window?.rootViewController = rootVC 
	 ```

2. 属性和方法
   - currentVCPanEnableRange
     
  		- pan侧拉手势范围  
 	  
  		- 默认值: 50
   - isSide 
    
   		- 侧拉开关
   		
   		- 默认值: 开启
   - currentNavController

     	- 获取主VC当前的导航控制器
     
   - closeSideVC() 
    
     	- 关闭侧拉栏
   - openSideVC()

   		- 打开侧拉栏


