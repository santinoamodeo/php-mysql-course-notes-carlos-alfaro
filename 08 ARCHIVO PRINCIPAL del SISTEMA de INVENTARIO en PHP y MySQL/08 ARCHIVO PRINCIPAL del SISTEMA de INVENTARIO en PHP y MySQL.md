# 08 ARCHIVO PRINCIPAL del SISTEMA de INVENTARIO en PHP y MySQL
## Manejo de la sesion
Al igual que todo, incluimos archivo independiente

```php
#session_start.php
<?php
    session_name('IV');
    session_start();
```

```php
#index.php
<?php require './inc/session_start.php'; ?>
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
Se coloca el require al principio, para que corrobore la inclusion de dicho archivo

### Interaccion entre los archivos
```php
<?php require './inc/session_start.php'; ?>
<!DOCTYPE html>
<html lang="es">
<head>
    <?php include './inc/head.php'; ?>
</head>
<body>
    <?php
        if(!isset($_GET['view']) || $_GET['view']==""){
            $_GET['view']="login";
        }

        if(is_file("./views/".$_GET['view'].".php") && $_GET['view']!="login" && $_GET['view']!='404'){
            include './inc/navbar.php'; 
            include './views/'.$_GET['view'].'.php'; 
            include './inc/script.php'; 
        }else{
            
            if($_GET['view']=='login'){
                include './views/login.php'; 
            }else{
                include './views/404.php';
            }
        }
    ?>
</body> 
</html>
```
## 1. Primera condición:
Si no viene "**view**" en la URL o está vacío → Usar "**login**"

***Ejemplo***: Si la URL es tusitio.com sin parámetros, automáticamente carga la página de login.

## 2. Segunda condición principal:
Si el archivo existe Y no es **login** ni **404** → Mostrar página normal


## Si falla la condición principal y el usuario accede

Si es **login** → Mostrar solo la página de **login**

Si es cualquier otra cosa → Mostrar error **404**
