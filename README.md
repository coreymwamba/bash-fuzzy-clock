bashfuzzyclock
==============

bash-fuzzy-clock is a natural language or "fuzzy" clock script, written in Bash. Use it in anything that accepts script output (like Conky, or i3bar, or swaybar or...) as a desktop-agnostic fuzzy clock. Translated to six languages.

INSTALL:
========

If you're on Arch Linux you can install this from the AUR:

<https://aur.archlinux.org/packages/bash-fuzzy-clock-git/>

If not, from a terminal:

```
$ tar xf bash-fuzzy-clock.tar.gz
$ sudo install -v bash-fuzzy-clock.sh -m 0755 /usr/bin/bash-fuzzy-clock
```

If you need a translation, make sure you 
have `LANGUAGE` set in .bashrc (and for Conky, .xinitrc) or 
/etc/locale.conf

```
$ sudo msgfmt fr.po -o /usr/share/locale/fr/LC_MESSAGES/bash-fuzzy-clock.mo
$ sudo msgfmt de.po -o /usr/share/locale/de/LC_MESSAGES/bash-fuzzy-clock.mo
$ sudo msgfmt es.po -o /usr/share/locale/es/LC_MESSAGES/bash-fuzzy-clock.mo
$ sudo msgfmt it.po -o /usr/share/locale/it/LC_MESSAGES/bash-fuzzy-clock.mo
$ sudo msgfmt pt.po -o /usr/share/locale/pt_BR/LC_MESSAGES/bash-fuzzy-clock.mo
```

USE
===

Just invoke it:

```
$ bash-fuzzy-clock
--> nearly twenty past seven
```

You can use the "m" option to display the general time of day:

```
$ bash-fuzzy-clock m
--> morning 
```
Using Conky, you can set the script to run every minute (or perhaps, if you just want, every five minutes). See <https://github.com/brndnmtthws/conky/wiki> for Conky's wiki.

Using Tint2, you use the executor panel item to run the script. See <https://gitlab.com/o9000/tint2/blob/master/doc/tint2.md#executor> for more details, or just use tint2conf.

On an Apple computer, you can use GeekTool to display the clock on your 
screen, using a Shell Geeklet: see 
<https://lifehacker.com/5834676/build-an-attractive-informative-mac-desktop-with-geektool>

TRANSLATIONS
============
If you want to translate bash-fuzzy-clock to your language, please do! Make a fork, and add a new .po file.

WHAT IS A FUZZY CLOCK?
======================

Fuzzy clocks display a generalisation of the time in informal or natural 
language. They only give precise time on the hour and at five-minute intervals from the hour.

WHY ANOTHER FUZZY CLOCK?
========================


There are a number of fuzzy clock implementations which

1. don't work in any other language than English;
2. are not fuzzy - they simply display the exact time in words; or
3. require Python

and at the time of first writing the script, I couldn't find a clock 
that I liked. So I made one that only required Bash, was fuzzy, and was 
(to the limits of my language knowledge) translatable.
