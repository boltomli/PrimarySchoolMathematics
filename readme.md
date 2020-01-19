孩子上小学一年级了，加减乘除的口算就要开始练习了，估计老师肯定会让家长出题，所以提前准备一下，利用Python开发了一套自动生成小学生口算题的小应用。而且今天是程序员节，撸200行代码庆祝一下。：）

为了让程序员老爹解放抄题的双手，让你拥有更多的时间去写代码而不用去手写几道口算题而伤神伤脑。所以有没有娃子的程序员爹爹加入一起来继续优化个开源小程序的？有什么点子，发现什么BUG，欢迎留言。

谨以此软件，献给那些热爱`Python`的程序员老爹们！

## 程序核心功能

1. 可以设置各算数项和结果的取值范围及多步算数符号的选择，可以生成求结果、求算数项、带括号的算式，最多支持3步算式题
1. 可以简单设置文档标题，小标题。设置生成的口算题文档个数

## 使用方法

1. 确定本机支持 Python 3.6.1 以上版本
1. 安装 docx，wxPython 模块
   ```
   pip3 install python-docx
   pip3 install wxpython
   ```
1. `git clone --depth=1 https://github.com/boltomli/PrimarySchoolMathematics && cd PrimarySchoolMathematics`
   * 在 macOS 上尝试打包
      ```
      pip3 install py2app
      py2applet --make-setup App.py
      python3 setup.py py2app -A # python3 setup.py py2app 暂未成功
      ```
   * 在 Linux 上打包 `pyinstaller App.py`
   * 在 Windows 上打包 `pyinstaller -w App.py`
   * 下载程序进入主目录，终端下运行 `python App.py`

### 程序界面截图

![输入图片说明](https://images.gitee.com/uploads/images/2019/0102/165314_cc68e64d_125848.png "Snip20190102_1.png")

修改运算项和结果范围里的数值,多步运算请添加修改需要的运算符号

![输入图片说明](https://images.gitee.com/uploads/images/2019/0102/165520_883d5be6_125848.png)
![输入图片说明](https://images.gitee.com/uploads/images/2019/0102/204453_e30f38d6_125848.png)

添加口算题到列表中，然后生成口算题，生成的口算题文件都在`docx`文件目录下，打开后连接打印机就可以开印了。

### 程序生成的口算题截图

![输入图片说明](https://images.gitee.com/uploads/images/2018/1119/214154_bb529734_125848.png "001.png")
![输入图片说明](https://images.gitee.com/uploads/images/2018/1119/214206_a3081f2e_125848.png "002.png")
![输入图片说明](https://images.gitee.com/uploads/images/2018/1119/214230_b9c6e3ef_125848.png "003.png")
![输入图片说明](https://images.gitee.com/uploads/images/2018/1119/214240_e946434d_125848.png "004.png")
