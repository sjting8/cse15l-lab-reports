# **Lab Report 5**
By: Sean Ting

I had a lot of fun researching different options for the grep command in Lab Report 3 so I decided I want to do the same for the find command for this lab report since the find command seems very useful.

## The Find Command

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


**/c option**

*cd into written_2/travel_guides/berlitz2*

```
  grep -c "Lucayans" Bahamas-History.txt
  
2
```

```
  grep -c "Carrer dels Escudellers" Barcelona-WhereToGo.txt
  
1
```

Prints only a count of the lines that match a pattern.
This option may be useful to check the existence of a string after redirecting a stdout to a file. (If "tests failed:" returns 0 then they all passed).

**/n option**

```
  grep -n "Lucayanas" Bahamas-History.txt
  
6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```


```
  grep -n "Carrer dels Escudellers" Barcelona-WhereToGo.txt
  
20:Carrer dels Escudellers, a busy pedestrian street on the other side of the Rambla, is the gateway to a district of cabarets, bars, flamenco shows, and restaurants, and the delights of the Gothic Quarter. Nearer the port, a passage leads to the Museu de Cera (Wax Museum), a tourist trap with a collection of some three hundred realistic wax effigies. The Rambla ends at the broad open space facing the Monument à Colom, a statue honoring the discoverer Christopher Columbus (Colom in Catalan) that can be climbed for good views of the port. Poor Columbus is supposed to be indicating the way to the riches of the New World, but he’s actually pointing at Mallorca or perhaps North Africa. Just beyond the statue is Barcelona’s newly revitalized waterfront.
```

Displays the matched lines and their line numbers.
This option may be useful if the user needs to find exactly where in a file a line appears. If the file is very big and they want to search for a specific section that contains a unique string pattern, this could be useful.

**/i option**

```
  grep -A1 "Lucayans" Bahamas-History.txt
  
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
English sea captains also came to know the beautiful but deserted Bahamian islands during the 17th century. England’s first formal move was on 30 October 1629, when Charles I granted the Bahamas and a chunk of the American south to his Attorney General, Sir Robert Health. But nothing came of that, nor of a rival French move in 1633 when Cardinal Richelieu, the 17th-century French statesman, tried claiming the islands for France.
```

```
  grep -A1 "Carrer dels Escudellers" Barcelona-WhereToGo.txt
  
Carrer dels Escudellers, a busy pedestrian street on the other side of the Rambla, is the gateway to a district of cabarets, bars, flamenco shows, and restaurants, and the delights of the Gothic Quarter. Nearer the port, a passage leads to the Museu de Cera (Wax Museum), a tourist trap with a collection of some three hundred realistic wax effigies. The Rambla ends at the broad open space facing the Monument à Colom, a statue honoring the discoverer Christopher Columbus (Colom in Catalan) that can be climbed for good views of the port. Poor Columbus is supposed to be indicating the way to the riches of the New World, but he’s actually pointing at Mallorca or perhaps North Africa. Just beyond the statue is Barcelona’s newly revitalized waterfront.
Barri GÒtic
```

Prints searched line and n lines after the result. (1 line in these examples because of A1)
Could be useful if the user wants to search for a method and they would input the method header and n lines to see the method.

Sources (for all four command options):
[grep window command](https://amalgjose.com/2021/08/08/pipe-grep-equivalent-command-in-windows/#:~:text=The%20syntax%20of%20grep%20command%20is%20given%20below.&text=Options%20Description%20%2Dc%20%3A%20This%20prints,lines%20and%20their%20line%20numbers.)
