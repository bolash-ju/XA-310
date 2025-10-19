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

FOREACH movie title
  SPLIT title into array of words
  IF movie has two words
    ADD to friend1 array
  ENDIF
ENDFOR
PRINT friend1 to console
PRINT friend1 to HTML

FOREACH movie title
  IF movie includes the word "in" OR "In"
    ADD movie to friend2 array
  ENDIF
ENDFOR
PRINT friend2 to console
PRINT friend2 to HTML

FOREACH movie title
  IF title ends with "Y"
    ADD movie to friends3 array
  ENDIF
ENDFOR
PRINT friend3 to console
PRINT friend3 to HTML

FOREACH movie title
  IF movie does NOT include the word "the" OR "The" OR "a" OR "A"
    ADD movie to friends4 array
  ENDIF
ENDFOR
PRINT friend4 to console
PRINT friend4 to HTML

SET count = 1
WHILE count < 4
  GET random number between 1 and 60
  GET movie at random number index of movies array
  PUSH selected movie to friend5 array
  SET count = count + 1
ENDWHILE
PRINT friend5 to console
PRINT friend5 to HTML

Links:
-----------
https://www.w3schools.com/jsref/jsref_push.asp
https://www.w3schools.com/jsref/jsref_match.asp
https://www.w3schools.com/jsref/jsref_filter.asp
https://www.w3schools.com/jsref/jsref_random.asp
https://www.rexegg.com/regex-boundaries.php#wordboundary
https://www.rajamsr.com/javascript-string-endswith/

Process & Issues Faced:
-----------
I started by drafting my pseudocode in a very basic, informal outline. Then, I opened the starter index file in Visual Studio Code and began with working on the 5th friend. I had to use w3 Schools' resources to find the JavaScript syntax that would help me choose a random number, then applied what I learned to the movie night scenario. 

Next, I worked on friends 2 and 4, because I intended to approach their code solutions in similar ways. I used string.match() to identify keywords (in, the, a), but realized that my code was finding titles that contained the keywords within other words (Zeppelin, there, about). Some searching online helped me understand how to use \b to identify word boundaries and search for instances where my keywords appeared on their own. For friend 4, I added a negation to the matching, to return titles that did not contain the keywords. 

Friend 1 was difficult to figure out. After working through different approaches in class, I learned more about using functions and returns. At one point, I tried to check my work in a browser and Chrome refused to open the HTML file. It took me a long time to figure out that a never-ending forEach loop was the culprit. I rewrote the code using a filter with split and return, and I was so excited when it finally worked!

Friend 3 gave me some trouble, too. I tried to approach it in a similar way to friend 1, by splitting each title into an array of strings in order to check whether each title's last word ends with y. I realized I was overcomplicating things and didn't need to separate each string into individual words. My final solution uses endsWith on the whole string, and it works!

I decided to add a few words of an introduction when printing each friend's list to the console log and HTML. I also joined the movie titles with commas and spaces, to make the formatting clean and consistent.
