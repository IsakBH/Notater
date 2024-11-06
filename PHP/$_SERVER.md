### **$SERVER info**
```php
echo $_SERVER['PHP_SELF'];
echo $_SERVER['SERVER_NAME'];
echo $_SERVER['HTTP_HOST'];
echo $_SERVER['HTTP_REFERER'];
echo $_SERVER['HTTP_USER_AGENT'];
echo $_SERVER['SCRIPT_NAME'];
```
### **PHP_SELF**
PHP_SELF printer ut filstien (file path) til PHP filen
	**Eksempler av bruk av PHP_SELF**
	```
    <form action="<?php htmlspecialchars($_SERVER['PHP_SELF']); ?>" method="post">
	```
	I dette eksempelet bruker du PHP_SELF istedet for å bruke filnavnet slik at hvis du endrer filnavnet, så fungerer den fortsatt. "htrmlspecialchars" er en måte å sanitize inputtet på.

### **SERVER_NAME**
SERVER_NAME printer ut... server name...

### **HTTP_HOST**
HTTP_HOST printer ut navnet på host serveren.

### **HTTP_REFERER**
HTTP_REFERER printer ut hvilke side som refererte til denne siden.

### **HTTP_USER_AGENT**
HTTP_USER_AGENT printer ut user agenten til brukeren, som viser informasjon om nettleser, nettleserens engine, operativsystem, osv.

### SCRIPT_NAME
SCRIPT_NAME printer ut navnet og filstien til PHP filen.
