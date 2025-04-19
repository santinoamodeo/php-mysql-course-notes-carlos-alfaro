# 05 CREAR COPIAS DE SEGURIDAD (BACKUP) en MySQL con PHPMYADMIN
1. Selecciono la DB
2. Exportar
3. Seleccionar entre rapido y personalizado
    
   - **Rapido** hace una copia de datos y estructural, pero no de la db, por lo que debemos crear una db con el mismo nombre que la exportada a la hora de importar
    
    - **Personalizado** permite seleccionar lo que queremos, si la usamos debemos marcar 'agregar sentencia CREATE DATABASE / USE'.

    En sintesis, **rapido no crea la db**, **personalizado con la sentencia si**