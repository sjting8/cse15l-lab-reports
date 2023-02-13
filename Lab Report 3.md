# **Lab Report 3**
By: Sean Ting

## The Grep Command

**-r option**

```
  grep -r "Lucayans" written_2
  
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

```
  grep -r "Carrer dels Escudellers" written_2
  
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:Carrer dels Escudellers, a busy pedestrian street on the other side of the Rambla, is the gateway to a district of cabarets, bars, flamenco shows, and restaurants, and the delights of the Gothic Quarter. Nearer the port, a passage leads to the Museu de Cera (Wax Museum), a tourist trap with a collection of some three hundred realistic wax effigies. The Rambla ends at the broad open space facing the Monument à Colom, a statue honoring the discoverer Christopher Columbus (Colom in Catalan) that can be climbed for good views of the port. Poor Columbus is supposed to be indicating the way to the riches of the New World, but he’s actually pointing at Mallorca or perhaps North Africa. Just beyond the statue is Barcelona’s newly revitalized waterfront.
```
   
Recursively reads all files under each directory and returns where the command line pattern is found. In this case, it searched for the string pattern in written_2.



**-c option**

**-A n option**

**-B n option**

https://amalgjose.com/2021/08/08/pipe-grep-equivalent-command-in-windows/#:~:text=The%20syntax%20of%20grep%20command%20is%20given%20below.&text=Options%20Description%20%2Dc%20%3A%20This%20prints,lines%20and%20their%20line%20numbers.
