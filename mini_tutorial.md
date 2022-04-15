Para encriptar los archivos pa* de la carpeta /home/user/automation
hacemos uso del siguiente algoritmo.
Cabe destacar que gpg debe de estar instalado en la maquina y los 
comandos deben tener permisos de ejecucion.

1-./generar_keys
    Con este comando crearemos nuestro par de llaves publicas/privadas
    el usuario debe seguir el interativo, se le sugiere que tome las opciones 
    que le sugiere el interactivo.

2- ./exportar_key
    Con este comando se exportara la llave al archivo <user>.key.asc y luego 
    eliminara la llave secreta del anillo de confianza local.

3- ./encriptar
    Este comando encriptara todas las carpetas pa* y transformara creara las
    las carpetas encriptadas pa*.tar ejemplo pa1 generara pa1.tar y asi...
    Este comando en un futuro tambien eliminara las carpetas pa^ ya que no
    tiene sentido que existan desencriptadas

4- ./importar_key
    Este comando se ejecutara cuando el usuario necesite desencriptar una
    carpeta ya que sin la llave secreta en el anillo de confianza seria imposible
    la desencriptacion.

    Ya habiendose importado la llave, el usuario podria hacer uso del comando
    'gpgtar -d <archivo>.tar el cual desencriptara la carpeta <archivo>.tar y
    mandara el contenido a la carpeta archivo._1_/ la cual contendra dentro de si
    la carpeta original desencriptada <archivo>

    en esta fase de prueba se sugiere que el usuario desencripte y mueva las capetas
    ya desencriptadas manualmente
    