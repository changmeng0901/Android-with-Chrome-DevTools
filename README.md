# Android-with-Chrome-DevTools
在Android和Chrome DevTools远程调试，即移动设备上调试html5开发的网页

#### 移动端Web开发调试之Chrome远程调试(Remote Debugging)<br />
#### Chrome DevTools调试移动设备Brower Page Tabs/WebViews

安卓远程调试目前支持所有操作系统（Windows,Mac, Linux, and Chrome OS.）中调试，支持：

● 调试站点的页面

● 调试安卓原生App中的WebView

● 实时将安卓设备的屏幕图像同步显示到开发机器。

● 通过端口转发（port forwarding）与虚拟主机映射（virtual host mapping）实现安卓移动设备与开发服务器进行交互调试。

 

调试要求：

● 开发环境安卓桌面版Chrome32+

● 一条USB数据线，连接电脑与移动设备，安装相应机型的USB驱动。驱动程序下载地址：http://developer.android.com/tools/extras/oem-usb.html

   如果电脑上安装有百度手机助手、360手机助手这类软件，一般连接后可以自动安装相应的USB驱动程序。

● 如果是调试网页，移动设备需要安装Chrome forAndroid ，且安卓系统须为Android 4.0+

● 对于APP WebView的调试，需要系统为Android 4.4+ 并且原生应用内的Webview须进行相应的调试声明配置。

说明：远程调试要求桌面版Chrome浏览器版本要高于安卓移动设备的Chrome版本号。有条件的最好使用Chrome 的金丝雀特别版Chrome Canary (Mac/Windows)或者Chrome桌面开发版Chrome Dev channel release (Linux)。

###第一步：首先在移动设备上开启USB调试模式。方法：

*  Android 3.2+，打开设置 – 应用程序 – 开发，在“USB调试”处打钩选上

* Android 4.0~ Android 4.1 ，打开设置-开发者选项-进入在“USB调试”处打钩选上。

* Android 4.2+，打开设置-关于手机-手机配置信息-连点“版本号”7次，返回上层就可以看到“开发者选项”显示出来了，在“USB调试”处打钩选上。

###第二步：用USB数据线连接设备，驱动装好连接成功后，你可能会在设备上看到一个弹框请求允许使用这台计算机通过usb调试,勾选后点击“确定”。

###第三步：
* 在电脑上打开Chrome浏览器的菜单– 更多工具 – 检查设备（Chromemenu > More tools > Inspect Devices），或者直接在浏览器地址栏输入chrome://inspect 或者about:inspect
* 打开后DevTools后，确保打钩选中Discover USB devices
* 如果USB连接成功，这时候我们可以看到移动设备的型号和设备上运行的页面和允许调试的WebView列表。找到需要调试的目标页面，点击inspect即可打开DevTools，点击reload可重新加载当前的调试页面，点击focus tab可将标签页置顶，close为关闭当前页面。更可以通过在输入框中键入网址新开一个页面。
* 点击inspect打开DevTools后，你可以选中页面中的DOM元素，同时设备中对应元素也高亮显示，也可使用DevTools中的Inspect Element 选中目标元素，可以实时与移动设备页面交互，方便的定位问题所在，进行代码调试。
* 在输入框中输入一个新的网址，点击Opoen可打开你想要调试的新页面。
