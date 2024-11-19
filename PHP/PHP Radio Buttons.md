
```php
<?php
$creditcard = null; // Angir $creditcard variabelen verdien 'null'

if (isset($_POST["creditcard"])) { // Sjekker om $_POST verdien "creditcard" er fylt inn i et HTML-form
    $creditcard = $_POST["creditcard"]; // Angir $creditcard variablen verdien til $_POST creditcard verdien fra et HTML-form
}
switch ($creditcard) { // Gjør det samme som if/elseif men med mindre kode. Trenger alltid "break" på slutten av en case for at den ikke skal fortsette i switchen
    case "obos":
        echo "You have picked Obos as your payment option.";
        break;
    case "mastercard":blir skrevet. Du kan også bruke variabeler for dette.
        echo "You have picked MasterCard as your payment option.";
        break;
    case "sparebanken":
        echo "You have picked Sparebanken as your payment option.";
        break;
    default: // Default sier hva den skal gjøre by default hvis ingen av case-ene matcher verdien til $creditcard.
        echo "Please pick a payment option.";
        break;
}
?>
```

**Hvorfor lage dette?**
Læring. Radio buttons er bra å bruke når brukeren skal velge mellom "predetermined" verdier.