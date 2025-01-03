跟ConTeXt中文字体设置和使用相关的一些例子。

## 文件

1. ConTeXt自带、**可直接使用**的中文mscore字体家族的用例，官方设置文件是`type-imp-mscore.mkiv`
    * mscore_testing.lmtx
2. 以安全稳定为目标的Win10、Win11中英文混排字体配置，中文使用系统自带的华文字体 **（设置方式是最新的，比较完善，可作为日用模版）**
    * winzh.tex
    * winzh-test.lmtx
3. noto加其他字体的设置，面向实际的印刷图书
    1. notoplus.tex
    2. notoplus-test.lmtx
    3. 一本已经正式出版的书的实际配置，后备字体稍复杂
        1. notoplusplus.tex
        2. notoplusplus-test.lmtx
4. 以开源简体中文字体[notocjksc](https://github.com/notofonts/noto-cjk)、[朱雀仿宋](https://github.com/TrionesType/zhuque)、[霞鹜文楷](https://github.com/lxgw/LxgwWenKai)为主的设置，拉丁字符使用latinmodern系列
    * opensc.tex
    * opensc-test.lmtx
5. [方正字库“商业发布”免费字体](https://www.foundertype.com/index.php/About/powerbus.html)。请自行处理版权问题！
    * fz.tex
    * fz-test.lmtx
6. noto系字体设置，设置方式比较老了
    * type-imp-notocjksc.mkiv
7. 利用后背字体设置测试各种字体对难字的支持
    * 难字.lmtx

## 安装字体相关命令

字体文件可以出放在`tex/texmf-fonts/fonts/`，或`tex/texmf-fonts/fonts/truetype/vendor/fontfamily`（注意对应字体类型）

使用系统字体，先设置环境变量，如：

```shell
set OSFONTDIR=C:\Windows\Fonts
```

更新文件目录，重载字体：

```shell
mtxrun --generate
mtxrun --script font --reload
```

查找你想要字体（包括文件名和符号名称），比如：

```shell
mtxrun --script fonts --list --all --pattern=*noto*cjk*sc*
```

或列出四种特性：

```shell
>mtxrun --script fonts --list --spec deng-light
```

