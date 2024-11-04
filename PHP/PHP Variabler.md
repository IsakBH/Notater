## Lag variabler
```
<?php
$du = "apekatt";
$jeg = "kul";
$linustorvalds = "alfa ulv";
?>
```
For å lage variabler i PHP og gi dem verdi, skriver du $(navn på variabel) = (verdi);
Etter det kan du "calle" på variablene ved å skrive $(navn på variabel). For eksempel:
`echo "Du er en {$du}";`
Du trenger ikke å bruke krøllparentes, men det er som oftest anbefalt. Hvorfor? Ingen anelse. Men jeg gjør det fortsatt.
## Globale variabler
```
<?php
$x = 69;

function apekatt()
{
    echo $GLOBALS["x"] / 2;
}

apekatt();


?>
```
$GLOBALS["x"] betyr at funksjonen leter etter en global variabel som heter "X", som kan være utenfor funksjonen selv. Har du ikke $GLOBALS inne i funksjonen der du caller variablen, kan ikke funksjonen finne den fordi den kan ikke se noe utenfor den selv.