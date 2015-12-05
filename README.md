# Runtime_Application
## 一 Runtime介绍

Objective-C是由Brad Cox和Tom Love于上世纪80年代，在C语言基础上，加入了面向对象特性和Smalltalk式的消息传递机制的扩展。而这个扩展的核心就是一个用C和汇编语言写的RunTime库，这个库所做的事情就是加载类信息，进行方法的分发和转发，也正是这个库赋予了Objective-C的动态特性。

我们从[官方API](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ObjCRuntimeGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40008048)中,可以了解到：

* runtime机制就是把代码执行的决策从编译和链接的时候，推迟到运行时。。也就是说只有编译器是不够的，还需要一个运行时系统 (runtime system) 来执行编译后的代码。这就是 Objective-C Runtime 系统存在的意义，它是整个Objc运行框架的一块基石,也是我们代码幕后运行的工作者。

* Runtime拥有Legacy（早期） and Modern（现行）两个版本。我们现在用的 Objective-C 2.0 采用的是现行(Modern)版的Runtime系统，只能运行在 iOS 和 OS X 10.5 之后的64位程序中。而OS X较老的32位程序仍采用 Objective-C 1中的（早期）Legacy 版本的 Runtime 系统。这两个版本最大的区别在于当你更改一个类的实例变量的布局时，在早期版本中你需要重新编译它的子类，而现行版则不需要。 
