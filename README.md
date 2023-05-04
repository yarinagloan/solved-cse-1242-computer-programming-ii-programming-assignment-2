Download Link: https://assignmentchef.com/product/solved-cse-1242-computer-programming-ii-programming-assignment-2
<br>
In this homework, you will implement your own <strong>String</strong> data type using <em>C</em> <em>structs</em>. Each <strong>String</strong>  is represented by a sequence of characters and should have a length property that shows the number of characters stored in that string (excluding the <em>null</em> character). Suppose that this <em>struct</em> can be used to represent only the strings with less than 50 characters. You should implement the following functions to operate on your <strong>String</strong> data type.




<ul>

 <li><strong>int charAt(String *s, int index) </strong></li>

</ul>

o This function should return the character stored at the location <strong>index</strong>. If there is no such an index (either negative index value, or greater or equal to the length of the string), then return -1.

<strong> </strong>

<ul>

 <li><strong>String *concat(String *s1, String *s2) </strong></li>

</ul>

o This function should concatenate the string pointed by s2 to the end of the string pointed by s1, and return the address of the new string. You cannot use <em>strcat</em> or <em>strncat</em> functions of <em>string.h</em> library of C in that function.

<strong> </strong>

<ul>

 <li><strong>unsigned int strSearch(String *s1, String *s2) </strong></li>

</ul>

o This function should scan the first string and return the length of initial segments that contain only the characters of the second string. If there is no such a segment, return -1. You cannot use <em>strspn</em> or <em>strcspn</em> functions of <em>string.h</em> library of C in that function.

<strong> </strong>

<ul>

 <li><strong>unsigned int findScore(String *s1) </strong></li>

</ul>

o This function should return a score by checking the given String. To calculate the score, you will use the following table:




<strong><u>Letter</u></strong>                           <strong><u>Value</u></strong>

A, E, I, O, U, L, N, R, S, T       1

D, G                               2

B, C, M, P                         3

F, H, V, W, Y                      4

K                                  5

J, X                               8

Q, Z                               10




o For example, the String is “<strong>hello</strong>” should be scored as 4+1+2∗1+1=8.







<ul>

 <li>Your program should continue to execute until the given word is either “<strong>exit</strong>” or “<strong>quit</strong>”. If the given word is “<strong>exit</strong>” or “<strong>quit</strong>”, your program should terminate. If the given word is “<strong>stat</strong>”, your program should print a two-line statistical report: the first line prints <em>the total number of words the user has entered</em>, and the second line prints <em>the total number of alphabetic letters</em> the user has entered. Note that we only count the 26 letters in the alphabet (either lower case or upper case). For example, if a user has entered the following string, i.e. “We love CSE1142 course a lot!!”, the following should be printed to screen after the user types “<strong>stat</strong>”:</li>

</ul>




The number of words: 6

The number of alphabetic letters: 19




<ul>

 <li>If the given word is not “<strong>stat</strong>”, “<strong>exit</strong>” or “<strong>quit</strong>”, then your program will continue to execute based on the user’s selection.</li>

</ul>




<ul>

 <li>You have to perform File I/O operations in this homework.

  <ul>

   <li>All the user options will be given using an input file that is passed to your program using command line arguments.</li>

   <li>All the outputs of your program must be printed to an output file that is passed to your program using command line arguments.</li>

   <li>For example, suppose that “txt” and “output.txt” are given to your program as command line arguments.</li>

   <li>Each line of the input file contains the related operations followed by the specified options.</li>

   <li>For example, if a line is as follows:</li>

  </ul></li>

</ul>




heLLo world:1,6




Here, o “heLLo world” is the given string that we use.  o <sub>1</sub> represents that the operation is finding a char o <sub>6</sub> represents the index for the searched char.

<ul>

 <li>The output for this option should be W, which will be added to a given output file.</li>

</ul>

<ul>

 <li>The valid options given as the second argument (given after colon <strong>:</strong> ) can be o <sub>1</sub> for finding a char in the given index, o 2 for string concatenation, o 3 for string search, o 4 for finding the string score.</li>

</ul>




<ul>

 <li>If the required operation needs a third option (given after comma <strong>,</strong> ) it can be o An index for finding a char in the given string, o A second string for string concatenation, o A second string for string search.</li>

</ul>




<ul>

 <li>An operation may not require a third option (For example, finding the string score), in such a case, you can directly find the score of the string.</li>

</ul>




<ul>

 <li>Suppose that the input file contains the following lines:</li>

</ul>




heLLo world:1,6

Welcome to C:2,programming!

welcome to marmara university!:3,mar We love CSE!!:4 stat exit

<ul>

 <li>Then, the output file should contain the output of each operation as follows:</li>

</ul>




W

Welcome to C programming!

7

17

The number of words: 14

The number of alphabetic letters: 70

Program ends. ByE