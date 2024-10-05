## 安装字体相关命令

mtxrun --generate
mtxrun --script font --reload

查找你想要字体（包括文件名和符号名称），比如：

mtxrun --script fonts --list --all --pattern=*noto*cjk*light*

或列出四种特性：

>mtxrun --script fonts --list --spec deng-light
