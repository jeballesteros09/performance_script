#!/bin/bash
#Actividad de shell scripting
#Creado por J


comando=""

menu(){

clear

echo "##############################################"
echo "#### SCRIPT DE INFORMACION DE RENDIMIENTO ####"
echo "##############################################"

echo "1. Informacion de CPUs"
echo "2. Informacion de memoria"
echo "3. Informacion de discos"
echo "4. Informacion de red"
echo "5. Toda la informacion de diagnostico"
echo "6. Salir"

read option_1;

case $option_1 in
	1) mostrar_cpu;;
	2) mostrar_memoria;;
	3) mostrar_disco;;
	4) mostrar_red;;
	5) echo "Toda la informacion de diagnostico. Funcion pendiente."
		sub_menu;;
	6) echo "Gracias por usar este script. Hasta luego."
		exit;;
	*) echo "Opcion invalida; por favor seleccione un numero a continuacion: " && menu
esac

}


sub_menu(){


echo "1-Presentar en pantalla."
echo "2-Capturar en archivo."
echo "3-Desplegar en pantalla y guardar en archivo."
echo "4-Volver"

read option_2;

option_3=""

if [ $option_1 -eq 1 ]
then
	option_3="CPU"
fi

if [ $option_1 -eq 2 ]
then
	option_3="MEM"
fi

if [ $option_1 -eq 3 ]
then
	option_3="DSK"
fi

if [ $option_1 -eq 4 ]
then
	option_3="NET"
fi

if [ $option_1 -eq 5 ]
then
	option_3="ALL"
fi

cierre="Operacion completada exitosamente. Script finalizado."

case $option_2 in

	1) echo -e "USUARIO: $(whoami) \n SISTEMA: $(cat /etc/os-release) \n VERSION DE KERNEL: $(uname -r) \n INFORMACION DE $option_3: \n $comando" && echo $cierre;;
	2) echo -e "USUARIO: $(whoami) \n SISTEMA: $(cat /etc/os-release) \n VERSION DE KERNEL: $(uname -r) \n INFORMACION DE $option_3: \n $comando" > "DIAG_"$option_3"_$(hostname)_$(date +'%Y%m%d_%H%M%S')".txt && echo $cierre;;
	3) echo -e "USUARIO: $(whoami) \n SISTEMA: $(cat /etc/os-release) \n VERSION DE KERNEL: $(uname -r) \n INFORMACION DE $option_3: \n $comando" && echo -e "INFORMACION DE $option_3: \n $comando" > "DIAG_"$option_3"_$(hostname)_$(date +'%Y%m%d_%H%M%S')".txt && echo $cierre;;
	4) menu;;
	*) clear &&  echo "Opcion invalida; por favor seleccione un numero a continuacion: \n" && sub_menu
esac
}


mostrar_cpu(){

clear

echo "############################"
echo "#### INFORMACION DE CPU ####"
echo "############################"

comando=$(lscpu)

sub_menu

}

mostrar_memoria(){

clear

echo "################################"
echo "#### INFORMACION DE MEMORIA ####"
echo "################################"

comando=$(free -mh)

sub_menu

}

mostrar_disco(){

clear

echo "###############################"
echo "#### INFORMACION DE DISCOS ####"
echo "###############################"

comando=$(df -h && lsusb)

sub_menu

}

mostrar_red(){

clear

echo "############################"
echo "#### INFORMACION DE RED ####"
echo "############################"

comando=$(ip a)

sub_menu

}

mostrar_todo(){

clear

echo "############################################"
echo "#### TODA LA INFORMACION DE DIAGNOSTICO ####"
echo "############################################"



}


menu
