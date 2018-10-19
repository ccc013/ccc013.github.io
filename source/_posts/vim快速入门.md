---
title: vim快速入门
date: 2018-10-19 21:53:10
tags:
- Linux
- vim


---

> 本文大约 5000 字， 阅读大约需要  10 分钟

在 Linux 下最常使用的文本编辑器就是 vi 或者 vim 了，如果能很好掌握这个编辑器，非常有利于我们更好的在 Linux 下面进行编程开发。

#### vim 和 vi

Vim是从 vi 发展出来的一个文本编辑器。代码补完、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用。

简单的来说， vi 是老式的字处理器，不过功能已经很齐全了，但是还是有可以进步的地方。 vim 则可以说是程序开发者的一项很好用的工具。

下面是 vim 快捷键盘图：

![vim 快捷键](http://upload-images.jianshu.io/upload_images/1171928-dccc21832804abca.gif?imageMogr2/auto-orient/strip)

#### vi/vim 的工作模式

基本上 vi/vim 共分为三种模式，分别是命令模式（Command mode），输入模式（Insert mode）和底线命令模式（Last line mode）。 这三种模式的作用分别是：

##### 命令模式

当使用 vi/vim 打开一个文件就进入了命令模式（也可称为一般模式），这是默认的模式。在这个模式，你可以采用『上下左右』按键来移动光标，你可以使用『删除字符』或『删除整行』来处理档案内容，也可以使用『复制、贴上』来处理你的文件数据。

##### 输入模式

在命令模式并不能编辑文件，需要输入如『i, I, o, O, a, A, r,R』等任何一个字母之后才会进入输入模式（也称为编辑模式）。注意了！通常在 Linux 中，按下这些按键时，在画面的左下方会出现『 INSERT 或 REPLACE 』的字样，此时才可以进行编辑。而如果要回到命令模式时，则必须要按下『Esc』这个按键即可退出编辑模式。

##### 底线命令模式

在命令模式下，按下『:,/,?』中任意一个，就可以将光标移动到最底下那一行，进入底线命令模式（也称为指令列命令模式）。在这个模式当中， 可以提供你『搜寻资料』的动作，而读取、存盘、大量取代字符、退出、显示行号等等的动作则是在此模式中达成的！同理，必须按下『Esc』按钮才可以退出该模式，返回命令模式

三种模式的切换和功能可以用下图来总结：

![vi/vim 工作模式](http://upload-images.jianshu.io/upload_images/1171928-4a5e2f5c0d5f9ad2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 简易示例

###### 1. 使用 vim 打开文件

在命令行中输入如下命令：

```
$ vim test.txt
```

采用 `vi 文件名` 或者 `vim 文件名` 就可以打开文件并且进入了命令模式。这里文件名是必须添加的，当文件不存在的时候，也能打开，并且进行编辑保存后就是创建一个新的文件。打开后的界面如下图所示：

![vim1.png](http://upload-images.jianshu.io/upload_images/1171928-2d14cd1bed279c98.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

整个界面可以分为两个部分，最底下一行和上面的部分，最底下一行主要是显示当前文件名和文件的行数、列数，上图是一个新的文件，所以最底下显示的是文件名，而且后面括号也说是新文件，而下图是一个已经有内容的文件，那么上面部分就显示文件内容，最底下一行显示了文件名，文件的行数和列数，并且在最右侧部分会显示当前坐标的位置，比如图中是显示 (4,1) 表示当前坐标在第四行第一列的位置。

![vim2.png](http://upload-images.jianshu.io/upload_images/1171928-3e4ea8bb56dc11c3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###### 2. 进入编辑模式

接下来就是开始对文件进行编辑，也就是需要进入编辑模式。只要按下『i, I, o, O, a, A, r,R』等字符就可以进入编辑模式了！在编辑模式当中，你可以发现在左下角状态栏中会出现 –INSERT- 的字样，那就是可以输入任意字符的提示啰！这个时候，键盘上除了 [Esc] 这个按键之外，其他的按键都可以视作为一般的输入按钮了，所以你可以进行任何的编辑！

如下图所示：

![vim3.png](http://upload-images.jianshu.io/upload_images/1171928-f0b360a2d0f97a00.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

注意：在 vim/vi 中 [Tab] 键是向右移动 8 个空格字符。

###### 3. 按下 [ESC] 按钮回到命令模式

如果对文件编辑完毕了，那么应该要如何退出呢？此时只需要按下 [Esc] 这个按钮即可！马上你就会发现画面左下角的 – INSERT – 不见了！并且返回了命令模式了

###### 4. 退出

最后就是存盘并离开，指令很简单，输入『:wq』即可存档离开！ (注意了，按下 : 该光标就会移动到最底下一行去！) ，如下图所示：

![vim4.png](http://upload-images.jianshu.io/upload_images/1171928-744511feb00c0e7f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



#### 更多按键说明

上述简易示例只是使用了简单的几个按键，但是从 vim 快捷键图可以知道 vim 是有很多快捷键的。

vim 更多快捷键可以如下思维导图所示：

![vim 快捷键.png](https://upload-images.jianshu.io/upload_images/1171928-82328fac0d759f04.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#### 练习

题目是来自[vim 程序编辑器](http://cn.linux.vbird.org/linux_basic/0310vi.php)的练习，如下所示，使用的操作文件 man_db.conf 可以在 http://linux.vbird.org/linux_basic/0310vi/man_db.conf
处获取。

```
1. 請在 /tmp 這個目錄下建立一個名為 vitest 的目錄；
2. 進入 vitest 這個目錄當中；
3. 將 /etc/man_db.conf 複製到本目錄底下(或由上述的連結下載 man_db.conf 檔案)；
4. 使用 vi 開啟本目錄下的 man_db.conf 這個檔案；
5. 在 vi 中設定一下行號；
6. 移動到第 43 列，向右移動 59 個字元，請問你看到的小括號內是哪個文字？
7. 移動到第一列，並且向下搜尋一下『 gzip 』這個字串，請問他在第幾列？
8. 接著下來，我要將 29 到 41 列之間的『小寫 man 字串』改為『大寫 MAN 字串』，並且一個一個挑選是否需要修改，如何下達指令？如果在挑選過程中一直按『y』， 結果會在最後一列出現改變了幾個 man 呢？
9. 修改完之後，突然反悔了，要全部復原，有哪些方法？
10. 我要複製 66 到 71 這 6 列的內容(含有MANDB_MAP)，並且貼到最後一列之後；
11. 113 到 128 列之間的開頭為 # 符號的註解資料我不要了，要如何刪除？
12. 將這個檔案另存成一個 man.test.config 的檔名；
13. 去到第 25 列，並且刪除 15 個字元，結果出現的第一個單字是什麼？
14. 在第一列新增一列，該列內容輸入『I am a student...』；
15. 儲存後離開吧！
```

那么，整体步骤应该如下所示：
```
1. mkdir vitest
2. cd vitest
3. mv /etc/man_db.conf .
4. vi man_db.conf
5. :set nu
6. 43G -> 59l ->括号内是 as 这个单词
7. gg 或 1G -> /gzip -> 在第 93 列
8. 输入命令 [:29,41s/man/MAN/gc] -> 然后一直点击 y ，总共需要替换 13 个
9. 一直按 u 键即可复原；更加简单粗暴的就是强制退出，也就是输入 :q!
10. 66G 跳到 66 行 -> 6yy 复制 6 行内容(输入后，屏幕最后一行会显示 6 lines yanked) -> G 跳到最后一行，输入 p 复制到最后一行的后面
11. 113G 跳到 113 行 -> 总共需要删除 16 行内容，所以输入 16dd，删除后光标所在行开头就是 ‘#Flags’
12. 输入 [:w man.test.config] 实现保存操作，接着可以输入 [:! ls -l]，即显示查看当前文件夹内文件内容的命令 ls -l 显示的内容在 vim 内，再次按下回车键即回到 vim 命令模式
13. 输入 25G 到 25 行 -> 15x 删除 15 个字符，然后显示的是 tree
14. gg / 1G 到 第一行 -> O 在上方新增一行，然后输入 『I am a student...』-> Esc 键返回命令模式
15. [:wq] 或者 ZZ 保存离开文件
```

本文参考文章如下：

- vim 程序编辑器(http://cn.linux.vbird.org/linux_basic/0310vi.php)
- Linux vi/vim(http://www.runoob.com/linux/linux-vim.html)

------

以上就是本文的主要内容和总结，欢迎关注我的微信公众号--机器学习与计算机视觉或者扫描下方的二维码，和我分享你的建议和看法，指正文章中可能存在的错误，大家一起交流，学习和进步！

公众号后台回复“vim快捷键”可以获取 vim 思维导图！

![image](http://upload-images.jianshu.io/upload_images/1171928-51f7b495edfa7210.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**推荐阅读**
1.[机器学习入门系列(1)--机器学习概览(上)](https://mp.weixin.qq.com/s?__biz=MzU5MDY5OTI5MA==&mid=2247483667&idx=1&sn=c6b6feb241897ede16bd745d595cef92&chksm=fe3b0f66c94c86701e9b071e62750d189c254fd3ebe9bb6251505162139efefdf866093b38c3&token=2134085567&lang=zh_CN#rd)
2.[机器学习入门系列(2)--机器学习概览(下)](https://mp.weixin.qq.com/s?__biz=MzU5MDY5OTI5MA==&mid=2247483672&idx=1&sn=34b6687030db92fd3e04dcdebd09fffc&chksm=fe3b0f6dc94c867b2a72c427ebb90e2a683e6ad97ea2c5fbdc3a3bb86a8b159b8e5f107d2dcc&token=2134085567&lang=zh_CN#rd)
3.[[实战] 图片转素描图](https://mp.weixin.qq.com/s?__biz=MzU5MDY5OTI5MA==&mid=2247483679&idx=1&sn=229eaae83f0fad327d4ae419dc6bf865&chksm=fe3b0f6ac94c867cf72992dd2ec118d165c3990818ddd45d5a87736bac907b8871e8a006e9ab&token=2134085567&lang=zh_CN#rd)






