# Huajh Awesome Latex CV 中文版 

+ **English Version** is in the [master](https://github.com/huajh/awesome-latex-cv/tree/master) branch

+ **中文版本**（包括所有所需文件）: [zh-cn](https://github.com/huajh/awesome-latex-cv/tree/zh-cn) 分支

+ 该分支**不包括中文字体**

## 样例

中文样例: [PDF](http://huajh.github.io/cv/awesome-cv-cn.pdf)

![Example](http://huajh.github.io/img/cv/awesome-cv-cn-1.png)
![Example](http://huajh.github.io/cv/awesome-cv-cn-2.png)

## 说明

由于zh-cn分支中的中文字体库太大，git clone的速度很比较慢。因此新建了这个分支，不包括中文字体库。

## 下载/clone

可以用以下命令clone该分支：

```
git clone --branch zh-cn-nofonts --depth 1 --single-branch https://github.com/huajh/awesome-latex-cv.git  <folder>
```

## 使用

如果系统已经按照了adobe的中文字体，可以选择在`awesome-cv-cn.tex`主程序中选择使用系统字体，如下

```matlab

% 在awesome-cv-cn.tex主文件中

%\usepackage{zh_cn-adobefonts_external} % Simplified Chinese Support using external fonts (./fonts/zn_cn-adobe/)
\usepackage{zh_cn-adobefonts_internal} % Simplified Chinese Support using system fonts
```

### 可选方案

如果你的系统未安装相关字体，我这里也提供了国内的[下载链接](https://pan.baidu.com/s/1qXEevJe), 应该有可靠的速度。
将下载的字体放到`./fonts/zn_cn-adobe/`目录下。

## 编译

+  采用 `xelatex` 编译。
+  需要 [fontawesome Package version 4.6.3.2.](http://www.ctan.org/tex-archive/fonts/fontawesome) 或更高版本（已经放在仓库的主目录下）。
+  中文支持借鉴[billryan/resume/tree/zh_CN的中文分支](https://github.com/billryan/resume/tree/zh_CN),`zh_cn-adobefonts_external.sty`,`zh_cn-adobefonts_internal.sty`和adobe字体库(在`fonts/zh_cn-adobe/`目录下,56.4MB)都来自于该仓库分支，感谢分享。



## The Latex 文件结构

```matlab
% cls file
awesome-source-cv.cls   

% main file 主函数
huajh-awesome-cv.tex

%subsection
  - section_headline.tex
  - section_education.tex
  - section_publications.tex
  - section_skills.tex
  - section_experience_short.tex
  - section_languages.tex
  - section_awards.tex
  - section_interests.tex
```

## License

The LaTeX Project Public License
