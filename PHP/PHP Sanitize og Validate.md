# Sanitize

```php
<?php
if (isset($_POST["login"])) { // sjekker om "login" i HTML-skjemaet er fylt inn
    $username = filter_input(INPUT_POST, "username", FILTER_SANITIZE_SPECIAL_CHARS); // lager en variabel som filtrerer input fra POST-variabelen "username" (fra HTML skjema), og filtrerer special characters.
    echo "Hello $username <br>";
    $age = filter_input(INPUT_POST, "age", FILTER_SANITIZE_NUMBER_INT); // lager en variabel som filtrerer input fra POST-variabelen "age" (fra HTML skjema), og filtrerer INT(eger) tall. Inputter du "wasdopwkasdl72asd", outputter den filtrerte variablen kun '72'.
    echo "You are $age years old <br>";
    $email = filter_input(INPUT_POST, "email", FILTER_SANITIZE_EMAIL); // lager en variabel som filtrerer input fra POST-variabelen "email" (fra HTML skjema), og filtrerer e-mail. Den filtrerer bort tegn og bokstaver som ikke er lovlig å ha i en email, som f.eks parantes, krokodillemunn, osv.
    echo "E-mail: $email";
}
?>
```

# Validate
```php
<?php
if (isset($_POST["login"])) { // sjekker om "login" i HTML-skjemaet er fylt inn
    $age = filter_input(INPUT_POST, "age", FILTER_VALIDATE_INT); // sjekker/validerer om POST variabelen "age" er en INT. Om det er en INT, gir den true, og false om det ikke er en int. (boolean)
    email = filter_input(INPUT_POST, "email", FILTER_VALIDATE_EMAIL) // sjekker/validerer om POST variabelen "email" har riktig email syntax, og hvis den ikke har det så returnerer den 0.
    if ($age) { // if age = true
        echo "You are $age years old";
    } else { // if age = false
        echo "That is not a valid age.";
    }

	if ($email) { // sjekker/validerer om $email er valid
	    echo "Your e-mail is $email <br>"; // Returnerer $email 1, så echo
	} else {
	    echo "That is not a valid e-mail. <br>"; // Returnerer $email 0, så echo at den ikke er valid.
	}
}
?>
```

Man burde alltid bruke sanitize og validate på all user input, just in case brukeren skriver noe med malicious intent.