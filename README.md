跟ConTeXt中文字体设置和使用相关的一些例子。

## 文件

1. 以安全稳定为目标的Win10、Win11中英文混排字体配置，中文使用系统自带的华文字体 **（设置方式是最新的，比较完善，可作为日用模版）**
    * winzh.tex
    * winzh-test.lmtx
1. ConTeXt自带、**可直接使用**的中文mscore字体家族的用例，官方设置文件是`type-imp-mscore.mkiv`
    * mscore_testing.lmtx
1. noto系字体设置，设置方式比较老了
    * type-imp-notocjksc.mkiv
1. 利用后背字体设置测试各种字体对难字的支持
    * 难字.lmtx

## 安装字体相关命令

```shell
>mtxrun --generate
>mtxrun --script font --reload
```

查找你想要字体（包括文件名和符号名称），比如：

```shell
>mtxrun --script fonts --list --all --pattern=*noto*cjk*light*
```

或列出四种特性：

```shell
>mtxrun --script fonts --list --spec deng-light
```
