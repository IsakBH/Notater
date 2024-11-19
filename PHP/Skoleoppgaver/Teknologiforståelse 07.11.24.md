## Swapper 2 variabler
```php
<?php
/*Lag to variabler tall1 og tall2 og en funksjon som bytter verdiene mellom de to tallene. Skriv ut tallene til konsollen før og etter at du bruker funksjon, slik: «tall1 = … og tall2 = …».*/

$tall1 = 5;
$tall2 = 10;

function swap()
{
    echo "Tall1: {$GLOBALS["tall1"]} <br> Tall2: {$GLOBALS["tall2"]} <br>";
    $temp = $GLOBALS["tall1"];
    $GLOBALS["tall1"] = $GLOBALS["tall2"];
    $GLOBALS["tall2"] = $temp;

    echo "Tall1: {$GLOBALS["tall1"]} <br> Tall2: {$GLOBALS["tall2"]}";
}

swap();
``` 

## Sjekker om et tall er i midten av 2 andre
```php
<?php
/*Lag en funksjon som tar tre tall som parametre. Hvis det første tallet ligger mellom de to andre tallene, skal funksjonen returnere true . Hvis ikke, skal den returnere false . Test funksjonen med forskjellige verdier og skriv ut resultatet i konsollen.*/

function sjekkImellom($tall1, $tall2, $tall3)
{
    if ($tall1 > $tall2 && $tall1 < $tall3) {
        echo "Tall1 er i midten av Tall2 og Tall3";
    } elseif ($tall2 > $tall1 && $tall2 < $tall3) {
        echo "Tall2 er i midten av Tall1 og Tall3";
    } else {
        echo "Tall 3 er i midten av Tall1 og Tall2";
    }
}

sjekkImellom(tall1: 9, tall2: 10, tall3: 12);
?>
```
