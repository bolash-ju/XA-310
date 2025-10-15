Please write your pseudocode for each challenge below; also include any
write-up of your process, issues you faced, any tutorials or resources you
used, and so on.

----------

Friend 1 will only watch movies with two-word titles.
Friend 2 will only watch movies that happen "in" some place or concept.
Friend 3 only will only watch movies that end with a “Y”.
Friend 4 flatly refuses to watch any movie where the title starts with the word "The" or "A".
Friend 5 only wants a list of three movies, but wants them selected randomly.

Pseudocode:
-----------
BEGIN movie night

PRINT introduction to Friend 1's list
SEARCH list for movies that have two-word titles
CREATE an array of the two-word titles
PRINT two-word titles to console

PRINT introduction to Friend 2's list
SEARCH list for movies that have "in" in the title
CREATE an array of the "in" titles
PRINT "in" titles to console

PRINT introduction to Friend 3's list
SEARCH list for movies that end with "Y"
CREATE an array of the "Y"-ending titles
PRINT "Y"-ending titles to console

PRINT introduction to Friend 4's list
SEARCH list for movies that start with "The" OR "A"
CREATE an array of the "The" AND "A"-starting titles
PRINT "The" and "A"-starting titles to console

WHILE less than 3 movies have been printed
  SELECT random movie from movies list
  PRINT random movie's title
  INCREASE count by 1
ENDWHILE


Links:
-----------
https://www.w3schools.com/jsref/jsref_push.asp
https://www.w3schools.com/jsref/jsref_match.asp
