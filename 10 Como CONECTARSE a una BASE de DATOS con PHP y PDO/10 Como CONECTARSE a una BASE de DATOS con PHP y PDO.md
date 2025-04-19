# 10 Como CONECTARSE a una BASE de DATOS con PHP y PDO
1. Creo el archivo `main.php` dentro de la carpeta `php`
2. Instancio la clase PDO
3. 'tipodeDB:host:elqueutilizo;dbname=nombreDB', 'user', ''
4. Ingresar a inventario/php/**main.php**

```php
<?
    # Conexion a la DB
    $pdo = new PDO('mysql:host=localhost;dbname=inventario', 'root', '');
```

En el  `main.php` creamos funciones reutilizables