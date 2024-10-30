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

### **$SERVER info**
```php
echo $_SERVER['PHP_SELF'];
echo $_SERVER['SERVER_NAME'];
echo $_SERVER['HTTP_HOST'];
echo $_SERVER['HTTP_REFERER'];
echo $_SERVER['HTTP_USER_AGENT'];
echo $_SERVER['SCRIPT_NAME'];
```
#### PHP_SELF
PHP_SELF printer ut filstien (file path) til PHP filen

#### SERVER_NAME
SERVER_NAME printer ut... server name...

#### HTTP_HOST
HTTP_HOST printer ut navnet på host serveren.

#### HTTP_REFERER
HTTP_REFERER printer ut URL-en til siden.

#### HTTP_USER_AGENT
HTTP_USER_AGENT printer ut user agenten til brukeren, som viser informasjon om nettleser, nettleserens engine, operativsystem, osv.

#### SCRIPT_NAME
SCRIPT_NAME printer ut navnet og filstien til PHP filen.

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