```php
<?php
setcookie("fav_food", "pizza", time() -0, "/");
setcookie("fav_drink", "urge", time() + (86400 * 2), "/");
setcookie("fav_dessert", "ice crem", time() + (86400 * 4), "/");
/*
foreach ($_COOKIE as $key => $value) {
    echo "$key -> $value <br>";
    }*/

if (isset($_COOKIE["fav_food"])) {
    echo "Salg på {$_COOKIE["fav_food"]}! Husk å kjøp!";
} else {
    echo "I do not know what your favourite food is.";
}
?>
```
