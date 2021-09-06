# Warwick Folk Band Folder

![](https://www.warwicksu.com/asset/Organisation/4113/Warwick%20Folk%20Logo.PNG?thumbnail_width=300&thumbnail_height=300&resize_type=ResizeFitAllFill)

Welcome to the Warwick Folk Github repository!

The standard means of sharing and scoring Folk music is with the use of a markup language called 'abc'. These files can be edited, compiled, viewed, exported via many different tools the most notable of which are listed bellow:
- [EasyABC](https://www.nilsliberg.se/ksp/easyabc/) - an open-source Python programme with an easy to use GUI (most user-friendly)
- [abc2svg](http://moinejf.free.fr/js/edit-1.xhtml) - an online tool that is good for quick compiling of abc files to svg which can then be exported via the browser (***warning*** for large complex files, such as the Band Folder, this tool is not recommended as some of the formatting features whithin the abc markup e.g. `%%newpage` cease to function)
- [abcm2ps](https://github.com/leesavide/abcm2ps) - a command-line tool on which EasyABC is based upon that compiles abc to PostScript (which can then be exported as PDF). This is the most powerful abc compiling tool, however, it does require you to be comfortable within the command-line (if you're up for it, this is the ***best tool***)
- abc2abc - this is a command-line abc checker/re-formatter/transposer

## Installing `abcm2ps`
### On Linux or MacOS
This is way doesn't install it on your system (portable).
1. `cd ~/Downloads`
2. `git clone https://github.com/leesavide/abcm2ps.git`
3. `cd abcm2ps`
4. `./configure`
5. `make`
Done. If successful `abcm2ps` should be compiled and executable on your system.
Remember, in this case it is portable so you have to be in the directory where it has been compiled to execute.

## Using abcm2ps
1. `cd abc/`
2. `abcm2ps <FILE_NAME>`
The resulting PostScript file will be compiled in the same directory with the default filename `Out.ps`.

With the Band Folders, a lot of pre-formatting within the abc file has already been done - so the standard compiled output from `abcm2ps` should work. 

## Converting from PostScript to PDF
There are many tools out there, if you are on MacOS, Preview should function perfectly fine, alternatively, you can use [ps2pdf Online](https://www.ps2pdf.com/convert-ps-to-pdf).

## Currently Testing
`abc2abc <FILE_NAME> -useclef bass > out.ps`
Not working for the moment
This would be better as it would allow the maintenance of a single Band Folder abc file and not the each folder in a different clef.