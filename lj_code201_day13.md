# LJ Code 201  - Day 13

## Notes
Quiz 7 & 8 due tomorrow night (Thurs) at 11:59pm
301 Entrance Exam due Sunday night at 11:59pm - no re-dos.

## Project FAQ
No API usage
Requirements are not firm (can be negotiated)
No Bootstrap or Skeleton. 
ChartJS or Google Maps allowed

## Final Project Details:

### Grades
- Overall Contributions (Keep a record of what you do). 20 Pts full, 15 partial.
- Code Contribution (Make a list of your commits). Full 15 Pts, 10 partial.
- Collaboration Contribution (Make a list of where you helped solve a problem for others). Full 15 its, 10 partial.

### Expectations:
- Good HTML, Good CSS, Good JS
- Survives page reload
- Ambitious and interesting, but completable in 1 week
- Makes something useful
- Team assignments Friday morning
- Pitching Thursday
- 30 Second Elevator Pitches

## Local Storage
- 201, we learn Persistence (storing states in the browser) 
- 301, we learn to access remote storage
- 401, we learn how to build storage, and access it
- Persistence: non-volatile storage of information (like a hard drive)
- State: stored information at a given instant
- Session Storage: as long as browser is open. 
- Local Storage: lives beyond closing of browser or shut-down of computer.
- Remote Storage: distributed storage of information, accessible by multiple computers // the internet.
- Cookies: local (browser storage).
- Local storage can share info across html pages.
- Local storage can’t store methods or functions. breaks them
- Local storage: lose inheritance structure between object and constructor. (Won’t matter to use now).
- Local storage stores in strings
- Need to convert data into string to place into Local Storage. Then store it.
- To retrieve from Local Storage: retrieve from LS, convert back to a data structure. Now data is in its original form.
- Converting data into string is called: stringify. To convert back, we parse.
- JSON: JavaScript Object Notation (values wrapped in double-quotes//string). XML and CSV are other methods to transfer information.
- var studentsStringified = JSON.stringify(students)

- var students = ['Kenneth', true, 34, 'Danny', true, 66, 'Sugey', true, 92]  
- var studentsStringified = JSON.stringify(students)   <— Change array to a String  
- localStorage.setItem(‘demo’, studentsStringinfied)    <— place item into Local Storage  
- var studentsRetrieved = localStorage.getItem('demo’)    <— get item back from Local Storage  
- JSON.parse(studentsRetrieved)    <— Turn string back into an array

#### Page Load
- if (LS exists) { retrieve, parse LS / assign that to allImages array, carry on} else { create image objects with 0 clicks 0 views, and carry on}
- User Votes
- Store into Local Storage


- localStorage.clear()  
- Or, create a clear local storage button on your page (with event listener), to clear it, and help you develop  

## Lab
Fork, clone, and edit your partner's repository.