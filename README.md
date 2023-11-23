# Debugging report

***When I try to submit an empty form  
Lines 10, 17:  
Runtime error.   
Found errors `400 (Bad request)` and `TypeError: Cannot read properties of undefined (reading 'temp')` in the console pointing to an incorrect line. Wrote `required` attribute of the input. 

*** When I try to submit a form with invalid value(Unxisting city, set of letters, space, number)  
Line 10:  
Runtime error.  
Found error `404 (Not found)` in the console pointing to an incorrect line. Used a debugger to see where is the mistake, and discovered that in API `res:false` when I input an invalid value. So I wrote a conditional into the function `getData()`

Line 3:  
Syntax error, missing closing quote.  
Found an error in the console pointing to an incorrect line. I fixed that by adding a closing quote.  

Line 3:  
Runtime error, `formEL` is `null`.  
Found an error `TypeError: Cannot read properties of null (reading 'addEventListener')` in the console pointing to an incorrect line №39. I added `#` before the element to search by id.  

Line 4:  
Runtime error, misspelled function name. `.querySelectr` is `undefined`, so we try to call `undefined` as a function.   
Found an error `TypeError: document.querySelectr is not a function` in the console pointing to an incorrect line.  

Line 4:  
Runtime error, `cityInputEl` is `null`.  
Found an error `TypeError: Cannot read properties of null (reading 'value')` in the console pointing to an incorrect line №11. I added `#` before the element to search by id.  

Line 5:  
Runtime error, `tempEl` is `null`.  
Found an error `TypeError: Cannot set properties of null (setting 'textContent')` in the console pointing to an incorrect line №19. I added `#` before the element to search by id.  

Line 6:  
Runtime error, `messageEl` is `null`.  
Found an error `TypeError: Cannot set properties of null (setting 'textContent')` in the console pointing to an incorrect line №29. I added `#` before the element to search by id.  

Line 17:  
Runtime error,  the variable `temp` showed as `NaN`.  
Used the debugger in the developer panel to watch the execution code step by step. Having reached line 17, I discovered that there is no such data in the API because `data.temp` is `undefined`. To access the data with temperature I need to use `data.main.temp`.  

Line 17:  
Logical error, incorrect data display.  
I saw incorrect data displayed on the webpage. To round the resulting value to the nearest integer, we need to use the appropriate mathematical method.  

Line 19:  
Logical error, incorrect data display.   
I saw incorrect data displayed on the webpage. Using template literals with `${}` inside backticks is the correct syntax for string interpolation in JavaScript.  

Lines 28, 30, 32, 34:  
Logical error, if-statement is flipped.  
Used debugger to see that the wrong branch gets called. 

Line 39:  
Syntax error, the improper declaration of the event listener function.  
Found an error in the console pointing to an incorrect  line.  

Line 40:  
Runtime error, improper usage of the method to prevent the default behavior.  
Found an error in the console pointing to an incorrect  line. In JavaScript, when using the `addEventListener` method to handle events, we need to pass a function that takes an event object as its parameter. There is a mistake in calling `preventDefault()`. The correct usage is `e.preventDefault();`, where e is the event object passed to the function.
