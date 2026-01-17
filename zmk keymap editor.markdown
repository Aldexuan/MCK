---
layout: default
title: zmk keymap editor
has_children: false
parent: Keymap Editing
---
## 键盘仓库链接地址:
~~~
https://github.com/Aldexuan/zmk-config-keyball61
~~~

## 1：构建自己的键盘代码库
1: 打开上面仓库链接,按照下图箭头位置，在右上方点击 Fork 
![zmk01.png](static/zmk/zmk01.png){: width="100%" }<br/>
2:<br/>
步骤1把 "Copy the main branch only"取消☑️可以fork所有分支
步骤2 点击 "Create fork" 即可创建自己的代码仓库
![zmk02.png](static/zmk/zmk02.png){: width="100%" }<br/>
## 2：固件工作流构建流程
1：在你自己的仓库点击上方的 "Action" 可以进入固件构建页面
![zmk03.png](static/zmk/zmk03.png){: width="100%" }<br/>
2：按照图中箭头指示点击确认自己了解工作流
![zmk04.png](static/zmk/zmk04.png){: width="100%" }<br/>
3：在页面左侧栏点击带 "bulid.ymal" 的工作流
![zmk05.png](static/zmk/zmk05.png){: width="100%" }<br/>
4：点击右边 1："Run workflow"下拉框 2：选择自己的分支 3：点击 "Run workflow"
![zmk06.png](static/zmk/zmk06.png){: width="100%" }<br/>
5：点击 "Run workflow" 后刷新一下页面可以看到构建固件的工作流，点击进去
![zmk07.png](static/zmk/zmk07.png){: width="100%" }<br/>
6：等待工作流构建完成，在最下方会出现一个 "firmware" 压缩包，点击下载固件
![zmk08.png](static/zmk/zmk08.png){: width="100%" }<br/>
## 3：编辑键位
### 1：zmk-studio 实时改建
```
https://zmk.studio/
```
* 使用zmk-studio修改键位，因为官方工具本身限制，仅支持基础键值修改
* 打开上面链接进入即可，主手使用usb进行连接修改键位
![zmk09.png](static/zmk/zmk09.png){: width="100%" }<br/>
![zmk10.png](static/zmk/zmk10.png){: width="100%" }<br/>
![zmk11.png](static/zmk/zmk11.png){: width="100%" }<br/>
* 按图示进入 zmk-studio 进行键位修改，修改之后点击右上角保存即可
### 2：自己改源码
* 如果自己会修改，可以把你自己仓库的代码 git 到本地，在本地修改后，再提交构建工作流会自动构建<br/>
### 3：使用 keymap-editor 在线编辑
```
https://nickcoutsos.github.io/keymap-editor/
```
#### 3-1:授权 keymap-editor 
* 打开上方链接，进入页面选择下图 github 选项
![zmk12.png](static/zmk/zmk12.png){: width="100%" }<br/>
* 在弹出的页面如果有登录页面，就进行登录(首次进入需要登录授权，之后就不需要了)
![zmk13.png](static/zmk/zmk13.png){: width="100%" }<br/>
* 使用github进行授权
![zmk14.png](static/zmk/zmk14.png){: width="100%" }<br/>
* 添加代码仓库
![zmk15.png](static/zmk/zmk15.png){: width="100%" }<br/>
* 按照图示1，2，3 选择特定键盘仓库进行授权
![zmk16.png](static/zmk/zmk16.png){: width="100%" }<br/>
* 授权完特定键盘代码库后会自动识别代码仓里的文件生成键位
* 在 "Branch"里选择键盘对应分支即可对键位进行修改
* ![zmk17.png](static/zmk/zmk17.png){: width="100%" }<br/>
#### 3-2：键位修改
* 每一个键位有两个显示区域，红色区域是绑定行为，蓝色区域是键值
红色基础按键有：&kp，&lt，&mo等等，其他可自行探索
![zmk18.png](static/zmk/zmk18.png){: width="100%" }<br/>
* 点击每个键位在弹出的弹框里可对该键位进行键位编辑
* 弹框里1代表红色区域，2代表蓝色区域
* 1-选择&kp代表基础键位，选择后在2-选择具体键值，最后点击"Apply"
![zmk19.png](static/zmk/zmk19.png){: width="100%" }<br/>
* 1-选择&lt代表长按切层，短按输出键值
* 2-选择长按切到的具体层，3-选择短按输出的键值， 4-应用
* 下图就是长按进入 1 层，短按输出 数字2
![zmk20.png](static/zmk/zmk20.png){: width="100%" }<br/>
* 如果在选择键值的时候按 1 选择修饰键 然后在 2 选择键值 就能形成对应快捷键
* 下图就是设置该按键输出是 Ctrl + C
* 1 不选择任何，只在 2 位置选，就是正常键值
![zmk21.png](static/zmk/zmk21.png){: width="100%" }<br/>
* 其他也是大概的操作
#### 3-3：Macros(宏)
* 按下图，1-进入 Macros 编辑页面， 2-添加新的 Macros
* 注意 Macros 名字要唯一，不能重复 
![zmk22.png](static/zmk/zmk22.png){: width="100%" }<br/>
* 添加好新的 Macros 页面会出现三个按钮，可以根据自己的需求对这个Macros进行设定
* 第一个是行为控制后面两个都是按键，相关高阶玩法具体可以咨询AI
![zmk23.png](static/zmk/zmk23.png){: width="100%" }<br/>
* 定义好的 Macros 切回到 LAYERS 标签页，跟修改键值一样使用即可
![zmk24.png](static/zmk/zmk24.png){: width="100%" }<br/>
* 只需要在修改键值的地方点击 "Behavior" 搜索刚刚定义的 Macros 名字即可 
![zmk25.png](static/zmk/zmk25.png){: width="100%" }<br/>
#### 3-4：combos
* 切换到 combos 选项卡 点击 "Add New Combo"
![zmk26.png](static/zmk/zmk26.png){: width="100%" }<br/>
* 1-填写 combo 的名字 2-输出的内容 
* 3-同时按哪些按键输出键值 4 创建
* 2是点击进入可以设置输出的内容，根据自己的想法设置
![zmk27.png](static/zmk/zmk27.png){: width="100%" }<br/>
* 创建完，如下图 1 名称 2 输出内容 3 具体哪些按键
* 下图就是右手 7，8两个按键按下触发 soft_off 软关机
![zmk28.png](static/zmk/zmk28.png){: width="100%" }<br/>

### 4:keymap-editor 提交 编译固件
* 全部改完后，点击 save 进行修改的保存
![zmk29.png](static/zmk/zmk29.png){: width="100%" }<br/>
* 在弹框里面填写修改的备注，用来提示自己本次修改了什么
![zmk30.png](static/zmk/zmk30.png){: width="100%" }<br/>
* 回到自己的 github 对应的代码仓库，在 action 页面会看到本次修改的提交
* 工作流会自动构建固件，点进去，等固件构建完成
![zmk31.png](static/zmk/zmk31.png){: width="100%" }<br/>
* 下载构建好的固件刷入键盘即可
![zmk08.png](static/zmk/zmk08.png){: width="100%" }<br/>

### 5：刷写键盘固件
* 解压下载的固件压缩包
* 会出现三个文件，left, right, reset
![zmk32.png](static/zmk/zmk32.png){: width="100%" }<br/>
* 左右手单独操作，刷固件需要将键盘单独连接电脑
* 刷固件时建议关闭电池再连接数据线，经测试，部分电脑供电端口电压不足
* 导致插上数据线也没办法识别数据线接入，还是保持蓝牙连接状态，无法进行固件写入
* 连接好数据线，双击键盘上的 reset 按钮，此时电脑会弹出一个 nicenano 的U盘
* 不要删除里面的任何东西，把要刷入的固件拖进去就行，不要复制粘贴，使用鼠标拖进去
* 如果只是修改键位，可以只刷主手就可以(不同键盘主手定义不同，可咨询卖家）
* 如果出现只刷主手连接不上的情况，就需要全流程刷一遍
* 刷写全流程顺序，严格按照以下顺序：
* * 左手刷 reset 固件
* * 右手刷 reset 固件
* * 左手刷 left 固件
* * 右手刷 right 固件
* 注意是先把两个手都刷入reset 固件之后，再单独刷左右手固件