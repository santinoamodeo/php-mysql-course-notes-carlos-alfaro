# 07 Como INSTALAR FRAMEWORK BULMA CSS en un PROYECTO WEB
1. Ir a https://bulma.io/
2. Documents/Overview/Start
3. Descargar y descomprimir el ZIP
4. Copiar el archivo `bulma.min.css` en la carpeta `css` del inventario
5. Vincular con link href el archivo en el `index.php`

Un poco como react, se trabaja incluyendo fragmentos de codigo repetitivo al `index.php`, como la navbar, el footer, etc

## Ordenamiento
Dentro de `index.php` unicamente incluimos codigos que estan ordenados en carpetas, se ve asi
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <?php include './inc/head.php'; ?>
</head>
<body>
    <?php include './inc/navbar.php'; ?>
    <?php include './inc/script.php'?>
</body> 
</html>
```

Scripts de JS van dentro de `script.php`
