# daily-question-javascript-q21

### Try/Catch/Throw

The experimentWithTries() function in the following HTML page throws and catches exceptions:

```
<!DOCTYPE html>
<html>
<head>
    <title>Intro to JavaScript</title>
	<meta charset=&quot;utf-8&quot; />
</head>
<body>
    <script>
        experimentWithTries();

        function experimentWithTries() {
            try {
                try {
                    console.log('Starting the process...');
                    throw new Error('Something went wrong');
                    console.log('Ending the process...');
                }
                catch (ex) {
                    console.log(ex);
                    throw new Error(ex);
                }
                finally {
                    console.log('The inner finally block')
                }
            }
            catch (ex) {
                console.log(ex);
            }
            finally {
                console.log('The outer finally block')
            }
            console.log('Glad to be done!');
        }
    </script>
</body>
</html>
```

* What will be displayed in the console when the page is loaded in the browser?

A.

Starting the process...  

Error: Something went wrong

The inner finally block  

Error: Error: Something went wrong 

The outer finally block  

Glad to be done!


B.

Starting the process...  

Error: Something went wrong 

Error: Error: Something went wrong 

The outer finally block  

Glad to be done! 


C.

Starting the process...  

Error: Something went wrong 

Ending the process... 

The inner finally block   

Error: Error: Something went wrong 

The outer finally block   

Glad to be done! 
