
```php
<form action="index.php" method="post">
    <input type="checkbox" name="foods[]" value="Pizza"> // Lager en input med typen "checkbox", name "foods[]" (array), og value "Pizza"
        Pizza <br>
    <input type="checkbox" name="foods[]" value="Pasta"> // Lager en input med typen "checkbox", name "foods[]" (array), og value "Pasta"
        Pasta <br>
    <input type="checkbox" name="foods[]" value="Hotdog"> // Lager en input med typen "checkbox", name "foods[]" (array), og value "Hotdog"
        Hotdog <br>
    <input type="submit" name="submit" value="confirm"> // Lager en input med type "submit", som betyr at det bare er en knapp som sender inn / submitter svaret på HTML form-en.
</form>

<?php if (isset($_POST["submit"])) {
    $foods = $_POST["foods"];

    foreach ($foods as $food) {
        echo "$food <br>";
    }
}
?>
```
## **Hvorfor bruke checkboxes ovenfor radio buttons?**
Checkboxes kan være veldig nyttig å bruke når du skal ha f.eks spørsmål hvor du kan svare på flere forskjellige svar, og andre ting som det. Når du har `name="blahblah[]`, betyr det at der er et array. Det kan være kult å ha når du skal samle inn svar på noe.