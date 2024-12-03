# How to print from the Mac/Linux command line

I just learned about the `cal` command, which displays a calendar in the command line. I wanted to print one to tape to my desk (do `cal -h` to remove highlighting of today's date). After saving the text to a file (`cal -h > cal.txt`), what to do next?

## tl;dr
Do `lp cal.txt`.

## Much more on command line printing ([1])

- Is `lp` available? Do `which lp` to make sure it is in your search path.

- Check the status of your printers:
```sh
lpstat -p -d
```
The `-p` option provides the printer descriptions; the `-d` option indicates the default printer.

- For a long list of printer options: `lpoptions`
This may be hard to read, so we can replace spaces by newlines, and use more:
```sh
lpoptions | tr " " `\n` | more
```
(`tr` stands for "translate", and is useful for basic replacing as well as more sophisticated transformations.)

And if there are multiple printers, you can specify one like "LaserJet" by using `lpoptions -p LaserJet`.

- For drivers, IP address, and related information: `lpinfo -v`

## Using the `lp` command

We already showed how to do basic printing: `lp cal.txt`

- To view the print queue, do `lpq`

- To print multiple copies, do `lp -n 10 cal.txt`

- To cancel a print job, do `cancel 229`

- To print double-sided, do `lp -o sides=two-sided-long-edge cal.txt`

- The `-o` is for options, and here are some more from the man page:

-- `-o media=size`: Most printers support at least "a4", "letter", and "legal"

-- `-o number-up={2|4|6|9|16}`: prints that many document pages on each output page

-- `-o orientation-requested={4|5|6}`: 4, landscape 90 deg ccw; 5, landscape 90 deg cw; 6, reverse portrait (180 deg) 

-- `-o print-quality={3|4|5}`: 3, draft; 4, normal; 5, best

-- `-o sides={one-sided|two-sided-long-edge|two-sided-short-edge}`

- To change the option settings: `lpoptions -o sides=two-sided-short-edge`

- Also, apparently there is an easier landscape mode: `lp -o landscape penguin.jpg`

- To print files to the named printer: `-d destination`

- To send an email when the job is completed: `-m`

- To specify when the job should be printed: `-H` with various options; see man page

- To specify which pages to print: `-P page-list` e.g., "1,3-5,16"

[1]: https://www.networkworld.com/article/967157/printing-from-the-linux-command-line.html