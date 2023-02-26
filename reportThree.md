# CSE15L LAB REPORT 3
By Zichen Wang

## Examples of "Find" Commands
> These parts of examples were developed based on the contents from following websites:
>
> [wikibooks](https://en.wikibooks.org/wiki/Grep), which assists in developing basic understandings
> 
> [geeksforgeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/), some of whose commands are used in this report

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


``` grep -e "Italy" -e "India" all_texts.txt > e_1.txt ```
```
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/IntroIndia.txt
written_2/travel_guides/berlitz1/IntroItaly.txt
written_2/travel_guides/berlitz1/WhatToIndia.txt
written_2/travel_guides/berlitz1/WhatToItaly.txt
written_2/travel_guides/berlitz1/WhereToIndia.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
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


``` grep -ve "travel_guides" -e "Castro" -e "Abernathy" -e "Fletcher" all_texts.txt> v_1.txt ```

See Output Results Below:
```
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
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

``` grep -v "Kauffman" v_1.txt > v_2.txt ```


See Output Results Below:
```
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch3.txt

```

---
-o : Print only the matched parts of a matching line, with each such part on a separate output line. 
I would personally say this part should be used in collaboration with -e to get combined results to facilitate searching
Also, it can be used to check the existance of a certain string

```grep -o "HistoryEgypt" all_texts.txt > o_1.txt```

```
HistoryEgypt
```

```grep -o "Mallorca" all_ber1.txt > o_2.txt```

```
Mallorca
Mallorca
Mallorca
Mallorca
Mallorca
```

---
-h : Display the matched lines, but do not display the filenames. This faciliates the searching process by only giving necessary information when a user only needs that part of line in order to do citation or paraphrazing.

```grep -h -r "Lucayans" written_2 > h_1.txt```
```
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

```grep -h "Bahamas-Intro" all_texts.txt >h_2.txt```
```
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
```
