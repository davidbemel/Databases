# Databases

# Postgresql
# ingresar a psql.exe
```
Cerrar conexión 	\q
Cambiar de Base de datos 	\c __base_datos__
Listar Bases de datos 	\l
Ver Definiciones 	\d __table__
Listar Schemas 	\dn
Listar funciones 	\df
Listar Vistas 	\dv
Ver código SLQ de la función 	\df+ __function
Pretty-format 	\x


```
Pasos para ingresar a Postgresql
```
psql -u postgres -W -h localhost
```

Pasos para hacer el dump
Respaldando:
```
> pg_dump -U [usuario] -W -x -O -d [base_de_datos] > [archivo.sql]
```
Recuperando
```
> psql -U [usuario] -W -d [base_de_datos_destino] < [archivo.sql]
```
# Monitoreo

Número de Sesiones:

psql> SELECT COUNT(*)FROM pg_stat_activity;

Ver las sesiones activas:

psql> SELECT COUNT(*)FROM pg_stat_activity;

Matar una conexión:

psql> SELECT pg_terminate_backend( [numero_sesion] );

## importing


    Exportando:

    psql> COPY [tabla] TO '[archivo_csv]' DELIMITER ',' CSV HEADER;

    Importando:

    psql> COPY [tabla] FROM '[archivo_csv]' WITH (FORMAT csv);



