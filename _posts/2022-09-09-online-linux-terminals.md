This became my favourite  [JSLinux](https://bellard.org/jslinux/vm.html?cpu=riscv64&url=fedora33-riscv.cfg&mem=256) sath/sathvik  [Fedora]
```
vflogin <username>
password: <pwd>
```

[webminal](https://www.webminal.org/) account with persistent storage across logins

> Favourite Guide [Linux-bash](https://ss64.com/bash/)

## Get These

`alias` vs `export` vs `variables` vs `functions`

In the variable form, it is expanded and evaluated. Ref via $

alias form, only expanded if it is the first word. Ref via name directly

## Watch out

`bc`	Arbitrary precision calculator language

`bzip2` `gzip` `tar`

`cal` calendar

`cat` Concatenate and print (display) the content of files

`cmp` Compare two files

`cp` copy [`cp -iv` -interactive(overwrite case) -verbose] [-s symbolic-link] [-R recursive] [-f force_overwrite] [-b backup existing file as file~ before overwriting] [-p preserve_attributes like:timestamp, author ...] [-a archive]

`csplit` split file by line no. [-f prefix_part_names]

`date`	Display or change the date & time

`df`	Display free disk space

`diff`	Display the differences between two files

`echo`

`egrep` `fgrep`  `grep`

`expr`

`file`

`find` ```find . -maxdepth 1 -type f -iname '*.SH' ! -iname 'c*'```

`grep`
```bash
grep [-w whole word] [-i ignore_cases] [-r include_subdirs] [-v lines_not_contains] [-x exact_entire_line] [-l files] [-c count] [-B -A n linesBefore and After match] [-n line_no.] [-m n limit_match] <pattern> <files>
```


`head` 
```bash
head [-LINES_FROM_BEGINNING] [-n output_first_n_lines] [-v verbose_filename_header] <file>

tail [-n last_n_lines] <file>  
```

`history` command history [CTRL+r reverse command search]

`less` better than `more`

`ls` 
```bash
# list dirs
ls -d */ 

# last modified time
ls -t

# list files including in subdirs
ls -R 
ls *

# list all (including starting from .)
ls -a

# sort by file extension
ls -X
```

`mkdir` 

`mv -iv`

`paste`

`ping`

`rm -iv`

`scp` copies files between hosts on a network

`sed` stream editor

`sleep` [NUMBER [smhd]]...

`sort`

`source`

`ssh`

`tar` tape archive 
```bash
# -create -verbose -z zipped_compress -filename -x Xtract -t list_archive_content -r add_file_to_archive
tar -cvf file.tar <req_files_dirs>  
tar -cvfz file.tar.gz <files>
```

`tee` T shaped operation
```bash
wc -l file.txt | tee -a capture.txt
tee passes the piped content(line count) to capture.txt (here append mode)(create capture if not exist)
```
`touch` change file timestamps or create empty file if not exist

`type` describe cmd

`uname` print sys-info (os, kernel, machine-hardware...)

`watch`

`yes <text>`  	Print a string until interrupted ( forever until killed ) (100% processor usage. Only for testing purposes)
```bash
yes Line OK. | head -10000 > file.txt
```



## Note

```bash
# Ok
cat file.txt | grep <keyword> 
# Better
grep <keyword> file.txt
```

```bash
cat [-n <numbered_lines>] [-b <number_only_nonblank_lines>]
```


A symlink (also called a symbolic link) is a type of file in Linux that points to another file or a folder on your computer. 

> Symlinks are similar to shortcuts in Windows.

mkdir: cannot create directory ‘tdir’: File exists

```bash
# get empty dirs
find . -type d -empty
```
```bash
^ --> ctrl
^c cancel current command (even if running)
^u erase current typed command
^k erase cmd after the cursor
^y getback last erased command
^l clear screen (not a cmd found in history but functionally equivalent to clear cmd)
^r Search command in history
works: Home_button(^a) End_button (^e)




