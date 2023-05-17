# QtMenuNote
# QMainWindow

# 菜单栏

菜单栏最多只能有一个

菜单栏用函数创建时自动放在树里面了，不需要setParent()

要有QMenuBar头文件

## 菜单栏创建(

`QMenuBar * bar = menuBar(this);`(this未考证)
或者
`QMenuBar * bar = new QMenuBar;`

## 将菜单栏放入窗口中

`setMenuBar(bar);`

## 创建菜单

`Menu * menu = bar->setMenu("文本");`

## 创建菜单中的项

`menu->addAction("文本");`

## 添加分割线

`menu->addSperator();`

# 工具栏

工具栏可以有多个

要包含QToolBar头文件

## 工具栏创建

`QToolBar * toolBar = new QToolBar(this);`

## 工具栏放入窗口中

`addMenuBar(toolBar);`

## 设置工具栏初始位置

在addMenuBar中增加参数

Qt::LeftToolBarArea

Qt::RightToolBarArea

Qt::TopToolBarArea

Qt::BottomToolBarArea

Qt::AllToolBarArea

Qt::NoToolBarArea

例:
`addMenuBar(Qt::LeftToolMenuBar,toolbar);`
## 设置浮动

`toolBar->setMovable(false);`
## 工具栏设置内容

`toolBar->addAction("文本");`

# 状态栏设置(需头文件)

`QStatusBar * sBar = StatusBar();`

## 放窗口中

`setStatusBar(stBar);`

# 放标签控件(需头文件)
```
QLabel * label = new QLabel("提示信息",this);
stBar->addWidget(label);
```
# 停靠窗口
```
QDockWidget * dwidget = new QDockWidget();
addDockWidget(Qt::BottomDockWidgetArea,dwidget);
```
#编辑窗口
```
QTextEdit * edit = new QTextEdit();
setCentralWidget(edit);
```

#小总结

在窗口中安放组件时

只能创建一个的用set

能创建多个的用add
