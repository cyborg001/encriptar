## Este escritorio contiene los siguientes scripts
1- generarador
2- encripta

## uso:
Es importante darle permiso de ejcutable a ambos scripts o simplemente
correrlos con el comando bash, ex:
bash generarador

## generar_keys
Este script se corre con el comando bash generador o ./generarador si tiene permiso de ejecucion y entrara en un
interativo para genearar un par clave publica/privada
solamente siga los pasos del iterativo


## encripta
se corre con el comando ./encripta clave, donde clave es el parametro que pasa la clave publica
Suponiendo que existe un directorio ~/automation que a su vez contiene subdirectoros pa1, pa2 ...
este script se encargara de encriptar todos los subdirectorios pa1, pa2,.... creando los
directorios encriptados pa1.tar,pa2.tar, ....

---------------------------------------------------------------------------
Los siguientes comandos estan en desarrollo

## importar_key
Se corre con ./importar_key
El script se encarga de importar la llave secreta creada a un archivo secret.key luego
elimina la clave del anillo para que no se pueda desencriptar el archivo a menos que
se importe la llave secreta.

## desencriptar
Se ejecuta como sigue: ./desencriptar parametro
Se encargara de desencriptar lo archivos encriptados y extraerlos y moverlos al directorio ~