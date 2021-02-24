# pdf-tricks
This repo keeps my pdf processing howto in Linux (and possibly all other OS-es)

Most of used tools are easy to install and can make your pdf processing so easy and enable you to save a lot of time. Of source you can use Inkscape to hand craft your pdf (and sometimes it is best option), but there are a lot of tools in the wild, which can save you enormous amount of time.

## Background

I love to craft my own PNP (Play And Print) board/card/rpg games. There are plenty of PNP games in boardgamegeek.com and other sites, but usually those downloadable files are unfortunately not very good for direct printing. I like to keep my games small in size, print only necessary components, modify graphics, adding cutting (crop) marks, etc. So PDF processing is necessary. This readme should give you ideas, how to attack some tasks and will remind me how to do it, when I forget.

## Tools used

I use all of following tools. Order is not important, they are all great and essential for me.

Command line:

* pdftk
* pdfjam
* poppler (poppler utils)
* imagemagick (and scripts)

GUI:

* pdfbooklet (Windows version)
* pdfarranger (flathub)
* pdf mix tools (flathub)
* scantailor


## Examples

### PocketMod

PocketMod is a paper folded in a way it forms a small book.

**Prepare**

```shell
git clone https://github.com/DavidFirth/pdfjam-extras
sudo cp pdfjam-extras/bin/* /usr/local/bin/
```



## Converting fonts to paths

Converting fonts to paths allows you to edit PDF in something like Inkscape without worrying about missing fonts.

```shell
gs -o out-txtpath.pdf -dNoOutputFonts -sDEVICE=pdfwrite in.pdf
```

Adding elements like cutting marks or other helpers into existing pages.

```shell
pdftk org.pdf background my/my_cutting_marks.pdf output my/out.pdf
```
