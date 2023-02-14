# Diffent Ways to Use Grep
## Purpose of this Lab
The purpose of this lab is to show the different ways of using the "grep" command. There will be four variations demonstrated with 8 examples total.
## Example #1
The first command that will be showcased is `grep -i`.
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
The second command that will be showcased is `grep 