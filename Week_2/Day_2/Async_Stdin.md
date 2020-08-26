## Getting data from async

Asynchronous Functions `can't return` data. Instead, a `callback` should be passed in, and it will be `given` the `data`.

```javascript
const fs = require('fs');

const breedDetailsFromFile = function(breed, done) {
  console.log('breedDetailsFromFile: Calling readFile...');
  fs.readFile(`./data/${breed}.txt`, 'utf8', (error, data) => {

    console.log("In readFile's Callback: it has the data.");
    (!error) ? done(data) : done(undefined);

  });
};

const printOutCatBreed = breed => {
  console.log('Return Value: ', breed) 
};

breedDetailsFromFile('Bombay', printOutCatBreed);

module.exports = breedDetailsFromFile;
```

## Stdin and Readline example

### Stdin
```javascript
//You can preface a backtick string with \r to keep the word on the same line
const stdin = process.stdin;

stdin.setRawMode(true);
stdin.setEncoding('utf8');

stdin.on('data', (key) => {

  if (key === 'b') {
    process.stdout.write('\x07');
  } else if (key === 'q') {
    process.exit();
  }
});
```

### Readline & question
```javascript
const readline = require('readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question('Ask a question', (answer) => {
  console.log(`Your answer was: ${answer}\n`);
```
