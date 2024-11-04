```php
<?php
$password = null; // Lager en variabel med verdi null.

if (isset($_POST["submit"])) { // Sjekker om "submit" knappen i et HTML-form er set, eller, trykket på.
    $password = $_POST["password"]; // Setter verdien til $password variabelen til samme verdien som "password" inputten fra HTML-formet
    $encrypted = password_hash($password, PASSWORD_DEFAULT, ["cost" => 10]); // Lag en variabel med password_hash, som encrypter $password variabelen med PASSWORD_DEFAULT encryption, som akkurat nå er bcrypt. "cost" vil si hvor mye CPU den får lov til å bruke, eller, hvor mye det "koster" av CPU-en å encrypte passordet.
    echo "Encrypted password: $encrypted <br>"; // printer ut det krypterte passordet i en string.
}

if (password_verify($password, $encrypted)) { // Sjekker om password_verify kan verifisere at $password og $encrypted er make. Den decrypter $encrypted og matcher resultatet med $password.
    echo "Password is valid. <br>";
} else {
    echo "Password is invalid. You shall not pass! <br>";
}

?>
``` 
## Hvorfor og når bruke encryption / hashing?
Encryption og hashing er **veldig** viktig å bruke hvis du skal ha noe form for sensetiv informasjon. For eksempel hvis du skal ha noe innlogging på siden din, burde du ha encryption og hashing på passordene.