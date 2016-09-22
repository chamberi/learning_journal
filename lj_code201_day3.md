# LJ Code 201 - Day 3

Today we did Code Review, including proper spacing, indentation, and comments. 

javascript variable(space) = (space)property

in Atom, highlight code and…:
move up or down: control+command+up/down arrow
tab in or out: tab or shift+tab

make your variable names semantic 

D.R.Y. = Don’t Repeat Yourself

charAt(0); --> selects character at place 0. (first character).

## CSS
Margin->Border->Padding
min-width, max-width, min-height, max-height
display: inline, block, inline-block

## Arrays:
samsCats = [‘Buddy', ‘Alistair', ‘Trillian’]; 		—> cats’ names are elements within an array
samsCats[0] = ‘BuddyCat’;
samsCats[3] = ‘Kilmauski’;
samsCats.push(‘MeowMix;);

push method appends value to end of the array
pop, shift, and unshift are also like push of manipulating arrays (we’ll learn later)

samsCats.length;

var samsDogs = [‘joe’, ‘fred’];
var samsPets = [samsCats, samsDogs];
samsPets[0][0];  —> first pet within first array (SamsCats BuddyCat)

console.table(samsPets); —> prints table (like an excel spreadsheet) of the arrays

parseInt
parseFloat

var demoPrompt = parseInt(prompt(‘Gimme a number’));