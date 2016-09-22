# LJ Code 201 - Day 2

Today we learned how to add, commit, and push to GitHub, and did it on our own.

GitHub -> “remote” location, also known as “origin"
Laptop -> “local” location

1. Staging Stage: git add <filename>
2. Commit Stage: git commit -m “*contextual message of what you changed in file(s), in present tense.*”
3. Push Stage: git push origin master

*use "git status” between each stage*

## CSS
everything is in boxes
selector & declaration: 

p { 
	font-family: Arial;
}

p is selector, inside brackets is declaration. Further, font-family is the “property”, and Arial is the “value”. Also called a “key-value pair”.

<link href=“[relative location URL.css]” type=“text/css” rel=“stylesheet” />

the url with href is called an attribute.

.class with CSS
\#id with Javascript

***** CSS Rules Cascade — Super Important page in Chap 10 of HTML/CSS Book

## Javascript
ASI - automatic semicolon insertion. Browsers can throw in semicolons if you’re missing them in your code.

code blocks {} themselves don’t need semicolons. statements within the code block does need semicolons.

javascript is case sensitive. 

// single-line comment
/* multi-line comment */

variable declaration: var myVariable;
variable assignment: myVariable = x;

single equals sign “=" is the assignment operator

3 data types in javascript: strings, numeric, boolean

a javascript variable can hold different types of variables. Start it as a string, change it to a number.

Can’t start a variable with a number. Shouldn’t start with $ or _. (We’ll learn why later).
Don’t start a variable with a capital letter
No dashes or periods in a variable name.
Use camelCase
Can’t use keywords
While javascript is case sensitive, don’t use the same name for a variable in different cases
Snake Case: what_about_this
Kabob Case: this-is-kabob-case

touch filename1 filename2 filename3
