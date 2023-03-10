# Understanding the *find* command

To start, the commands used in this report, I learned primarily from lecture, this [Geeks for Geeks](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) article, and this [Tecmint](https://www.tecmint.com/35-practical-examples-of-linux-find-command/) article.

### -empty Command

Using *-empty* gives users the ability to find any empty folders or files that exist in your current/working directory.

```
[cs15lwi23awo@ieng6-202]:written_2:506$ find -empty
[cs15lwi23awo@ieng6-202]:written_2:507$ ls
non-fiction  travel_guides
```

As seen in the code block above, I use the *-empty* command while inside the *written_2* directory, but nothing is returned, as both *non-fiction* and *travel-guides* are non-empty directories.

```
[cs15lwi23awo@ieng6-202]:written_2:509$ mkdir empty
[cs15lwi23awo@ieng6-202]:written_2:510$ ls
empty  non-fiction  travel_guides       
[cs15lwi23awo@ieng6-202]:written_2:511$ find -empty
./empty
```

However, in this example above, I make an empty directory called *empty*, call the command once more, and the path to this empty directory is returned.

### -name Command

Using the *-name* command allows users to find specific files or types of files in a given directory

```
[cs15lwi23awo@ieng6-202]:travel_guides:525$ find ./berlitz2 -name China-History.txt
./berlitz2/China-History.txt
```

In the code block above, I search for the *China-History.txt* file inside the *berlitz2* directory, which returns the relative path to the exact file.                 

```
[cs15lwi23awo@ieng6-202]:travel_guides:528$ find ./berlitz2 -name *.txt
./berlitz2/Algarve-History.txt
./berlitz2/Algarve-Intro.txt
./berlitz2/Algarve-WhatToDo.txt
./berlitz2/Algarve-WhereToGo.txt
./berlitz2/Amsterdam-History.txt
```

In this example, instead of searching for a filename, I search for *.txt* files only, by inputting * *.txt*, which returns a long list of *.txt* files, which I shortened for legibility.

### -size Command

Using the *-size* command allows users to check the memory size of files in a given range of bytes.

```
[cs15lwi23awo@ieng6-202]:berlitz2:555$ find -size +1M  
[cs15lwi23awo@ieng6-202]:berlitz2:556$ 
```

Up above, I look for files above 1 megabyte, as designated by the *1M*, however nothing is returned. This makes sense since the directory is filled with small text files.

```
[cs15lwi23awo@ieng6-202]:berlitz2:554$ find -size +100k
./Canada-WhereToGo.txt
./China-WhereToGo.txt
./Portugal-WhereToGo.txt
```

In this one though, when I search for files above 100 kilobytes, three files are returned, designating them to be above the memory range I inputted.
