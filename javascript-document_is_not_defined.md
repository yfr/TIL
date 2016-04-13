When you have a webapp developing with nodejs stack and use let's say something like `document.cookie` to get the csrftoken for upcoping requests to a server. You would have to put that somewhere in you code.

Let's further asume you want to test your stuff with some kind of nodejs test runner. 

That's when you might run into a problem with document is not defined. Which makes sense and sounds right and all. To circumwent this error my first atempt was to just say const cookies = !document ? document.cookie : ''.

But to my suprise this throws ecactly the same error. Me: w ... t ... f? I just you. What to do when there is no document. 
