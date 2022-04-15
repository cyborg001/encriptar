## Este escritorio contiene los siguientes scripts
1- generardor
2- encripta
3- exportar_key
4- importar_key

## uso:
Es importante darle permiso de ejcutable a ambos scripts o simplemente
correrlos con el comando bash, ex:
bash generarador

## generar_keys
Este script se corre con el comando bash generar_keys o ./generar_keys si tiene permiso de ejecucion y entrara en un
interativo para genearar un par clave publica/privada
solamente siga los pasos del interativo

## exportar_key
Se ejecuta con ./exportar_key el comamdo tomara la key privada de la ultima claves en el anillo de confianza(1)
y la exportara al archivo <nombre>.key.asc que es un archivo en codigo asci que puede ser enviado sin problemas
por correo electronico. El comando luego de exportar la clave secreta tambien la elimina del anillo de confianza 
por lo tanto es importante guardar la llave exportada en un lugar seguro. 'OJO' sin la clave secreta sera imposible
desencriptar los archivos.

## encriptar
se corre con el comando ./encriptar 
Al ejecutarse el comando este internamente buscara la clave creada por generar_keys y tomara
el nombre del usuario para autenticar la encriptacion
Suponiendo que existe un directorio ~/automation que a su vez contiene subdirectoros pa1, pa2 ...
este script se encargara de encriptar todos los subdirectorios pa1, pa2,.... creando los
directorios encriptados pa1.tar,pa2.tar, ....

---------------------------------------------------------------------------
Los siguientes comandos estan en desarrollo

## importar_key
Se corre con ./importar_key <nombre>.key.asc
Toma como parametro la llave importada en formato asc y la adiere al anillo de confianza
para poder desencriptar los archivos .tar previamente encriptado con esta clave


## desencriptar
Se ejecuta como sigue: ./desencriptar parametro
Se encargara de desencriptar lo archivos encriptados y extraerlos y moverlos al directorio ~