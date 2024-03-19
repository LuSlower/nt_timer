# SetTimerRes
Una herramienta más para cambiar la resolución del temporizador del sistema en el contexto del proceso de llamada

![image](https://github.com/LuSlower/SetTimerRes/assets/148411728/ff586b35-1470-42a5-b960-9525a69a048f)


## ACTUALMENTE
* Presione ESC para ocultar la GUI, puede hacer clic en el icono de la bandeja para volver a mostrarla tambien añadi un control show alli
* Se permiten solo 7 digitos como máximo en el cuadro de texto, debe ser un numero entero o arrojara un error
* La resolución del temporizador máxima será siempre 5000ns (5ms), asi que cualquier valor por debajo de ese ingresado sera reemplazado automaticamente por el, 
aplica la misma relatividad para el minimo 156250ns
* Hago uso de LoadLibrary y FreeLibrary para maximizar el rendimiento de DllCall(), las llamadas dinamicas constantes pueden bloquear el script
* Tambien hago uso de EmptyWorkingSet y SetProcessWorkingSetSize para recolectar algo de basura (este lenguaje no posee uno)

## PROBLEMAS CONOCIDOS
* Si posees Windows 11 debes tener marcada la casilla GlobalTimerRequest (reiniciar), referencia: [EL GRAN CAMBIO DE REGLAS](https://randomascii.wordpress.com/2020/10/04/windows-timer-resolution-the-great-rule-change/)

* Nose si funciona en Windows 11 y Windows Server 2022+ luego de minimizar/ocultar el proceso, debido a que aun no implemento una forma correcta para llamar dinamicamente a SetProcessInformation, estaré trabajando en aquello

# INFO
* La primera version de este programa se baso en una version de AutoIT3, puedes verificar el archivo [AQUI](AU3/SetTimerRes(OnEvent).au3)
deje de programarlo alli por que sondea demasiado, la GUI siempre tiene que estar en un WHILE, DO/UNITL en cambio AHK usa un mejor manejo de EVENTOS para su GUI lo que hace que el proceso no sondee todo el tiempo, este script posee un rendimiento excelente a comparación del de AutoIT3

## CONTRIBUYENDO
Gracias AutoHotkey y AutoIT Comunmity

## CONSTRUIR
* Descarga SetTimerRes.ahk
* Debes tener instalada la ultima versión de AHK v1.1 (AHK_L), la puedes encontrar en: [AutoHotKey GitHub](https://github.com/AutoHotkey/AutoHotkey)
* Simplemente edite el script a su gusto, mi IDE preferido es SciTE4AHK

## DERECHOS DE AUTOR Y LICENCIA
[LICENCIA](LICENSE)
