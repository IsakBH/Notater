## Antall forekomster
```php
<?php
echo substr_count("hei på deg verden, hei hei", "hei"); // substr_count teller hvor mange ganger stringen etter komma (som i denne tilfellen er "hei") blir skrevet. Du kan også bruke variabeler for dette.
?>
```
## Stein saks papir
```php

<?php
$muligheter = array("0", "1", "2"); // lager en array med verdiene 0, 1, og 2
$maskinensValg = array_rand($muligheter); // lager en variabel og angir en tilfeldig verdi fra arrayen $muligheter
$dittValg = $_POST["dittValg"]; // 

if ($dittValg == $maskinensValg) { // hvisdittValg er det samme som maskinensValg 
    echo "Uavgjort <br>"; // Uavgjort
}
elseif ($dittValg == "0" && $maskinensValg == "1" ||$dittValg == "2" && $maskinensValg == "0" || $dittValg == "1" && $maskinensValg == "2") { // sjekker alle mulighetene for at du vinner
    echo "Du vant! <br>"; // Du vant
}
else { // Hvis det ikke er uavgjort, og du ikke vant, så har du tapt. 
    echo "Du tapte... <br>"; // Du tapte
}

echo "<br> Du valgte: $dittValg <br> Maskinen valgte: $maskinensValg <br>"; // Printer ut dittValg og maskinensValg
?>
```
## Partall og Oddetall
