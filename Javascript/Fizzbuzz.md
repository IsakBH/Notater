```js
function fizzbuzz(i, n) { // lag en funksjon med to argumenter
    for (let i = 1; i <= n; i++) { // for loop med let for bedre scoping
        if (i % 3 === 0 && i % 5 === 0) { // om det er delelig på både 3 og 5
            console.log("FizzBuzz"); // printer fizzbuzz
        } else if (i % 3 === 0) { // om det er delelig på 3
            console.log("Fizz"); // printer fizz
        } else if (i % 5 === 0) { // om det er delelig på 5
            console.log("Buzz"); // printer buzz
        } else { // hvis ingen av de over
            console.log(i); // skriv ut tallet
        }
    }
}

fizzbuzz(1, 100); // call på funksjonen med argumentene 1 og 100
```
