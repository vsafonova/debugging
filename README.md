# Debugging report

When I try to submit an empty form  
Lines 10, 17:  
Runtime error.   
Found errors `400 (Bad request)` and `TypeError: Cannot read properties of undefined (reading 'temp')` in the console pointing to an incorrect line. Wrote `required` attribute of the input. 

Line 3:  
Syntax error, missing closing quote.  
Found an error in the console pointing to an incorrect line. I fixed that by adding a closing quote.  

Line 3:  
Runtime error, `formEL` is `null`.  
Found an error `TypeError: Cannot read properties of null (reading 'addEventListener')` in the console pointing to an incorrect line №39. I added the searching element by id and added `#` before the element.  

Line 4:  
Runtime error, misspelled function name. `.querySelectr` is `undefined`, so we try to call `undefined` as a function.   
Found an error `TypeError: document.querySelectr is not a function` in the console pointing to an incorrect line.  

Line 4:  
Runtime error, `cityInputEl` is `null`.  
Found an error `TypeError: Cannot read properties of null (reading 'value')` in the console pointing to an incorrect line №11. I added the searching element by id and add `#` before the element.  

Line 5:  
Runtime error, `tempEl` is `null`.  
Found an error `TypeError: Cannot set properties of null (setting 'textContent')` in the console pointing to an incorrect line №19. I added the searching element by id and add `#` before the element.  

Line 6:  
Runtime error, `messageEl` is `null`.  
Found an error `TypeError: Cannot set properties of null (setting 'textContent')` in the console pointing to an incorrect line №29. I added the searching element by id and add `#` before the element.  

Line 17:  
Runtime error, `data.temp` is `NaN`.  
Used the debugger in the developer panel to watch the execution code step by step. Having reached line 17, I discovered that there is no such data in the API. To access the data with temperature I need to use `data.main.temp`.  

Line 17:  
Logical error, incorrect data display.  
I saw incorrect data displayed on the webpage. To round the resulting value to the nearest integer, we need to use the appropriate mathematical method.  

Line 19:  
Syntax error, incorrect data display.   
I saw incorrect data displayed on the webpage. Using template literals with `${}` inside backticks is the correct syntax for string interpolation in JavaScript.  

Lines 28, 30, 32, 34:  
Logical error, if-statement is flipped.  
Used debugger to see that the wrong branch gets called. 

Line 39:  
Syntax error, the improper declaration of the event listener function.  
Found an error in the console pointing to an incorrect  line.  

Line 40:
Syntax error,  improper syntax of the method to prevent the default behavior.  
Found an error in the console pointing to an incorrect  line. In JavaScript, when using the `addEventListener` method to handle events, we need to pass a function that takes an event object as its parameter. There is a mistake in calling `preventDefault()`. The correct syntax is `e.preventDefault();`, where e is the event object passed to the function.
