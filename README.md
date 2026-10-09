# Respuestas Evaluacion 2 Introduccion a Tecnologias de Informacion
--- 
## Nombres: Jose Ricardo Guerrero Gamez  y Andres Cardenas
---
**## Introducción a Tecnologías de Información**

---

**## Pregunta 1**

**Respuesta correcta:** C. 9000 milisegundos.

**Justificación:** La duración total de un ciclo completo en un sistema secuencial como un semáforo se obtiene sumando los tiempos individuales programados para cada estado. Al sumar el tiempo de verde, amarillo y rojo, se completa el ciclo establecido.

---

**## Pregunta 2**

**Respuesta correcta:** C. Ejecuta el subcomando compile e indica el identificador de la placa.

**Justificación:** El subcomando compile de Arduino CLI se emplea específicamente para verificar la sintaxis y compilar el código fuente del sketch. Para ello, es indispensable especificar el identificador de la placa objetivo mediante el parámetro correspondiente.

---

**## Pregunta 3**

**Respuesta correcta:** C. Los LEDs de los bits 1, 2 y 3.

**Justificación:** Al procesar el número trece mediante operaciones lógicas de desplazamiento a la derecha y máscaras de bits, se evalúa su equivalente binario. Esto determina qué posiciones específicas de los LEDs de 4 bits deben activarse.

---

**## Pregunta 4**

**Respuesta correcta:** B. Ignora nuevas lecturas del pulsador durante un breve intervalo tras detectar el primer cambio.

**Justificación:** Las transiciones eléctricas espurias generadas por el rebote mecánico del pulsador se controlan mediante software. Esto se logra ignorando lecturas adicionales durante un pequeño intervalo posterior al primer flanco detectado.

---

**## Pregunta 5**

**Respuesta correcta:** D. 16 patrones.

**Justificación:** Un conmutador DIP switch de 4 canales ofrece un total de combinaciones posibles basadas en potencias binarias. Con 4 canales independientes, se pueden configurar 16 opciones distintas entre patrones y velocidades.

---

**## Pregunta 6**

**Respuesta correcta:** D. Nivel LOW porque el contacto cerrado impone sobre el pin una tensión de cero voltios.

**Justificación:** Al colocar el canal en posición ON, el pin se conecta físicamente a tierra. Esto vence la resistencia de pull-up interna y fuerza de manera directa un nivel lógico bajo en la lectura digital del microcontrolador.

---

**## Pregunta 7**

**Respuesta correcta:** A. 480 milisegundos.

**Justificación:** El cálculo de la duración total del efecto de persecución se realiza multiplicando el tiempo asignado a cada paso por el número total de transiciones netas. Así se define el ciclo completo de ida y vuelta.

---

**## Pregunta 8**

**Respuesta correcta:** A. Agregar el usuario al grupo dialout y reiniciar su sesión en Debian 13.

**Justificación:** En entornos operativos Linux como Debian 13, los permisos de acceso a los puertos serie USB están estrictamente restringidos. Para habilitar la comunicación, el usuario actual debe pertenecer al grupo de privilegios dialout.

---

**## Pregunta 9**

**Respuesta correcta:** D. 204.

**Justificación:** La función map se encarga de convertir de forma lineal y proporcional un valor proveniente de un rango analógico de entrada hacia el rango de salida de la modulación PWM.

---

**## Pregunta 10**

**Respuesta correcta:** B. El monitor muestrea los bits con una tasa distinta a la configurada en el sketch.

**Justificación:** La comunicación serial asíncrona exige que tanto el microcontrolador como el monitor compartan idéntica velocidad en baudios. Una discrepancia temporal en el muestreo genera directamente la lectura de caracteres ilegibles.

---

**## Pregunta 11**

**Respuesta correcta:** C. 4,7 segundos.

**Justificación:** La constante de tiempo en un circuito RC se calcula multiplicando el valor de la resistencia por la capacitancia del condensador. Al multiplicar los ohmios por los faradios, se obtiene el tiempo característico.

---

**## Pregunta 12**

**Respuesta correcta:** A. Solo la declaración 1 es verdadera.

**Justificación:** Los procesos de carga y descarga en condensadores siguen un comportamiento exponencial válido. No obstante, al cumplirse una sola constante de tiempo, el capacitor alcanza el 63.2% de la fuente y no el total.

---

**## Pregunta 13**

**Respuesta correcta:** B. 4,3 miliamperios.

**Justificación:** Aplicando la ley de Ohm en la malla de base del transistor, se resta la caída de tensión base-emisor a la del pin digital. El resultado se divide entre el valor de la resistencia de base configurada.

---

**## Pregunta 14**

**Respuesta correcta:** B. Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.

**Justificación:** Existe una relación directa de causa y efecto donde el diodo de protección absorbe los picos de corriente inversa generados por la bobina del motor. Esto evita daños físicos en el transistor de conmutación.

---

**## Pregunta 15**

**Respuesta correcta:** C. Pin digital 9.

**Justificación:** En la estructura de hardware del Arduino UNO R3, los pines habilitados con capacidad de salida PWM mediante circuitería interna están debidamente identificados, siendo el pin 9 uno de ellos.

---

**## Pregunta 16**

**Respuesta correcta:** D. Porque la demanda de la bobina excede la capacidad de corriente que soporta el pin.

**Justificación:** La corriente máxima que soporta de forma segura un pin de E/S del microcontrolador es limitada. Puesto que la bobina demanda una intensidad superior, se requiere un transistor de interfaz para proteger la placa.

---

**## Pregunta 17**

**Respuesta correcta:** B. Solo la declaración 2 es verdadera.

**Justificación:** El relé proporciona un aislamiento galvánico que separa lógicamente el control de la potencia, haciendo falsa la primera afirmación. La segunda es correcta porque el diodo limita los picos inductivos.

---

**## Pregunta 18**

**Respuesta correcta:** A. Los cierres y aperturas repetidos del relé cuando la señal fluctúa alrededor de un único valor.

**Justificación:** Implementar dos umbrales de conmutación diferenciados introduce histéresis en el sistema. Esto evita el parpadeo o traqueteo constante del relé cuando la señal del sensor experimenta pequeñas oscilaciones.

---

**## Pregunta 19**

**Respuesta correcta:** D. El pin 2 lee nivel LOW y el sketch activa el buzzer con la función tone().

**Justificación:** Al abrirse la puerta se interrumpe la alimentación directa de cinco voltios y la resistencia pull-down tira del pin hacia tierra. Esta transición a nivel bajo es interpretada por el programa para activar la alarma.

---

**## Pregunta 20**

**Respuesta correcta:** B. La afirmación es verdadera, mientras que la razón es una proposición falsa.

**Justificación:** La función tone genera ondas cuadradas oscilantes para frecuencias audibles en el buzzer pasivo, lo que desmiente que mantenga un nivel alto estático continuo hasta la ejecución de la desactivación.

---

**## Pregunta 21**

**Respuesta correcta:** A. Disminuye porque la LDR aumenta su resistencia y la resistencia fija recibe menos tensión.

**Justificación:** Al reducirse la iluminación ambiental, la fotorresistencia incrementa su resistencia óhmica. Esto provoca una mayor caída de tensión en la LDR y reduce el voltaje proporcional que percibe el pin analógico.

---

**## Pregunta 22**

**Respuesta correcta:** A. 2 LEDs.

**Justificación:** La función de mapeo convierte proporcionalmente la lectura analógica al rango de salida de los LEDs. Al truncar los decimales resultantes de la operación matemática entera, se determina la cantidad exacta encendida.

---

**## Pregunta 23**

**Respuesta correcta:** C. II, I, III, IV.

**Justificación:** Por normativas de seguridad vial y control secuencial, el sistema de tráfico debe transicionar primero a luz amarilla de advertencia, detenerse en rojo, habilitar el paso peatonal y luego reiniciar el ciclo.

---

**## Pregunta 24**

**Respuesta correcta:** B. La placa se reinicia al abrirse el puerto serie y tarda unos segundos en iniciar el sketch.

**Justificación:** Por diseño físico en las placas basadas en microcontroladores AVR con interfaz USB, abrir una conexión serial activa un mecanismo de auto-reset que reinicia la ejecución, demorando la recepción inicial.

---

**## Pregunta 25**

**Respuesta correcta:** D. Ejecutar core update-index y core install con el paquete arduino:avr.

**Justificación:** Las instalaciones limpias de la interfaz de comandos carecen de paquetes de arquitectura preconfigurados. Es necesario actualizar los índices y descargar explícitamente el soporte de hardware mediante los comandos de núcleo.