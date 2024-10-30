### Funksjon for å sjekke om et tall er et partall
```php
<?php
function is_even($number) { // Lager en funksjon som heter "is_even" med parameteret "$number". Parameteret er noe du må skrive inn i parantesen når du caller på funksjonen, og oppfører seg som en midlertidig variabel som bare eksisterer inni funksjonen.
    return $number % 2; // Returnerer variabelen "$number" med modulus 2. 
}

echo is_even(11); // printer resultatet av "is_even" funksjonen med "$number" parameteret som 11.
?>
```
**Resultat:**
Funksjonen returnerer 0 om et tall er et partall, og 1 om det er et oddetall.
### Funksjon for å finne hypotenus av en trekant
```php
<?php
function hypotenuse($a, $b)
{
    $c = sqrt($a ** 2 + $b ** 2);
    return $c;
}

echo hypotenuse(4, 5);
?>
```

## **String Functions**
```php
<?php
$username = array(Isak Brun Henriksen);
$phone = "458-48-234";
/*
$username = strtolower($username); // 'strtolower' står for "string to lower", og som du kanskje tenkte, så omgjør den alle uppercase bokstaver i en string variabel til lowercase.
$username = strtoupper($username); // 'strtoupper' er det motsatte av 'strtolower' 
$username = trim($username); // 'trim' fjerner all tomrom i en string
$username = str_pad($username, 20, "0"); // str_pad legger til vis mengde padding (i dette eksempelet er det 20) med en bokstav du selv velger (som i dette tilfellet er "0"), 
$phone = str_replace("-", " ", $phone); // 'str_replace' erstatter en ting med en annen. I dette eksempelet erstatter den "-" med et mellomrom, eller, " ". 
$username = strrev($username); // 'strrev' snur en variabel omvendt.
$username = str_shuffle($username); // 'str_shuffle' shuffler en variabel. (who would have guessed)
$equals = $username = strcmp($username, "Isak Henriksen"); // 'strcmp' sammenligner en variabel med en streng, og printer 0 hvis de er identisk, og 1 hvis de ikke er det.
$count = strlen($username); // 'strlen' finner lengden til en streng.
$index = strpos($username, " "); // 'strpos' finner posisjonen til et tegn eller ord i en variabel.
$firstname = substr($username, 0, 4); //  'substr' lager en ny string fra deler av en annen string. I dette eksemplet, ser du at den lager en string fra bokstav 0 til 4. 
$fullname = explode(" ", $username); // 'explode' lager en array av en variabel. I dette eksempelet bruker jeg "Isak Brun Henriksen", og da lager 'eplode' en array med de 3 verdiene 'Isak', 'Brun', og 'Henriksen'.
$username = implode(" ", $username); // 'implode' er det motsatte av 'explode'.
echo $username;
*/

?>
```
