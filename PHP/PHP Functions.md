### Funksjon for å sjekke om et tall er et partall
```<?php
function is_even($number) { // Lager en funksjon som heter "is_even" med parameteret "$number". Parameteret er noe du må skrive inn i parantesen når du caller på funksjonen, og oppfører seg som en midlertidig variabel som bare eksisterer inni funksjonen.
    return $number % 2; // Returnerer variabelen "$number" med modulus 2. 
}

echo is_even(11); // printer resultatet av "is_even" funksjonen med "$number" parameteret som 11.
?>
```
**Resultat:**
Funksjonen returnerer 0 om et tall er et partall, og 1 om det er et oddetall.

### Funksjon for å finne hypotenus av en trekant
```
<?php
function hypotenuse($a, $b)
{
    $c = sqrt($a ** 2 + $b ** 2);
    return $c;
}

echo hypotenuse(4, 5);
?>
```
