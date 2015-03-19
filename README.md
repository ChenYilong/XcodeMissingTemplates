# XcodeMissingTemplates
Add
Add OC category templates to Xcode 6，pls modify PROJECT_TEMPLATES_PATH and FILE_TEMPLATES_PATH as your need.
Include:

⓵Empty Application.xctemplate

⓶Objective-C category.xctemplate

⓷Objective-C class extension.xctemplate

⓸Objective-C protocol.xctemplate

let me show you with Xcode Empty Application Template
=======================

Adding the Empty Application template back to Xcode.

<p align="center"><img title="Open and close animation" src="https://raw.github.com/rnystrom/Xcode-Empty-Application/master/screenshot.jpg"/></p>

# Installation

Clone this repository. Close Xcode.

Then in your terminal, ```cd``` into the repo directory and execute the following command:

```
sudo cp -r Empty\ Application.xctemplate /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/Project\ Templates/iOS/Application/
```
you can also do with shell:

```sh
# !/bin/sh

SAVEIFS=$IFS
IFS=$(echo -en "\n\b")

PROJECT_TEMPLATES_PATH="/Applications/Xcode6.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/Project Templates/iOS/Application"
FILE_TEMPLATES_PATH="/Applications/Xcode6.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/File Templates/Source"

EMPTY_APPLICATION_PATH="$PWD/Empty Application.xctemplate"

OC_CATEGORY_PATH="$PWD/Objective-C category.xctemplate"
OC_PROTOCOL_PATH="$PWD/Objective-C protocol.xctemplate"
OC_EXTENSION_PATH="$PWD/Objective-C class extension.xctemplate"

cp -R $EMPTY_APPLICATION_PATH $PROJECT_TEMPLATES_PATH

cp -R $OC_CATEGORY_PATH $FILE_TEMPLATES_PATH
cp -R $OC_PROTOCOL_PATH $FILE_TEMPLATES_PATH
cp -R $OC_EXTENSION_PATH $FILE_TEMPLATES_PATH

IFS=$SAVEIFS
```

# Support

This has only been tested against Xcode 6.1. If this breaks please [let me know](http://weibo.com/luohanchenyilong/).

中文：
在Apple最新的XCode6.x中没有了EmptyApplication模板，同时变换了位置的还有category，extension，protocol，这对一个老人来说是不能别接受的，同时也可以看出Apple在主力推荐IB和StoryBoard。好在XCode可以添加模板，而且可以自定义模板。下面以添加EmptyApplication模板为例做下介绍：

首先可以到 XCode5.x中复制 Empty Application 模板，定位位置如下：

​/Applications/Xcode5.x.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/ProjectTemplates/Application/

也可使用快捷键：打开任意文件夹，Shift+cmd+g。复制以上路径回车定位到目标目录，

如果无法直接访问，请按目录逐个定位。​

 找到 EmptyApplication.xctemplate 复制到XCode6.x中以上位置:

/Applications/Xcode6.x.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/ProjectTemplates/Application/
可手动添加，也通过命令：
```
sudo cp -r Empty\ Application.xctemplate /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/Project\ Templates/iOS/Application/
```

可参考上文写的shell脚本。（shell 脚本中以 Xcode6为例）
重启Xcode。​

# Support

如果不可行， [请告知我](http://weibo.com/luohanchenyilong/).

