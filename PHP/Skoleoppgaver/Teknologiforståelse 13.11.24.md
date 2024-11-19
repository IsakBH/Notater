## Arrays med foreach
```php 
<?php
$frukter = array("appelsin", "banan", "eple");

$frukter[0] = "apekatt"; // Endrer det første elementet i arrayen "$frukter" til "apekatt"

foreach($frukter as $frukt){ // Går igjennom arrayen $frukter og gjør den "echo-able" so variabel $frukt.
    echo "$frukt <br>";
}
?>
``` 

## Funksjon for velkomstmelding
```php
<?php
function welcomeMessage($navn){ // Lager en funksjon med argument $navn
    echo "Velkommen til siden, $navn";
}

welcomeMessage("apekatt"); // Calller på funksjonen med navn argumentet som "apekatt"
?>
``` 

## Lengden av en array (legg til i PHP Arrays)
``` php
<?php
$dyr = array("katt", "hund", "and", "gås"); // lager en array med navn "dyr"
$dyrelengde = sizeof($dyr); // lager en variabel med verdien "4" (lengden av $dyr)

echo "$dyrelengde"; // echo-er $dyrelengde
?>
```

## Sjekk om et element er i en array
``` php
<?php
$farger = array("hvit", "svart", "grå"); // lager enarray som heter $farger

if(in_array('svart', $farger)){ // sjekker om 'svart' er in_array $farger
    echo "'Svart' er i arrayen 'farger'"; // echoer at den er det
}
else{
    echo "Fargen 'svart' er ikke i arrayen 'farger'"; // echoer at den ikke er det
}
?>
```

## Finn kvadratroten av et tall
```php
<?php
$tall = 491; // lager en variabel som heter $tall
$kvadratrot = sqrt($tall); // finner kvadratroten av $tall

echo "Kvadratroten av $tall er $kvadratrot"; // echo-er kvadratroten av $tall
?>
``` 
## Pluss sammen to tall/verdier i en array
```php
<?php
$tall = array(1, 2, 3, 4);
$sum = $tall[0] + $tall[3]; // variabel med verdien av summen av den første og den siste verdien i en array

echo "Summen av to av tallene er $sum"; // echo-er $sum
?>
```

## Sammenlign 2 variabler og se hvilken som er lengst
```php
<?php
function longestWord($word1, $word2){ // lager en funksjon med 2 argumenter
    if($word1 > $word2){ // hvis $word1 er større/lengre enn $word2
        echo "$word1 (word1) er lengre enn $word2";
    }
    elseif($word2 > $word1){ // hvis $word2 er større/lengre enn $word1
        echo "$word2 (word2) er lengre enn $word1";
    }
    else{ // hvis ingen av de er true
        echo "Du skal gi et ordentlig tall da, din apekatt";
    }
}

longestWord(word1: "apekatt1234", word2: "apekatt123"); // kaller funksjonen longestWord med argumentene "apekatt1234" og "apekatt123"
?>
```
 
## Fizzbuzz
```php
<?php
function fizzbuzz($i, $n){ // lager en funksjon med navnet fizzbuzz og 2 argumenter
    for($i = 1; $i <= $n; ++$i){ // for loop
        if($i % 3 == 0 && $i % 5 == 0){ // hvis $i ikke er delelig med 3, og ikke delelig med 5
            echo "FizzBuzz <br>"; // echo-er FizzBuzz
        }
        else if($i % 3 == 0){ // hvis $i ikke er delelig med 3
            echo "Fizz <br>"; // echo-er Fizz
        }
        else if($i % 5 == 0){ // hvis $i ikke er delelig med 5
            echo "Buzz <br>"; // echo-er Buzz
        }
        else{ // hvis ingen av de er true
            ech6o $i . "<br>"; // echo-er $i
        }
    }
}

fizzbuzz(1, 100);
?>
```