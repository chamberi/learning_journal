  # LJ Code 201 - Day 8

## Code Review  
for (var i in hours) {totals[i] = 0;} <— New For Loop  
for each <— another new For Loop (we’ll learn later)  

#### Structure Code  
Set up Data  —> Var  
Define our Actions  —> function() {}
Execute our Action  —> function()

Function Expressions:  
var xyz = function () {}  
  
vs.  
  
Function Declaration:  
function xyz() {}  

Load functions that  you need right away with Function Declarations.   
Only load functions that you might need later via Function Expressions.  

At bottom of code:

createHeaderRow();
for (var i = 0; i < allLocations.length; i++; {
	allLocations[i].render();
}
createFooterRow();

## Reading Review - Events  
Event Listeners listen to a particular type of event, event handler takes over.  
Events are actually objects.  
async - asynchronous actions.  

UI events, keyboard, mouse, focus, form, mutation, interactive on phone/device  
For Today: click event and submit events.  

setting up event listener  
creates an event object  
event handler takes event object and executes the actions you want  

HTML event // Don’t Use (old)  
DOM Event Listeners  

element.addEventListerner(‘event’, functionName, Boolean);  
element.addEventListerner(submit, functionName); <— We’ll use today  

Event Listener takes 
event (submit event)  
function (event handler)  
boolean (event flow <— we won’t use today)  

### Event Code Demo  

#### HTML:  

<>Note: Your possible users are Aliza,Benton, Frazier, Maelle, Munir, Nick, Otis, Rachel, and Sam.</h1>  
  
<form id=“form-name”>  
  <fieldset> <— defines a group of forms for us, also makes a border around the form  
    <legend>Chat Submission Form</legend>  

    <label for="who">Who: </label>>       <— label for “who” needs to equal input name “who  
    <input name=“who” type=“text” />   
    
    <label for=“says”>Comment: </label>  
    <input name=“says” type=“text” size=“50" />  
  
    <button type=“submit”>Create new comment!</button>  
  </fieldset>  
</form>  
 
<button id="clear-chat-list">Clear all comments!</button>  

#### JS

// Global variables for DOM access and such  
var chatList = document.getElementById('chat-list’);  
var chatForm = document.getElementById('chat-form’);  
var clearChatList = document.getElementById('clear-chat-list’);  
var allComments = [];  

// Here's the constructor for the individual comments  
var Comment  = function(userName, text) {  
  this.userName = userName;  
  this.text = text;  
};  
  
Comment.prototype.render = function() {  
  var liEl = document.createElement('li’);  
  liEl.innerHTML = '<img width="100px" src="img/' + this.userName + '.jpg"> <b>' + this.userName + ': </b><em>' + this.text + '</em>’;  
  return liEl;  
};  

// FUNCTION DECLARATIONS  
  
// This function gots through the array of comments and calls the render() method on each one  
function renderAllComments() {  
  chatList.innerHTML = ‘’;        <— wipes away comments (later puts them back, plus new one)  
  
  for (var i = 0; i < allComments.length; i++) {  
    chatList.appendChild(allComments[i].render());   <— adds all comments back  
  }  
  
  // These lines could be used to replace the 'for' loop above  
  // allComments.forEach(function(unicorn) {  
  //   chatList.appendChild(unicorn.render());  
  // });  
  
};  
   

// This function is the event handler for the submission of comments  
function handleCommentSubmit(event) {     <— sometimes just (e) instead of (event)  
  
  // console.log('log of the event object', event);  
  // console.log('log of the event.target', event.target);  
  // console.log('log of the event.target.says', event.target.says);  
  // console.log('log of the event.target.says.value', event.target.says.value);  

  event.preventDefault(); //gotta have it for this purpose. prevents page reload on a 'submit’ event  
  
  if (!event.target.says.value || !event.target.who.value) {  
    return alert('Fields cannot be empty!’);  
  }  
  
  var commenter = event.target.who.value;  
  var remark = event.target.says.value;  
  
  if (commenter === 'Sam') {  
    remark = '@$^#$%$^@#$%@‘;  
  }  
  
  if (commenter === 'Benton') {  
    remark = remark.toUpperCase();  
  }  
  
  if (commenter === 'Otis') {  
    remark = 'Shama-lama-ding-dong’;  
  }  
  
  var newComment = new Comment(commenter, remark);  
  
  // console.log('Comment by ' + event.target.who.value + ' at ' + Date());  
  
  event.target.who.value = null;  
  event.target.says.value = null;  
  
  allComments.push(newComment);  
  renderAllComments();  
};  
  
// +++++++++++++++++++++++++++++++++++++++++++++++++++++  
// Event listener for comment submission form  
chatForm.addEventListener('submit', handleCommentSubmit);  
  
// +++++++++++++++++++++++++++++++++++++++++++++++++++++  
// Event listener for the 'Clear all comments’ button  
clearChatList.addEventListener('click', function() {  
  chatList.innerHTML = ‘';  
  console.log('You just cleared the chat list!’);  
  allComments = [];  
});  
  
// +++++++++++++++++++++++++++++++++++++++++++++++++++++  
/* Here is where we would put everything else that we want to execute on page load.   


Need Event Handler  
Need Prevent Default  
Should Use !event.target.says.value —   validation of form  
Should use commenter and remark to simplify var  
Need to pass to constructor  
Need to render  
Need event listener  

Need parseInt - convert strings into numbers