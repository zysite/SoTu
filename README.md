# sotu

利用[Flask](http://flask.pocoo.org/docs/0.12/)框架实现的基于内容的图像检索(Content Based Image Retrieval, CBIR)系统

## 要求

`python`版本：`3.5.2`

`pip`版本： `9.0.3`

相关组件要求见`requirements.txt`

## 浏览器兼容

由于使用了部分HTML5的特性，因此仅支持现代浏览器，IE9及以下的浏览器可能会有显示问题. 此外由于对于input元素中files属性安全性政策执行的不同，部分浏览器的「Drag & Drop」功能会受影响，相关情况见[W3C testing](https://github.com/w3c/web-platform-tests/pull/6617).  
页面显示及各项功能在新版本的Chrome、FireFox及Edge上经测试没有问题.

## 初始化

下载仓库并进入相应目录：

```sh
$ git clone https://github.com/zy2625/SoTu.git
$ cd SoTu
```

### 虚拟环境

首先确保安装`virtualenv`，创建虚拟环境并激活.

在虚拟环境下需要安装所有必要的组件，并设置环境变量`FLASK_APP`的值.

在Linux下所有的命令为：

```sh
$ virtualenv venv
$ . venv/bin/activate
$ pip install -r requirements.txt
$ export FLASK_APP=sotu.py
```

其中激活虚拟环境的命令在Windows的环境下有所不同：

```sh
$ venv\Scripts\activate
```

如果是用cmd设置环境变量`FLASK_APP`，需要用`set`代替上面的`export`. 

如果是用powershell设置，则命令为：

```sh
$ $env:FLASK_APP="sotu.py"
```

### 图像特征提取

利用`SIFT+BoF`模型提取[caltech101](http://www.vision.caltech.edu/Image_Datasets/Caltech101)数据集的图像特征：

```sh
$ flask extract
```

## 运行

运行应用时可以指定主机和端口：

```sh
$ flask run -h localhost -p 8080
```

最后退出虚拟环境：

```sh
$ deactivate
```

## 相关链接
[Explore Flask — Explore Flask 1.0 documentation](http://exploreflask.com/en/latest/index.html)  
[关于Flask表单，我所知道的一切](https://zhuanlan.zhihu.com/p/23577026?refer=flask)  
[Flask-WTF：单个页面两个（多个）表单](https://zhuanlan.zhihu.com/p/23437362)  
[Flask: show flash messages in alertbox](https://stackoverflow.com/questions/33580143/flask-show-flash-messages-in-alertbox)  
[How to make this Header/Content/Footer layout using CSS?](https://stackoverflow.com/questions/7123138/how-to-make-this-header-content-footer-layout-using-css)  
[Drag and Drop File Upload jQuery Example](http://hayageek.com/drag-and-drop-file-upload-jquery/)  
[How to set file input value when dropping file on page?](https://stackoverflow.com/questions/47515232/how-to-set-file-input-value-when-dropping-file-on-page)  
[使用纯 CSS 实现 Google Photos 照片列表布局](https://github.com/xieranmaya/blog/issues/4)  
[window.onload vs document.onload](https://stackoverflow.com/questions/588040/window-onload-vs-document-onload)  
[Targeting flex items on the last row](https://stackoverflow.com/questions/42176419/targeting-flex-items-on-the-last-row)  
[Image inside div has extra space below the image](https://stackoverflow.com/questions/5804256/image-inside-div-has-extra-space-below-the-image)  
[How TO - Image Overlay Title](https://www.w3schools.com/howto/howto_css_image_overlay_title.asp)  