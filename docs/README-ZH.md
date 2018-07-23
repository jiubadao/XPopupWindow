# XPopupWindow, 一个用Kotlin实现的增强版PopupWindow

![Travis](https://img.shields.io/badge/build-passing-brightgreen.svg)

[English Version](https://github.com/XuDeveloper/XPopupWindow/blob/master/README.md)

XPopupWindow是一个用Kotlin语言实现的开源库，它对系统的PopupWindow进行进一步封装和加强以便于使用。它提供了许多额外的特性例如灵活设置弹窗位置，调整弹窗动画等等。这个库能帮助你更快创建一个稳定性高的Android PopupWindow。

## 预览



## 特性

* 简单快速地创建一个自定义弹窗
* 以一种相对便捷的方式设置弹窗位置
* 更加自由地调整你的弹窗动画


## 开始

使用Gradle：

```Groovy
allprojects {
  repositories {
    ...
	 maven { url "https://jitpack.io" }
  }
}

dependencies {
  compile ''
}
```

## 使用
```Kotlin
class TestPopupWindow(ctx: Context): XPopupWindow(ctx) {
    override fun getLayoutId(): Int {
        return R.layout.test
    }

    override fun getLayoutParentNodeId(): Int {
        return R.id.parent
    }

    override fun initViews() {
    }

    override fun initData() {
    }

    override fun startAnim(view: View): Animator? {
        return null
    }

    override fun exitAnim(view: View): Animator? {
        return null
    }

    override fun animStyle(): Int {
        return -1
    }

}
```

```Kotlin
private fun showPopup() {
   popupWindow = TestPopupWindow(this, 400, 300)    
   popupWindow?.showPopupFromScreenBottom(R.layout.activity_main)
}
```

* 你可以查看xpopupwindowdemo以获取更多使用方法！

## 给我买杯柠檬茶呗 :smile:

| 微信 |支付宝 | 
| ---- | ---- | 
| ![](https://github.com/razerdp/FriendCircle/blob/master/art/wechat.jpeg)      | ![](https://github.com/razerdp/FriendCircle/blob/master/art/alipay.jpeg) |

## 协议
```license
Copyright [2018] XuDeveloper

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```