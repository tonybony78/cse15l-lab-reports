# Week 3 Lab Report

## Understanding the *grep* Command

To preface, the commands I explain in this report all come from what I learned on this [Geeks for Geeks article](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) and our [Week 4 Lab.](https://ucsd-cse15l-w23.github.io/week/week4/#counting-sizes-of-text-files)

### -l Command

Using the *-l* command allows users to find files that contain a certain string/pattern input given after *-l*.

```
[cs15lwi23awo@ieng6-202]:berlitz2:421$ grep -l "Poland" *
Berlin-History.txt
Poland-History.txt
Poland-WhatToDo.txt
```

As shown above, by searching the string "Poland" inside all the files in the current directory by typing * after, we can see that the string appears in three files.

```
[cs15lwi23awo@ieng6-202]:berlitz2:426$ grep -l "China" Beijing-WhereToGo.txt
Beijing-WhereToGo.txt
```

Rather than seeing which files contain a string, if we type a specific file after the string, we can see if the file actually does contain the string. Because it returns the same filename, the string must exist within that file.

### -r Command

By using the *-r* command, users are able to recursively search for a specific pattern/string within a given directory and all of its contents.

```
[cs15lwi23awo@ieng6-202]:skill-demo1-data:446$ grep -r "FV-416"  written_2
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:...FV-416 across the mountains. In either event, once in Antigua — the island’s capital from 1834–1835 — you can’t miss the traditional old windmill found just to the north of town, and this is your destination...
```

Here in this block, I recursively searched for the string "FV-416" within the *written_2* directory, which returned the path, file, and text passage that contains that specific string. One side note, the passage that was returned from the command I ran above was originally much longer, thus the use of *...*.

```
[cs15lwi23awo@ieng6-202]:berlitz2:454$ grep -rl "nudists"
Canada-WhereToGo.txt
CanaryIslands-WhereToGo.txt
```

Interestingly, in the block above, I combined both *-r* and *-l* to recursively search through the current directory and return only the filenames that contain the string input.

### -w Command

With the *-w* command, users are able to find whole words/strings in specific files, as opposed to the previous commands, which find every instance of a string, even if it is part of another string/word.

```
[cs15lwi23awo@ieng6-202]:berlitz2:455$ grep -w "dry" California-History.txt
...dry land, or perhaps covered in ice. In the succeeding centuries, their descendants continued to push south and east, and eventually spread out to people the whole of the continent from Alaska to Patagonia...
```

In the block above, I ran the command to search for the word "dry" within the *California-History.txt* file, which returned the passage that contained the whole word by itself. Once again, the passage that was returned from the command I ran above was originally much longer, thus the use of *...*.

```
[cs15lwi23awo@ieng6-202]:written_2:462$ grep -rlw "Poland" travel_guides/
travel_guides/berlitz1/IntroJerusalem.txt
travel_guides/berlitz1/WhereToFrance.txt
travel_guides/berlitz2/Berlin-History.txt
travel_guides/berlitz2/Poland-History.txt
travel_guides/berlitz2/Poland-WhatToDo.txt
```

Looking at this block, I combined the three commands I have explained in order to recursively search through the *travel_guides* directory to see which files contain the whole string "Poland." As a result, the names of each file that do contain the string are returned.

### -n Command

Using the *-n* command gives users the ability to find both the line and line number in which a given string is found.

```
[cs15lwi23awo@ieng6-202]:travel_guides:468$ grep -n "Friedrich der" berlitz2/Berlin-History.txt
15:Friedrich der Große (Frederick the Great, 1740–1786), King of (not just in) Prussia, took his realm to the forefront of European politics and had little time for Berlin...
```

In this block, I used *-n* to find the line and line number in which the string "Friedrich der" can be found within the *Berlin-History.txt* file. As we can see, the string can be found in line 15 of the file. Again, same side note as before with the *...*.

```
[cs15lwi23awo@ieng6-202]:travel_guides:477$ grep -rwn "Lucayans"  berlitz2
berlitz2/Bahamas-History.txt:6:We know them today as the Lucayans...
berlitz2/Bahamas-History.txt:7:As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean...
```

Now, after understanding all four of these commands, we are able to put a few together and put it into use. By running this command here, I recursively search the *berlitz2* directory for files that contain the whole string "Lucayans," as well as the line and line number in which it can be found.
