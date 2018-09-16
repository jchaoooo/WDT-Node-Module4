Questions

1. Run the commands sort, wc and uniq on the commands.js file. Explain how they work and what the output was.

`sort`: Printed every line of code from the commands.js file in a certain structure.  Each hierarchy in the code was grouped together and alphabetically sorted by the first word of the line.

`wc`: Printed out the # of lines, the number of words and the number of characters.

`uniq filename`: Sorted each line in the file and only returned different lines and removed the duplicate lines next to each other.

2. Using the pipe (|) connect at least two commands and run it on commands.js. Explain what the output was and why the specific data was outputted.

`sort commands.js | uniq`:  This first sorted everything in commands.js then removed any duplicate lines that were next to each other.  For instance, it removed duplicate `break;`

`uniq commands.js | sort`: This first deleted duplicate lines next to each other then sorted each line.  In this instance both `break;` lines still existed.

In conclusion when things are piped the first command executes and then the second will take the info that was executed and execute the second command.

3-5.

6. Given a string, reverse the order of characters in each word within a sentence while maintaining the original word order and whitespace and return the string. To improve your problem-solving experience, use the suggested functions to solve the problem.

```
function reverseString(inputString) {
      return inputString.split('').reverse().join('');
    };
```
