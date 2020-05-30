latex-course
============

LaTeX'e giriş dersinin içeriği üzerine kısa bir bilgi. Slaytlar ve diğer LaTeX kaynaklarına dair kodlar 
[bu github repository'sinde](https://github.com/jdleesmiller/latex-course) bulunur (kodlar serbest MIT lisansı altındadır).

Bu rehberin amacı öğrencilere LaTeX kullanarak yazmayı hızlıca öğretmektir. Materyaller örnekler grubu ve gerektiği zaman genel konsept ve teknıklerın açıklanması şeklinde dizayn edilmiştir. Her bir parça (Part 1, Part 2 ...) [Overleaf](https://www.overleaf.com)'da yapabileceğiniz şekilde tasarlanmıştır. [Overleaf](https://www.overleaf.com) ücretsiz ve online bir LaTeX editörüdür, yani LaTeX ya da gerekli programları edinmek ile uğraşmak zorunda değilsiniz. 

Aslında iki saatlik bir atölye şeklinde dizayn edilmiştir, ama üç saat sürecek olan bir atölye için de mevcut materyaller vardır. Bu üç parça ise şunlardır: 

1. [Temel Öğeler](http://jdleesmiller.github.io/latex-course/en/part1.pdf): fikirler, sintaks, formüller, çevreler (environments), ve paketler

1. [Yapılandırılmış Dokümanlar ve Daha Fazlası](http://jdleesmiller.github.io/latex-course/en/part2.pdf): başlıklar, bölümler, etiketlemek, figürler, tablolar, bibliografya.

1. [Ödevlerden Daha Fazlası: Sunumlar & Diğerleri](http://jdleesmiller.github.io/latex-course/en/part3.pdf): tekrar egzersizleri, beamer paketi kullanarak sunum hazırmala, tikz paketi kullanarak çizim yapma.

İstediğiniz şekilde kullanmaya özgürsünüz --- her türlü katkıya açıktır!

Çeviriler
------------

Bu repo'da yer alan çeviriler şunlardır:

- `fr` Fransızca (Yannis Haralambous tarafından)

Bu repo dışında bulabileceğiniz çeviriler ise:

- [Çince](https://github.com/tanjz12/latex-course)
- [İspanyolca](https://github.com/guanucoluis/latex-course)
- [Fince](https://github.com/villeheilala/latex-course)
- [İtalyanca](https://github.com/mirtexxan/latex-course)
- [Portekizce](https://github.com/lrsantos11/latex-course)
- [Rusça](https://github.com/sgolovan/latex-course)
- [Türkçe](https://github.com/ozlemtuncel/latex-course)

Eğer siz de bu slaytları çevirirseniz, pull request yaparak kendi dosyalarınızı ya da linklerinizi ekleyebilirsiniz --- tamamen sizin tercihinize kalmış.

Development
-----------

You may need to install some extra LaTeX packages and system packages in order
to build the slides yourself.

1. The [minted package](http://www.ctan.org/pkg/minted) provides syntax
highlighting. It is installed by default in recent versions of TeX Live.

1. The minted package calls out to the
[pygments syntax highlighter](http://pygments.org/), which is written in python.
The relevant package is python-pygments in Debian / Ubuntu
(`sudo apt-get install python-pygments`).

1. There is a simple `Makefile` that manages the build. To use it, you'll
probably need to be on Linux, and you will need `make`.

The slides include links to exercises that open in Overleaf. The exercise
source files are hosted on github. If you want to use exercise files in another
location, you can [fork](https://help.github.com/articles/fork-a-repo) this
github repository and then change the `\fileuri` macro in `preamble.tex`:
```
\newcommand{\fileuri}{https://raw.github.com/jdleesmiller/latex-course/master/en}
```
so that instead of pointing to `jdleesmiller/latex-course`, it points to
`your-github-user-name/latex-course`. Then, once you've pushed your changed
exercise files to github, the slides will load them up in Overleaf.

The `deploy-to-gh-pages.sh` script builds the slides using the Makefile and
copies the slides over to the `gh-pages` branch, which is available at
`http://jdlm.info/latex-course` thanks to
[github pages](http://pages.github.com/).

License
-------

The slides and source are released under the MIT license. See the LICENSE file.

Credits
-------

* Diana A -- found that exercise links had broken
* Sana A -- pointed out an error in part 1
* Andy Roberts -- an earlier version of this course used an image from one of his articles
* Ruby Trinh -- for organising the original short courses
