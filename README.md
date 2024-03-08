# Interpreter Demo

The source code constitutes an interpreter tailored for a specialized language intended for text file manipulation, primarily through cutting and pasting operations. Within its framework, the interpreter accommodates data types like Strings and Integers, enabling variable declarations, arithmetic expressions, and the execution of functions. Noteworthy functionalities encompass string concatenation, subtraction, and the inclusion of built-in functions designed for text manipulation.

# Functions  

1. size(myText): Returns the size of myText as an integer.  

2. subs(myText, begin, end): Retrieves a substring of myText between the characters marked by the two integers begin and end.  

3. locate(bigText, smallText, start): Searches for the first occurrence of smallText in bigText and returns its position as an integer. Returns 0 if not found, starting the search from the location marked by the integer start.  

4. insert(myText, location, insertText): Inserts insertText into the position marked by the integer location in myText and returns the resulting text.  

5. override(myText, location, ovrText): Writes ovrText onto myText, overriding whatever was previously there, starting from the location (given as an integer). If the writing operation exceeds the size of myText, it terminates at the end of myText without creating any error condition.  

6. asString(myInt): Converts myInt to a string and returns it.  

7. asText(myString): Converts myString to an integer and returns it.

# Commands  

1. read myString from myTextFile;: Reads a string from a text file named myTextFile.txt. No size limit.  

2. write myText to yourTextFile;: Writes the string called myText onto a text file named yourTextFile.  

3. input myText prompt promptText;: Accepts input from the keyboard into myText, using promptText as a prompt.  

4. output myText;: Displays the contents of myText on the screen.  

# Lexical Rules

1- Identifiers:  
•	Maximum identifier size is 30 characters. If an identifier larger than that is used, the lexical analyzer issues an error message.  
•	The language is not case sensitive and all the identifier names are standardized as lower case.  
•	Identifiers start with an alphabetic character (a letter) and are composed of one or more letters/digits/_ (underscore).  

2- Integer Constants  
• The maximum size for integers aligns with that of an unsigned int in C.  
• The absence of support for negative values means that all integers are either zero or positive.  

3- Operators  
•	Valid operators of the language are +,-,:=  

4- String Constants:  
•	String constants of the language are delimited by double quotes (ASCII code 34)as in “this is a string”.  
•	String constants have unlimited size.  
•	String constants cannot contain the double quote character. when you reach one, the string terminates.  
•	If a string constant cannot terminate before the file end, a lexical error is issued.  

5- Keywords:  
•	Keywords are: new, int, text, size, subs, locate, insert, override, read, write, from, to, input, output, asText, asString  

6- End of Line:  
• EndOfLine: ;  

7- Comments:  
• Anything between /* and */ is a comment.  
•	If a comment cannot terminate before the file end, a lexical error is issued.  
