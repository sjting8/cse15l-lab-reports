# **Lab Report 5**
By: Sean Ting

I had a lot of fun researching different options for the grep command in Lab Report 3 so I decided I want to do the same for the find command for this lab report since the find command seems very useful.

## The Find Command

**-empty option**

```
    [cs15lwi23aum@ieng6-206]:written_2:24$ find -empty
      ./lab5/emptytxt.txt
```
```
    [cs15lwi23aum@ieng6-206]:written_2:25$ find -empty
    ./non-fiction/emptytxt1.txt
    ./travel_guides/emptyD
    ./lab5/emptyfile.txt
```
For the sake of demonstrating this option, I have added some empty files to some of the directories and an empty directory.
The option -empty is recursively searching through all files and folders within ./written2 and is returning anything that is empty (file or directory).
This option can be useful if you want to search for unused files and directories to either fill or delete.
 


**-min/maxdepth option**

```
      [cs15lwi23aum@ieng6-206]:written_2:26$ find -maxdepth 2 -empty
      ./non-fiction/emptytxt1.txt
      ./travel_guides/emptyD
      ./lab5/emptytxt.txt
```
```
      [cs15lwi23aum@ieng6-206]:written_2:27$ find -mindepth 2 -type d
      ./non-fiction/OUP
      ./non-fiction/OUP/Abernathy
      ./non-fiction/OUP/Berk
      ./non-fiction/OUP/Castro
      ./non-fiction/OUP/Fletcher
      ./non-fiction/OUP/Kauffman
      ./non-fiction/OUP/Rybczynski
      ./travel_guides/berlitz1
      ./travel_guides/berlitz2
      ./travel_guides/emptyD
```

The -mindepth and -maxdepth options restrict the recursive search to a certain bound by either setting a minimum or a maximum.
The output of the list of files in the examples above is a list of files that fit the bound.
This can be useful if you want to exclude shallow files or you only want files that a few branches down. 


**-type option**

```
    [cs15lwi23aum@ieng6-206]:written_2:28$ find -mindepth 4 -type f
    ./non-fiction/OUP/Abernathy/ch1.txt
    ./non-fiction/OUP/Abernathy/ch14.txt
    ./non-fiction/OUP/Abernathy/ch15.txt
    ./non-fiction/OUP/Abernathy/ch2.txt
    ./non-fiction/OUP/Abernathy/ch3.txt
    ./non-fiction/OUP/Abernathy/ch6.txt
    ./non-fiction/OUP/Abernathy/ch7.txt
    ./non-fiction/OUP/Abernathy/ch8.txt
    ./non-fiction/OUP/Abernathy/ch9.txt
    ./non-fiction/OUP/Berk/CH4.txt
    ./non-fiction/OUP/Berk/ch1.txt
    ./non-fiction/OUP/Berk/ch2.txt
    ./non-fiction/OUP/Berk/ch7.txt
    ./non-fiction/OUP/Castro/chA.txt
    ./non-fiction/OUP/Castro/chB.txt
    ./non-fiction/OUP/Castro/chC.txt
    ./non-fiction/OUP/Castro/chL.txt
    ./non-fiction/OUP/Castro/chM.txt
    ./non-fiction/OUP/Castro/chN.txt
    ./non-fiction/OUP/Castro/chO.txt
    ./non-fiction/OUP/Castro/chP.txt
    ./non-fiction/OUP/Castro/chQ.txt
    ./non-fiction/OUP/Castro/chR.txt
    ./non-fiction/OUP/Castro/chV.txt
    ./non-fiction/OUP/Castro/chW.txt
    ./non-fiction/OUP/Castro/chY.txt
    ./non-fiction/OUP/Castro/chZ.txt
    ./non-fiction/OUP/Fletcher/ch1.txt
    ./non-fiction/OUP/Fletcher/ch10.txt
    ./non-fiction/OUP/Fletcher/ch2.txt
    ./non-fiction/OUP/Fletcher/ch5.txt
    ./non-fiction/OUP/Fletcher/ch6.txt
    ./non-fiction/OUP/Fletcher/ch9.txt
    ./non-fiction/OUP/Kauffman/ch1.txt
    ./non-fiction/OUP/Kauffman/ch10.txt
    ./non-fiction/OUP/Kauffman/ch3.txt
    ./non-fiction/OUP/Kauffman/ch4.txt
    ./non-fiction/OUP/Kauffman/ch5.txt
    ./non-fiction/OUP/Kauffman/ch6.txt
    ./non-fiction/OUP/Kauffman/ch7.txt
    ./non-fiction/OUP/Kauffman/ch8.txt
    ./non-fiction/OUP/Kauffman/ch9.txt
    ./non-fiction/OUP/Rybczynski/ch1.txt
    ./non-fiction/OUP/Rybczynski/ch2.txt
    ./non-fiction/OUP/Rybczynski/ch3.txt
```
```
    [cs15lwi23aum@ieng6-206]:written_2:29$ find -type d
    .
    ./non-fiction
    ./non-fiction/OUP
    ./non-fiction/OUP/Abernathy
    ./non-fiction/OUP/Berk
    ./non-fiction/OUP/Castro
    ./non-fiction/OUP/Fletcher
    ./non-fiction/OUP/Kauffman
    ./non-fiction/OUP/Rybczynski
    ./travel_guides
    ./travel_guides/berlitz1
    ./travel_guides/berlitz2
    ./travel_guides/emptyD
    ./lab5
```
The -type option allows the user to find a specific type of file with the given or current directory.
For example, two that are used in the examples above are "f" for file and "d" for directory.
This can be useful if there are multiple file types in the working directory and you want to look at all of one specific type of file.

**-mmin option**

```
      [cs15lwi23aum@ieng6-206]:written_2:35$ find -mmin -10
      ./non-fiction/OUP/Kauffman
      ./non-fiction/OUP/Kauffman/chQ.txt
      ./non-fiction/emptytxt1.txt
      ./travel_guides/berlitz2/Bahamas-WhatToDo.txt
      ./travel_guides/berlitz2/Poland-History.txt
      ./lab5
      ./lab5/emptytxt.txt
```
```
      [cs15lwi23aum@ieng6-206]:written_2:40$ find -maxdepth 2 -mmin +20
      ./non-fiction
      ./non-fiction/OUP
      ./travel_guides
      ./travel_guides/emptyD
```
The -mmin option finds all files/directories that have been modified within the given time frame.
The number given after the -mmin option is the number of minutes in the time frame.
Adding the +/- modifier gives the command decides whether to include files that have been changed after or before that many minutes, + being after and - being before. For the sake of providing these examples, I have modifed specific files in the last 10 minutes and they are outputted in the first example and the same for the files in the second example over 20 minutes ago.
This can be useful if you are working on a shared directory and you want to know which files have been modified recently or which ones have not been.


Sources (for all four command options):
[find command](https://man7.org/linux/man-pages/man1/find.1.html)
