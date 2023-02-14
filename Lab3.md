# Diffent Ways to Use Grep
## Purpose of this Lab
The purpose of this lab is to show the different ways of using the "grep" command. There will be four variations demonstrated with 8 examples total.
## Example #1
The first command that will be showcased is `grep -i`.
> The information about this command was obtained from ChatGPT.

So what does this command do exactly? This command searches through files the same way grep does, however, using "-i" allows the search to get rid of case sensitivity. Normally, grep is case-sensitive and relies on your exact input to search through files.
- The following command was ran: `grep -i "berlin" grep-results.txt > grepBerlin.txt` , and the output was as follows:
```
written_2/travel_guides/berlitz2/Berlin-History.txt
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
```
- The following command was ran: `grep -i "Italy" grep-results.txt > grepItaly.txt` , and the output was as follows:
```
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/IntroItaly.txt
written_2/travel_guides/berlitz1/WhatToItaly.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
```
## Example #2
> The information about this command was obtained from ChatGPT.

The second command that will be showcased is `grep -o`.
What does this command do? This command searches for the string inputted and returns only the string instead of the whole line. For example, when using `grep -i`, the whole file location is returned, however, `grep -o` just returns the string that was being searched.
- The following command was ran: `grep -o "Berlin" grep-results.txt > grepBerlin2.txt` , and the output was as follows: 
```
Berlin
Berlin
Berlin
```
- The following command was ran: `grep -o "Italy" grep-results.txt > grepItaly2.txt` , and the output was as follows:
```
Italy
Italy
Italy
Italy
```
## Example #3
> The information about this command was obtained from ChatGPT.

The third command that will be showcased is `grep -n`.
What does this command do? This command prints out the lines in which the string that is being searched for is located. Not only that, but it also returns the exact file location of the string inputted.
- The following command was ran: `grep -n "Berlin" grep-results.txt > grepBerlin3.txt` , and the output was as follows:
```
172:written_2/travel_guides/berlitz2/Berlin-History.txt
173:written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
174:written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
```
- The following command was ran: `grep -n "Italy" grep-results.txt > grepItaly3.txt` , and the output was as follows:
```
72:written_2/travel_guides/berlitz1/HistoryItaly.txt
93:written_2/travel_guides/berlitz1/IntroItaly.txt
117:written_2/travel_guides/berlitz1/WhatToItaly.txt
138:written_2/travel_guides/berlitz1/WhereToItaly.txt
```
## Example #4
> The information about this command was obtained from ChatGPT.

The fourth and final command that will be showcased is `grep -v`.
What does this command do? This command looks for the opposite of what is inputted. To be more clear, it excludes the string inputted and looks for the files or information not containing the input.
- The following command was ran: `grep -v "Berlin" grep-results.txt > grepBerlin4.txt` , and the output was as follows:
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
...
```
> The output shown above is not what was printed out in its entirety, I chose a small portion since the output was too big.
- The following command was ran: `grep -v "Italy" grep-results.txt > grepItaly4.txt` , and the output was as follows: 
```
written_2/travel_guides/berlitz1/IntroMadrid.txt
written_2/travel_guides/berlitz1/IntroMalaysia.txt
written_2/travel_guides/berlitz1/IntroMallorca.txt
written_2/travel_guides/berlitz1/JungleMalaysia.txt
written_2/travel_guides/berlitz1/WhatToDublin.txt
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt
written_2/travel_guides/berlitz1/WhatToEgypt.txt
written_2/travel_guides/berlitz1/WhatToFrance.txt
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz1/WhatToGreek.txt
written_2/travel_guides/berlitz1/WhatToHawaii.txt
...
```
> The output shown above is not what was printed out in its entirety, I chose a small portion since the output was too big.
