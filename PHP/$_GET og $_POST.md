## _$GET  og $_POST

```
<?php
$x = $_POST["value til html form input"];
echo $x;
?>
```
Når du bruker $POST, så henter den verdien til et input-field i et HTML-form, som er ganske nyttig å ha når du skal ha input fra bruker. Med dette kan du ha et HTML-form hvor du spør brukeren om en verdi, og så bruker du det input-et til et spill eller hva no enn annet du vil bruke det til.

``` 
<?php
$x = $_GET["value til html form input];'
echo $x;
?>
```
$GET er mye det same som $POST, bare at den putter all informasjonen i URL-en til siden. Noen ganger kan dette være helt ok, for eksempel når du driver med ting som ikke har noe med credentials / personlig data, fordi 

### Hvorfor bruke POST ovenfor GET?
POST er mer sikkert enn GET, fordi når GET får data, så putter den det i URL-en til siden. Det er ikke særlig bra når du skal ha innlogging med passord eller andre personlige ting som du ikke vil andre skal vite. 