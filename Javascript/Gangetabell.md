```js
for (let i = 1; i <= 10; i++) { // lager for loop for tallene den skal printe ut gangetabellen for
  console.log(`Gangetabellen til ${i} er:`); // printer ut hvilket tall gangetabellen er til
  for (let j = 1; j <= 10; j++) { // lager for loop for tallene den skal gange det forrige tallet med
    console.log(`${i} x ${j} = ${i * j}`); // printer ut den faktiske gangetabellen med å ta tallet fra for loopen over og ganger det med en ny en som går fra 1-10
  }
  console.log(); // legger til ny linje mellom hver gangetabell
}
```

