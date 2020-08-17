# Tips

Command line arguements can be passed into the command line to test scripts.

## Why Use Command Line Arguements

* You can pass information to an application before it starts. This is particularly useful if you want to perform large number configuration settings.
* Command line arguments are passed as strings to your program. String data types can easily be converted to other data types within an application, making the arguments very flexible.
* You can pass unlimited number of arguments via the command line.
* Command line arguments are used in conjunction with scripts and batch files, which is particularly useful for automated testing.

``` javascript
'use strict';

for (let j = 0; j < process.argv.length; j++) {
    console.log(j + ' -> ' + (process.argv[j]));
}
```

All this script does is `loop through the process.argv array and prints the indexes, along with the elements stored in those indexes.` It's very useful for debugging if you ever question what arguments you're receiving, and in what order.

``` javascript
const args = process.argv.slice(2);
```

This line of code removes the first two elements from the array leaving you with only the arguments passed by the user.