# Huajh Awesome Latex CV  

+ This is CV in English.

+ 中文用户可以到 [zh-cn](https://github.com/huajh/awesome-latex-cv/tree/zh-cn) branch， 包括所有所需文件。


+ zh-cn分支仓库比较大，主要是中文字体比较大，国内用户下载速度慢的可以移步到 [zh-cn-nofonts](https://github.com/huajh/awesome-latex-cv/tree/zh-cn-nofonts) branch，该分支不含中文字体，提供国内下载链接。



## Example

An output example can be found [here](http://huajh7.com/cv/awesome-cv.pdf)

![Example](http://huajh7.com/img/cv/awesome-cv-1.png)
![Example](http://huajh7.com/img/cv/awesome-cv-2.png)


**中文样例**: [PDF](http://huajh7.com/cv/awesome-cv-cn.pdf)

![Example](http://huajh7.com/img/cv/awesome-cv-cn-1.png)
![Example](http://huajh7.com/img/cv/awesome-cv-cn-2.png)


## clone
Since the Simplified Chinese fonts files in `zh-cn` branch are very large,  if you only need a CV in Enlish, it is better to clone only the master branch. 

The command is 

```
 git clone --branch master --depth 1 --single-branch https://github.com/huajh/awesome-latex-cv.git 
```


## Setup 

This latex CV template uses `luatex` engine and needs [fontawesome Package version 4.6.3.2.](http://www.ctan.org/tex-archive/fonts/fontawesome) or higher version.

## About

Huajh awesome Latex CV was originally based on a CV template created by Christophe Roger (Darwiin). This template use `luatex` engine and `Source Sans Pro Font` from Adobe.

More informations about the original Christophe Roger (Darwiin) template can be found here :

   -  [ Github ](https://github.com/darwiin/awesome-neue-latex-cv)
   -  [ Overleaf ](https://www.overleaf.com/latex/templates/awesome-source-cv/wrdjtkkytqcw)   


## The Latex file structure

```matlab
% cls file
awesome-source-cv.cls   

% main file
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