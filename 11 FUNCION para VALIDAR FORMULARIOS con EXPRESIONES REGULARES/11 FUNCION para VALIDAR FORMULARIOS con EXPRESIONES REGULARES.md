# 11 FUNCION para VALIDAR FORMULARIOS con EXPRESIONES REGULARES
```php
    #Verificacion datos formulario
    function verify_data($filtro, $cadena){
        if(preg_match("/^".$filtro."$/", $cadena)){
            return false;
        }else{
            return true;
        }
    }

    $nombre = 'Carlos';

    if(verify_data('[a-zA-Z]{6,10}', $nombre)){
        echo 'Los datos no coinciden';
    }

```
Esta hecho medio raro, puede mejorarse, practicamente usa preg match para corroborar que el valor de la variable coincida con los parametros prestablecidos