# LJ Code 201 - Day 5

## Quizes
Quiz 1: 
Question 1: Operators (“+” is the string operator, connects: ‘hello” + username)
Question 2: to run javascript in an html file: <script></script>
Q3: data types: booleans, numbers, string, array, objects
Q4: git checkout -b filename
Q5: html provides structure to document
Q6: use whitespace. use fixed-width font (characters are the same width). use syntax highlighting. use step-by-step instructions (i.e. comments).
Q7:  mkdir (makes directory)
Q8: && (and), || (or), != (does not equal) —> will evaluate left side first (true || false), and then not evaluate right side.
Q9: if (x > y) {
		code;
	}
Unexpected token error: Missing bracket
Variable Not Defined: 
Q10: !=


Quiz 2:

Q2: body {
color: white
}
Text within body becomes white.
Q3: Span is inline.
Q4: 
typeof(object) = string

## Images
600 x 300: (first is length, second is height)

_____|300
 600

Gimp —> photo editor

jpeg/jpg: most common image format
gif: good for limited amount of colors: line art, not images. much smaller.
png: transparency layer. 

## Cleanup
variables - name them as nouns, and make them descriptive
unctions - name them as verbs

3 hardest parts of programming: naming, off by 1, memory conflict.

## Git
git checkout branch-name —> moves you to new (existing) branch
git checkout -b branch-name —> creates new branch (-b) AND moves you to the new branch
git branch —> lists branches, and which branch you’re currently on
git push origin branch-name —> pushing updates to GH to the branch repo

You don’t NEED to do a git push with every git add/git commit.

Master —> Initial git commit —> 									   /—> Merge							    /—> Merge
				|_> question1sum —> commit —> commit —> commit /		      \							  /
																		question2multiply —> commit/ 



  var sum = a + b;
  var message = 'The sum of ' + a + ' and ' + b + ' is ' + sum + '.';
  var output = [sum, message];
  return output;

git checkout -b question2
edit code in atom


make a repo on GH
Grab clone URL on Terminal
In terminal, git clone URL
cd new branch
touch index.html app.js xyz.css

git add .
git commit -m "mulitply is working"
git push origin question2
on GH, pull request
git checkout master 
git pull origin master
git checkout -b question3