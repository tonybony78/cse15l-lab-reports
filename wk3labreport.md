# Week 3 Lab Report

## Understanding the *grep* Command

To preface, the commands I explain in this report all come from what I learned on this [Geeks for Geeks article.](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) and our [Week 4 Lab.](https://ucsd-cse15l-w23.github.io/week/week4/#counting-sizes-of-text-files)

### -l Command

Using the *-l* command allows users to find files that contain a certain string/pattern input given after *-l*.

'''
[cs15lwi23awo@ieng6-202]:berlitz2:421$ grep -l "Poland" *
Berlin-History.txt
Poland-History.txt
Poland-WhatToDo.txt
'''

As shown above, by searching the string "Poland" inside all the files in the current directory by typing * after, we can see that the string appears in three files.

'''
[cs15lwi23awo@ieng6-202]:berlitz2:426$ grep -l "China" Beijing-WhereToGo.txt
Beijing-WhereToGo.txt
'''

Rather than seeing which files contain a string, if we type a specific file after the string, we can see if the file actually does contain the string. Because it returns the same filename, the string must exist within that file.

### -r Command

By using the *-r* command, users are able to recursively search for a specific pattern/string within a given directory and all of its contents.

'''
[cs15lwi23awo@ieng6-202]:skill-demo1-data:446$ grep -r "FV-416"  written_2
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:Betancuria, by far the most attractive and visited inland town on the island, is an oasis of greenery on this barren island. Although the riverbed here is almost perpetually dry, the town is fortunate to have a high water table. Because of its theoretical invulnerability at the heart of the island, it was made Fuerteventura’s first capital in the early 15th century. However, in 1539 somehow the ravaging Berber pirates overcame the mountains (which still provide a difficult drive today), and destroyed the original cathedral. The present 17th-century church, Iglesia de Santa María is a splendid building and hosts many interesting treasures. Look at the unusual wooden beams between the flagstones on the floor, the wooden altar and choir, and the decorated pulpit. Adjacent to the museum is a leather factory-cum-shoe-shop, set in an atmospheric old building. Wander round this lovely little town and admire the view from across the bridge, where there is an unpretentious restaurant/bar and a gift shop. Just south of ==Betancuria== is the neat and pretty village of Pájara, but a stop at Antigua, on the other side of the mountains is in order. This is reached either by continuing on the loop past Tuineje, or backtracking from Betancuria and taking the FV-416 across the mountains. In either event, once in Antigua — the island’s capital from 1834–1835 — you can’t miss the traditional old windmill found just to the north of town, and this is your destination. Actually, the Centro de Artesania “Molino de Antigua” (Windmill Crafts Center) is much more than just that, and has something for almost everyone’s tastes. Interesting crafts and a visit inside the windmill certainly, but also ethnographic and archaeological exhibitions, modern art, an audiovisual room, rooftop view- points and an intriguing cactus garden, not to mention a nice restaurant.
'''

