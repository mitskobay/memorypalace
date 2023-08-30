# grep cheatsheet

grep is used to search for a string inside files.
It stands for **G**lobal **R**egular **E**xpression **P**rint.
[man page]
## To search in one file, several files, or a whole directory
```sh
grep string filename
grep string filename1 filename2 filename3
grep string *
```
* Every line of the file(s) containing the string will be displayed.
* In the case of multiple files, the lines will be returned with respective filenames.
* Use quotation marks around string when it contains non-alphanumeric characters.

## Useful Options
| option | description |
| ------ | ----------- |
| -r | searches subdirectories |
| -n | displays line numbers |
| -w | matches whole words only |
| -i | ignores case |
| -v | searches for lines that do **not** include the string |
| -x | shows only whole lines that exactly match the string |
| -l | prints only the filenames of matches |
| -c | prints a count of matches per file |
| -A 3 | shows also 3 lines after matching line |
| -B 3 | shows also 3 lines before matching line |
| -C 3 | shows also 3 lines before and after matching line |
| -m2 | limits number of matching lines shown per file to 2 |
| --color | adds color coding |

> Thanks to [phoenixnap.com] for much of this info.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [man page]: <https://man7.org/linux/man-pages/man1/grep.1.html>
   [phoenixmap.com]: <https://phoenixnap.com/kb/grep-command-linux-unix-examples>

