# **Lab Report 5**
By: Sean Ting

I had a lot of fun researching different options for the grep command in Lab Report 3 so I decided I want to do the same for the find command for this lab report since the find command seems very useful.

## The Find Command

**-min/maxdepth option**

```
      [cs15lwi23aum@ieng6-206]:written_2:26$ find -maxdepth 2 -empty
      ./non-fiction/emptyfile2.txt
      ./travel_guides/emptyDirectory
      ./lab5/emptyfile.txt
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
      ./travel_guides/emptyDirectory
```

The -mindepth and -maxdepth options restrict the recursive search to a certain bound by either setting a minimum or a maximum.
The output of the list of files in the examples above is a list of files that fit the given criteria.
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
    ./travel_guides/emptyDirectory
    ./lab5
```
The -type option allows the user to find a specific type of file with the given or current directory.
For example, two that are used in the examples above are "f" for file and "d" for directory.
This can be useful if there are multiple file types in the working directory and you want to look at all of one specific type of file.




Sources (for all four command options):
[grep window command](https://amalgjose.com/2021/08/08/pipe-grep-equivalent-command-in-windows/#:~:text=The%20syntax%20of%20grep%20command%20is%20given%20below.&text=Options%20Description%20%2Dc%20%3A%20This%20prints,lines%20and%20their%20line%20numbers.)
