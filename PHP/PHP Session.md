## Start session:
```php
<?php
session_start(); // ... starter en session (who would've guessed)
?>
```

## Session variabler
```php
<?php
if (isset($_POST["login"])) { // sjekker om login knappen i HTML-skjemaet er set

    if (
        !empty($_POST["username"]) &&
        !empty($_POST["password"]) // sjekker om POST variabelene "username" og "password" ikke er empty
    ) {
        $_SESSION["username"] = $_POST["username"]; // lager en SESSION variabel med samme verdien som POST variabelen "username"
        $_SESSION["password"] = $_POST["password"]; // lager en SESSION variabel med samme verdien som POST variabelen "password"
        header("Location: heim.php"); // redirecter deg til "heim.php"
    } else {
        echo "Username/password field is empty"; // hvis POST variabelene "username" og "password" ER empty, så echo-er den
    }
}
?>
```
