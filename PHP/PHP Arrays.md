## Pluss sammen to tall/verdier i en array
```php
<?php
$tall = array(1, 2, 3, 4);
$sum = $tall[0] + $tall[3]; // variabel med verdien av summen av den første og den siste verdien i en array

echo "Summen av to av tallene er $sum"; // echo-er $sum
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

## Velg et tilfeldig element i en array
```php
$maskin = array_rand($muligheter); // 'array_rand' velger et tilfeldig element innenfor en array. Den returnerer posisjonen til elementet i arrayen, ikke navnet. (f.eks 0, 1, 2, 3, osv)
```

