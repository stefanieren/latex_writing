参考了知乎的问答 https://www.zhihu.com/question/22906637 

[code]
%!TEX program = xelatex
%!TEX TS-program = xelatex
%!TEX encoding = UTF-8 Unicode

```
\documentclass[12pt]{article} 
\usepackage{url} 
\usepackage{fontspec,xltxtra,xunicode} %最新的mactex都有

\defaultfontfeatures{Mapping=tex-text}
\setromanfont{Heiti SC} %设置中文字体
\XeTeXlinebreaklocale “zh”
\XeTeXlinebreakskip = 0pt plus 1pt minus 0.1pt %文章内中文自动换行，可以自行调节

\newfontfamily{\H}{Songti SC} %设定新的字体快捷命令
\newfontfamily{\E}{Weibei SC} %设定新的字体快捷命令
\begin{document}
\thispagestyle{empty}
\small{给一个比较简单的方法，在mac上折腾CJK有点麻烦，其实XeTeX就可以解决中文的问题。编码的改动其实不需要在mactex的设置里面改，写在前面然后注释掉就好了。\\
繁體字什麼的也是可以實現的。\\
当你需要打不同字体的时候，就需要用到这个\url{\newfontfamily}，这样你可以在一行中显示多种字体。比如说：\\}
\Huge{{\H 宋体} {\E 魏碑} 黑体}
\end{document}
```
**在开始的时候一直会出现乱码，后来发现是 TexStudio 没有设置 UTF-8 的编码方式。但是实际上我在编辑器的设置中已经进行了设置，所以一脸懵逼**

![FontBook](https://wx4.sinaimg.cn/mw690/6777c595gy1g1vby9lo12j20n60n0n8q.jpg)

使用的字体需要在 FontBook 中找到
