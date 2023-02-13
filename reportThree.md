# CSE15L LAB REPORT 3
By Zichen Wang

## Examples of "Find" Commands
> These parts of examples were developed based on the contents from following websites:
>
> https://en.wikibooks.org/wiki/Grep, which assists in developing basic understandings
> 
> https://www.geeksforgeeks.org/grep-command-in-unixlinux/, some of whose commands are used in this report

**Settings**:
```
find written_2 > all_files.txt
grep ".txt" all_files.txt > all_texts.txt
grep "berlitz1" all_texts.txt > all_ber1.txt
```
These commands puts the text files to a single .txt file for some modifications


**Commands**:

---
-e exp : Specifies expression with this option, and can be used by adding multiple values after each -e.
This will help us reduce the operating time by adding several searches together.


``` grep -e "History" -e "Intro" all_texts.txt > e_1.txt ```
```
all_texts.txt:written_2/travel_guides/berlitz1/HistoryDublin.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryEgypt.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryFrance.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryFWI.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryGreek.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryHawaii.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryHongKong.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryIbiza.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryIndia.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryIsrael.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryIstanbul.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryItaly.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryJamaica.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryJapan.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryJerusalem.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryLasVegas.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryMadeira.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryMadrid.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryMalaysia.txt
all_texts.txt:written_2/travel_guides/berlitz1/HistoryMallorca.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroDublin.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroEdinburgh.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroEgypt.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroFrance.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroFWI.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroGreek.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroHongKong.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroIbiza.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroIndia.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroIsrael.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroIstanbul.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroItaly.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroJamaica.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroJapan.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroJerusalem.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroLakeDistrict.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroLasVegas.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroLosAngeles.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroMadeira.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroMadrid.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroMalaysia.txt
all_texts.txt:written_2/travel_guides/berlitz1/IntroMallorca.txt
all_texts.txt:written_2/travel_guides/berlitz2/Algarve-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Algarve-Intro.txt
all_texts.txt:written_2/travel_guides/berlitz2/Amsterdam-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Amsterdam-Intro.txt
all_texts.txt:written_2/travel_guides/berlitz2/Athens-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Athens-Intro.txt
all_texts.txt:written_2/travel_guides/berlitz2/Bahamas-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Bahamas-Intro.txt
all_texts.txt:written_2/travel_guides/berlitz2/Bali-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Barcelona-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Beijing-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Berlin-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Budapest-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/California-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Canada-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/CanaryIslands-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Cancun-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/China-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Costa-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/CostaBlanca-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Crete-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Cuba-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Nepal-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/NewOrleans-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Poland-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Portugal-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/PuertoRico-History.txt
all_texts.txt:written_2/travel_guides/berlitz2/Vallarta-History.txt
```

``` grep -e "China" -e "France" all_texts.txt >e_2.txt ```

```
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/IntroFrance.txt
written_2/travel_guides/berlitz1/WhatToFrance.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhatToDo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt

```
---

-v : This prints out all the lines that do not matches the pattern. 
This command can be used to facilitate the searching process by excluding unnecessary lines, or searching for a lot of files in without certain contents


``` grep -v "travel_guides" all_texts.txt > v_1.txt ```

See Output Results Below:
```
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
written_2/non-fiction/OUP/Castro/chA.txt
written_2/non-fiction/OUP/Castro/chB.txt
written_2/non-fiction/OUP/Castro/chC.txt
written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chM.txt
written_2/non-fiction/OUP/Castro/chN.txt
written_2/non-fiction/OUP/Castro/chO.txt
written_2/non-fiction/OUP/Castro/chP.txt
written_2/non-fiction/OUP/Castro/chQ.txt
written_2/non-fiction/OUP/Castro/chR.txt
written_2/non-fiction/OUP/Castro/chV.txt
written_2/non-fiction/OUP/Castro/chW.txt
written_2/non-fiction/OUP/Castro/chY.txt
written_2/non-fiction/OUP/Castro/chZ.txt
written_2/non-fiction/OUP/Fletcher/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch5.txt
written_2/non-fiction/OUP/Fletcher/ch6.txt
written_2/non-fiction/OUP/Fletcher/ch9.txt
written_2/non-fiction/OUP/Kauffman/ch1.txt
written_2/non-fiction/OUP/Kauffman/ch10.txt
written_2/non-fiction/OUP/Kauffman/ch3.txt
written_2/non-fiction/OUP/Kauffman/ch4.txt
written_2/non-fiction/OUP/Kauffman/ch5.txt
written_2/non-fiction/OUP/Kauffman/ch6.txt
written_2/non-fiction/OUP/Kauffman/ch7.txt
written_2/non-fiction/OUP/Kauffman/ch8.txt
written_2/non-fiction/OUP/Kauffman/ch9.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch3.txt
```

``` grep -v -e "Wh" -e "Intro" -e "Hand" all_ber1.txt > v_2.txt ```


See Output Results Below:
```
written_2/travel_guides/berlitz1/HistoryDublin.txt
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
written_2/travel_guides/berlitz1/HistoryEgypt.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryFWI.txt
written_2/travel_guides/berlitz1/HistoryGreek.txt
written_2/travel_guides/berlitz1/HistoryHawaii.txt
written_2/travel_guides/berlitz1/HistoryHongKong.txt
written_2/travel_guides/berlitz1/HistoryIbiza.txt
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryIsrael.txt
written_2/travel_guides/berlitz1/HistoryIstanbul.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/HistoryJamaica.txt
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz1/HistoryJerusalem.txt
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
written_2/travel_guides/berlitz1/HistoryLasVegas.txt
written_2/travel_guides/berlitz1/HistoryMadeira.txt
written_2/travel_guides/berlitz1/HistoryMadrid.txt
written_2/travel_guides/berlitz1/HistoryMalaysia.txt
written_2/travel_guides/berlitz1/HistoryMallorca.txt
written_2/travel_guides/berlitz1/JungleMalaysia.txt

```

---
-o : Print only the matched parts of a matching line, with each such part on a separate output line. 
I would personally say this part should be used in collaboration with -e to get combined results to facilitate searching
Also, it can be used to check the existance of a certain string

```grep -o "HistoryEgypt" all_texts.txt > o_1.txt```

```
HistoryEgypt
```

```grep -o "History" all_ber1.txt > o_2.txt```

```
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
History
```

---
-h : Display the matched lines, but do not display the filenames. This faciliates the searching process by only giving necessary information when a user only needs that part of line in order to do citation or paraphrazing.

```grep -h -r "Lucayans" written_2 > h_1.txt```
```
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

```grep -h -v -e "non-fiction" -e "berlitz1" all_texts.txt >h_2.txt```
```
written_2/travel_guides/berlitz2/Algarve-History.txt
written_2/travel_guides/berlitz2/Algarve-Intro.txt
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
written_2/travel_guides/berlitz2/Amsterdam-History.txt
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
written_2/travel_guides/berlitz2/Athens-History.txt
written_2/travel_guides/berlitz2/Athens-Intro.txt
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Bali-History.txt
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
written_2/travel_guides/berlitz2/Barcelona-History.txt
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
written_2/travel_guides/berlitz2/Beijing-History.txt
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/Berlin-History.txt
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
written_2/travel_guides/berlitz2/Bermuda-history.txt
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
written_2/travel_guides/berlitz2/Budapest-History.txt
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt
written_2/travel_guides/berlitz2/California-History.txt
written_2/travel_guides/berlitz2/California-WhatToDo.txt
written_2/travel_guides/berlitz2/California-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-History.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/CanaryIslands-History.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
written_2/travel_guides/berlitz2/Cancun-History.txt
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhatToDo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/Costa-History.txt
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
written_2/travel_guides/berlitz2/CostaBlanca-History.txt
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
written_2/travel_guides/berlitz2/Crete-History.txt
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
written_2/travel_guides/berlitz2/Cuba-History.txt
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt
written_2/travel_guides/berlitz2/Nepal-History.txt
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt
written_2/travel_guides/berlitz2/NewOrleans-History.txt
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
written_2/travel_guides/berlitz2/Poland-History.txt
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-History.txt
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
written_2/travel_guides/berlitz2/PuertoRico-History.txt
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
written_2/travel_guides/berlitz2/Vallarta-History.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
