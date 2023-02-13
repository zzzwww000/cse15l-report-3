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

-e exp : Specifies expression with this option, and can be used by adding multiple values after each -e.
This will help us reduce the operating time by adding several searches together.

---
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


-v : This prints out all the lines that do not matches the pattern. 
This command can be used to facilitate the searching process by excluding unnecessary lines, or searching for a lot of files in without certain contents

---
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
