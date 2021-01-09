#!/bin/bash
#funcion de ayuda
function ayuda(){
cat << DESCRPCION_AYUDA
SYNOPSIS 
$0 NOMBRE_1 [NOMBRE_2] ... [NOMBRE_N]
DESCRIPCION
Muestra "Hola NOMBRE_1, NOMBRE_2, ... NOMBRE_N!" por pantalla.
CODIGOS DE RETORNO
1 S i el numero de parametros es menor que 1
DESCRPCION_AYUDA
}

# si numero de parametros <= 0

if test $# -le 0 ; then
        echo "Hay que introducir al menos un parametro."
        ayuda
        exit 1
fi

mensaje="Hola"
primero=1

#mientras haya parametros
while [ -n "$1" ];do
        if [ $primero -eq 1 ];then
                mensaje="$mensaje $1"
                primero=0
        else
                mensaje="$mensaje, $1"
        fi
        #pasamos al siguente parametro
        shift
done

#mostramos la salida por la pantalla
echo $mensaje"!"
exit 0
         
