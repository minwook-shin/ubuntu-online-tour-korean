#UBUNTU ONLINE TOUR KOREAN
korean po file <br>
made by.minwook-shin <br>
demo site : http://minwook-shin.github.io/ubuntu-online-tour-korean <br>

#translate License
GPL 3.0

#Details License for source package
Files: * <Br>
Copyright: 2011, 2012 Canonical Ltd.<Br>
License: GPL-3+<Br>

Files: img/*<Br>
Copyright: 2011 Canonical Ltd.<Br>
License: CC-BY-SA 3.0<Br>

Files: pie/*<Br>
Copyright: 2011 Jason Johnston<Br>
License: Apache-2<Br>

Files: js/jquery.min.js<Br>
Copyright: 2011 John Resig<Br>
License: MIT<Br>

Files: js/jquery-ui.min.js<Br>
Copyright:(c) 2008 Paul Bakaus (ui.jquery.com)<Br>
License: MIT<Br>

## How to create translated HTML pages

You simply need to go to the translate-html/bin folder and run: <br>

./translate-html -t <br>

This will generate a set of folders, one for each available translations, <br>
ready to publish online <br>

## Translate script help

translate-html/bin$ ./translate-html --help <br>
Usage: translate-html {--extract|--translate} [options] <br>

    This script can be used to prepare translatable messages in HTML files <br>
    and expose them to translators and to subsequently use those translations <br>
    to build localized HTML files based on the original in English. <br>

    It works in one of two modes: <br>

    - Extract mode: extracts translatable strings from the file specified <br>
      in the 'po/POTFILES.in' file and puts them into a .pot file into the <br>
      'po' folder, ready to give it to translators. <br>
    - Translate mode: fetches the translations in the form of .po files in the <br>
      'po-html' folder and builds localized files based on the original. <br>
      Untranslated strings in the PO files are left as their English originals <br>
      in the generated localized files. The localized files are named <br>
        <ISO-639-2-lang-code>/<original-filename>.<original-fileext> <br>
      E.g. <br>
        en/index.html      <- original file <br>
        zh-CN/index.html   <- Simplified Chinese translation <br>

    Structure of the 'po-html' folder: <br>

      po-html/template.pot <- translation template created in extract mode <br>
      po-html/POTFILES.in  <- files to extract strings from are specified here <br>
      po-html/zh_CN.po     <- translation done by translators <br>
      po-html/ca.po        <- another translation, naming: <ISO 639-2 code>.po <br>


Options: <br>
  --version        show program's version number and exit <br>
  -h, --help       show this help message and exit <br>
  -d, --debug      Print the maximum debugging info (implies -vv) <br>
  -v, --verbose    set error_level output to warning, info, and then debug <br>
  -x, --extract    Extract mode: extract the strings from the original HTML <br>
                   file <br>
  -t, --translate  Translate mode: get the translations from PO files and <br>
                   write them to a new translated HTML file <br>
  -s, --test       Test mode: only effective in conjunction with Translate <br>
                   mode. If set, untranslatable messages are translated as <br>
                   reversed English, so that they are easy to spot. <br>

