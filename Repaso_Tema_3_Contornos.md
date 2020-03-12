# RepasoContornos
Apuntes de repaso para el examen de Entornos de desarrollo

#### Saber describir el significado de cada uno de los 7 principios de las pruebas del software

	- Las pruebas solo confirman la existencia de los errores que detectan:
	
	Las pruebas solo ven el error cuando se topan con el pero no sifnifica que no exista el error
	- Es imposible probar todos los casos posibles:
	
	Los programas pueden llegar a ser muy grandes y pueden tener mucho código, tanto que resulta imposible probarlo todo, esto nos obliga a elegir bien los caos donde ejecutar la prueba unitaria
	- **La paradoja del pesticida**:
	
	La eficacia en la detección de errores disminuye con el paso del tiempo, no se puede hacer unas pruebas una vez y usarlas para el resto de la vida, hay que ir modificando las pruebas según vaya pasando el tiempo
	- El software se puede probar sin estar terminado:
	
	No se necesita de un programa terminado para empezar a realizar las pruebas sobre el, de hecho cuanto antes empecemos a hacer pruebas mejor.
	- Los errores se ocultan detrás de otros errores:
	
	Es normal que detrás de un código que tiene pocos errores aparezcan mas justo después de corregir los primeros fallos, es por que los primeros fallos no dejaban que el código se ejecutase al 100% y evitaba mostrarnos los demás errores.
	- Las pruebas dependen del contexto:
	
	Para que las pruebas sean efectivas se tiene que tener en cuenta el tipo de proyecto y el tipo de producto sobre el cual se realizan.
	- Un software sin errores es una falacia:
	
	Todo código escrito tiene errores, de hecho si no los encuentras es cuando más deberías desconfiar de el.
	
#### Saber explicar la diferencia entre:
	- Pruebas Funcionales vs no Funcionales:
		- Funcionales: Destinadas a comprobar requisitos funcionales del software
		- No Funcionales: No están destinadas a la comprobación de requisitos ( si el programa es intuitivos, si el código es inteligible, dificultad para migrar a otro entorno...)
	* Manuales vs Automáticas
		- Manuales: Se realizan siguiendo un plan detallado pero sin tener un proceso automático para ejecutarlas.
		- Automáticas: Disponen de un proceso automático que se puede repetir las veces que se quiera de manera cómoda.
	* Caja Negra vs Caja Blanca
		- Caja Negra: Se analiza directamente el código de la aplicación, basándose en la lógica del programa y los caminos que se pueden seguir.
		- Caja Blanca: se llevan a cabo sin saber la estructura ni el funcionamiento del programa. Es fundamental comprobar entradas y resultados.
	* Prueba Unitaria vs Prueba de integración
		- Prueba Unitaria: Pruebas de caja Blanca o Negra que permiten detectar problemas en un módulo individual ( un método o una clase). Al porcentaje de código probado se le denomina cobertura del software.
		- Pruebas de integración: Permiten detectar problemas entre módulos relacionados y probados anteriormente en pruebas individuales.
		
#### Definir Debuggin y utilidades del debug: ver variables, breakpoint, paso a paso ... variantes
	* Debugging: Permite detectar el código que da resultados erroneos en la misma ejecución. Las herramientas de depuración permiten la ejecución controlada del programa:
		- Linea a linea
		- Puntos de interrupción ( la ejecucción  se para donde están definidos)
		- Inspección de variables y expresiones
		- Pila
#### Integración incremental vs no incremental
	* Incremental: se combina el siguiente módulo que se debe probar con los módulos que ya fueron probados. Dos tipos:
		- Ascendente: Se comienza por los módulos Hijo
		- Descendiente: Se comienza por el modulo Raiz
	* No incremental: Se prueba cada módulo por separado y luego se integran todos de una vez para probar el programa completo. Denomidado Big bang
	
#### Pruebas de integración: Cual  es la funcion del módulo impulsor y el módulo ficticio:
	* Módulo impulsor: Es un módulo escrito para permitir simular la llamada a módulos, introducir los datos de prueba en los parámetros de entrada y recoger los resultados de salida.
	* Modulo Ficticio: Simulan la presencia de subordinados ausentes. Deben simular que recogen el control de la llamada y hacen algo con los parámetros que se le pasan ( a través de salidas muestran lo que se iria ejecutando, parámetros que recibe y retornos ficticios que pueden o no depender de los parámetros).
	
#### Definir los siguientes distintos tipos de pruebas de sistema: carga, estrés, compatibilidad, seguridad, tolerancia a fallos.
	* Pruebas de Carga: Observa el comportamiento bajo una cantidad de peticiones esperada, pudiendo tratarse del número de usuarios concurrentes realizando transacciones...
	* Pruebas de sobrecarga o de estrés: Evalúan el comportamiento del sistema al someterlo a una situación limite ( con una demanda excesiva de peticiones, utilización de la memoria máxima, muchos usuarios realizando la misma operación...),
	* Estabilidad: Determina si el sistema puede aguantar una carga esperada continuada ( por posible fuga de memoria).
	* Compatibilidad: Probar el sistema en diferentes entornos o sistemas operativos.
	* Prueba de picos: Observar el comportamiento del sistema cuando varia el número de usuarios, tanto cuando bajan como cuando tienen cambios drásticos en su carga. Recomendado usar herramientas automáticas que simules estos cambios.
	* Seguridad y acceso a datos: Prueban como responde el sistema a ataques externos, como irrupciones no autorizadas o inyección de código malicioso.
	* Tolerancia a fallos y recuperación: Simulan anomalías externas ( Fallos eléctricos, de dispositivos , comunicación...) y ven si el sistema se recupera sin perdida de datos, fallos de integridad y el tiempo que tarda.
	
#### Distinguir entre Pruebas Alfa vs Pruebas Beta
	* Pruebas Alfa: Asociandas al software contratado. Realizadas por el cliente en un entorno controlado bajo la supervisión de la empresa desarrolladora, la cual toma datos de posibles errores y problemas en el uso.
	* Pruebas Beta: Asociadas al software de interés general o software contratado. Es realizada por usuarios. A veces publicadas al público general, con esta etiqueta para que se sepa que puede tener errores.
	
#### Definir Pruebas de Regresión

Son pruebas realizadas por el personal técnico para evitar efectos colaterales. Se aplican cuando hay cambios en el software para verificar que no se producen errores en otras partes del mismo ( algo relativamente normal cuando la integración es incremental, donde habrá que volver a aplicar un subconjunto significativo de las pruebas realizadas a los módulos ya integrados).
	
	
	
