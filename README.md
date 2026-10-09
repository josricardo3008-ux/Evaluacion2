# Respuestas Evaluacion 2 Introduccion a Tecnologias de Informacion
---
## Nombre: Jose Ricardo Guerrero Gamez
---
## Introducción a Tecnologías de Información

---

## Pregunta 1

Un Técnico desarrolla en la terminal de la Raspberry Pi 5 con Debian 13 un sketch .ino para una maqueta de Internet de las Cosas que simula un semáforo vehicular de tres tiempos en la placa Arduino UNO R3. El sketch mantiene el verde durante 5000 milisegundos, el amarillo durante 2000 milisegundos y el rojo durante 4000 milisegundos mediante la función delay(). Al contrastar la temporización real con la esperada en el monitor serial de Arduino CLI (interfaz de línea de comandos), qué duración total tiene un ciclo completo?
- **A.** 5000 milisegundos.
- **B.** 7000 milisegundos.
- **C.** 9000 milisegundos.
- **D.** 11000 milisegundos.

**Respuesta correcta:** C 9000 milisegundos.

**Justificación:** La duración total de un ciclo completo en un sistema secuencial como un semáforo se obtiene sumando los tiempos individuales programados para cada estado. Al sumar el tiempo de verde, amarillo y rojo, se completa el ciclo establecido.

---

## Pregunta 2

En la terminal de la Raspberry Pi 5 con Debian 13, un Tecnólogo ubica la carpeta del sketch semaforo_tres_tiempos, que contiene el archivo semaforo_tres_tiempos.ino para la placa Arduino UNO R3. Antes de conectar la placa, necesita detectar errores de sintaxis del código mediante Arduino CLI (interfaz de línea de comandos). Qué acción ejecuta para lograrlo?
- **A.** Ejecuta el subcomando upload e indica el puerto serie de la placa.
- **B.** Ejecuta el subcomando board attach e indica el identificador de la placa.
- **C.** Ejecuta el subcomando compile e indica el identificador de la placa.
- **D.** Ejecuta el subcomando sketch archive e indica la carpeta del sketch.

**Respuesta correcta:** C Ejecuta el subcomando compile e indica el identificador de la placa.

**Justificación:** El subcomando compile de Arduino CLI se emplea específicamente para verificar la sintaxis y compilar el código fuente del sketch. Para ello, es indispensable especificar el identificador de la placa objetivo mediante el parámetro correspondiente.

---

## Pregunta 3

Un Técnico programa un contador binario de 4 bits en Arduino UNO R3 desde la terminal de la Raspberry Pi 5 con Debian 13. Cada pulsación incrementa en uno la variable contador, y el sketch enciende el LED del bit i cuando el resultado de desplazar contador i posiciones a la derecha y aplicar la operación lógica AND bit a bit con el valor 1 es igual a 1. Tras trece pulsaciones, cuáles LEDs permanecen encendidos?
- **A.** Los LEDs de los bits 0, 1 y 2.
- **B.** Los LEDs de los bits 0, 1 y 3.
- **C.** Los LEDs de los bits 1, 2 y 3.
- **D.** Los LEDs de los bits 0, 2 y 3.

**Respuesta correcta:** C Los LEDs de los bits 1, 2 y 3.

**Justificación:** Al procesar el número trece mediante operaciones lógicas de desplazamiento a la derecha y máscaras de bits, se evalúa su equivalente binario. Esto determina qué posiciones específicas de los LEDs de 4 bits deben activarse.

---

## Pregunta 4

Un contador binario de 4 bits en Arduino UNO R3 incrementa su valor en más de una unidad cada vez que el Tecnólogo presiona el pulsador mecánico, porque el contacto genera varias transiciones eléctricas durante unos pocos milisegundos. El sketch .ino se compila y se carga desde la terminal de la Raspberry Pi 5 con Debian 13 mediante Arduino CLI (interfaz de línea de comandos). Qué técnica de software corrige este comportamiento?
- **A.** Reemplaza la lectura digital del pulsador por una lectura analógica de mayor resolución.
- **B.** Ignora nuevas lecturas del pulsador durante un breve intervalo tras detectar el primer cambio.
- **C.** Aumenta el valor de las resistencias de los LEDs de 220 ohmios a 10 kiloohmios.
- **D.** Declara la variable contador con un tipo de dato de mayor capacidad de almacenamiento.

**Respuesta correcta:** B Ignora nuevas lecturas del pulsador durante un breve intervalo tras detectar el primer cambio.

**Justificación:** Las transiciones eléctricas espurias generadas por el rebote mecánico del pulsador se controlan mediante software. Esto se logra ignorando lecturas adicionales durante un pequeño intervalo posterior al primer flanco detectado.

---

## Pregunta 5

Un Técnico conecta un DIP switch de 4 canales a la placa Arduino UNO R3 para un tablero de señalización. Los canales 1 y 2 seleccionan el patrón de encendido de 4 LEDs mediante una tabla de verdad, y los canales 3 y 4 seleccionan la velocidad del efecto. El sketch .ino se carga desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos). Cuántos patrones distintos permite seleccionar el tablero?
- **A.** 4 patrones.
- **B.** 8 patrones.
- **C.** 12 patrones.
- **D.** 16 patrones.

**Respuesta correcta:** D 16 patrones.

**Justificación:** Un conmutador DIP switch de 4 canales ofrece un total de combinaciones posibles basadas en potencias binarias. Con 4 canales independientes, se pueden configurar 16 opciones distintas entre patrones y velocidades.

---

## Pregunta 6

Un Tecnólogo conecta cada canal de un DIP switch entre un pin digital de Arduino UNO R3 y tierra (referencia de 0 voltios). En el sketch .ino, cada pin se declara con el modo INPUT_PULLUP, que activa una resistencia interna conectada a 5 voltios. Si un canal se coloca en la posición ON, que cierra el contacto con tierra, entonces la función digitalRead() sobre ese pin devuelve:
- **A.** Nivel HIGH porque la resistencia interna mantiene el pin conectado a 5 voltios.
- **B.** Un valor indeterminado porque el pin permanece flotante, desconectado de toda referencia.
- **C.** Un nivel alternante entre HIGH y LOW porque el contacto cerrado genera oscilaciones.
- **D.** Nivel LOW porque el contacto cerrado impone sobre el pin una tensión de cero voltios.

**Respuesta correcta:** D Nivel LOW porque el contacto cerrado impone sobre el pin una tensión de cero voltios.

**Justificación:** Al colocar el canal en posición ON, el pin se conecta físicamente a tierra. Esto vence la resistencia de pull-up interna y fuerza de manera directa un nivel lógico bajo en la lectura digital del microcontrolador.

---

## Pregunta 7

Un Técnico programa un efecto de luces de persecución con 6 LEDs en Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian 13. El efecto enciende un LED por paso durante 80 milisegundos, recorre los LEDs de izquierda a derecha y regresa, con cada LED de los extremos encendido una sola vez por ciclo. Cuánto dura un ciclo completo de ida y vuelta?
- **A.** 480 milisegundos.
- **B.** 800 milisegundos.
- **C.** 880 milisegundos.
- **D.** 960 milisegundos.

**Respuesta correcta:** A 480 milisegundos.

**Justificación:** El cálculo de la duración total del efecto de persecución se realiza multiplicando el tiempo asignado a cada paso por el número total de transiciones netas. Así se define el ciclo completo de ida y vuelta.

---

## Pregunta 8

Un Tecnólogo escribe en la Raspberry Pi 5 con Debian 13 el sketch .ino de un efecto de luces para la placa Arduino UNO R3. La compilación finaliza con éxito, pero al ejecutar el subcomando upload de Arduino CLI (interfaz de línea de comandos), el sistema muestra un mensaje de permiso denegado sobre el dispositivo /dev/ttyACM0. Qué acción habilita el acceso al puerto serie para este usuario?
- **A.** Agregar el usuario al grupo dialout y reiniciar su sesión en Debian 13.
- **B.** Reinstalar el núcleo arduino:avr mediante el subcomando core install.
- **C.** Modificar el identificador de la placa por el de otro modelo de Arduino.
- **D.** Aumentar la velocidad de transmisión del puerto a 115200 baudios.

**Respuesta correcta:** A Agregar el usuario al grupo dialout y reiniciar su sesión en Debian 13.

**Justificación:** En entornos operativos Linux como Debian 13, los permisos de acceso a los puertos serie USB están estrictamente restringidos. Para habilitar la comunicación, el usuario actual debe pertenecer al grupo de privilegios dialout.

---

## Pregunta 9

Un Técnico conecta un potenciómetro de 10 kiloohmios al pin analógico A0 de Arduino UNO R3 para atenuar un LED mediante modulación por ancho de pulso (PWM). El conversor analógico-digital (ADC) de 10 bits entrega una lectura de 819, y el sketch .ino la convierte al rango de 0 a 255 con la función map() antes de llamar a analogWrite(). El sketch se compila y se carga desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Qué valor recibe analogWrite()?
- **A.** 102.
- **B.** 128.
- **C.** 191.
- **D.** 204.

**Respuesta correcta:** D 204.

**Justificación:** La función map se encarga de convertir de forma lineal y proporcional un valor proveniente de un rango analógico de entrada hacia el rango de salida de la modulación PWM.

---

## Pregunta 10

Un Tecnólogo carga desde la terminal de la Raspberry Pi 5 con Debian 13, mediante Arduino CLI (interfaz de línea de comandos), un sketch .ino que inicia la comunicación serial a 9600 baudios para mostrar las lecturas de un potenciómetro. Al abrir el monitor serial con una configuración de 115200 baudios, la terminal presenta caracteres ilegibles. Cuál es la causa de este comportamiento?
- **A.** El pin analógico A0 convierte la señal con una resolución menor a la declarada.
- **B.** El monitor muestrea los bits con una tasa distinta a la configurada en el sketch.
- **C.** El cable USB entrega la tensión con polaridad invertida.
- **D.** El sistema Debian 13 limita el puerto serie a una velocidad de 1200 baudios.

**Respuesta correcta:** B El monitor muestrea los bits con una tasa distinta a la configurada en el sketch.

**Justificación:** La comunicación serial asíncrona exige que tanto el microcontrolador como el monitor compartan idéntica velocidad en baudios. Una discrepancia temporal en el muestreo genera directamente la lectura de caracteres ilegibles.

---

## Pregunta 11

Un Técnico analiza la carga de un capacitor electrolítico de 470 microfaradios a través de una resistencia de 10 kiloohmios, alimentados con 5 voltios desde la placa Arduino UNO R3. Desde la terminal de la Raspberry Pi 5 con Debian 13, compila y carga el sketch .ino con Arduino CLI y recibe las lecturas en el monitor serial. Qué valor tiene la constante de tiempo del circuito RC (resistencia-capacitor)?
- **A.** 0,47 segundos.
- **B.** 2,35 segundos.
- **C.** 4,7 segundos.
- **D.** 47 segundos.

**Respuesta correcta:** C 4,7 segundos.

**Justificación:** La constante de tiempo en un circuito RC se calcula multiplicando el valor de la resistencia por la capacitancia del condensador. Al multiplicar los ohmios por los faradios, se obtiene el tiempo característico.

---

## Pregunta 12

Un Tecnólogo grafica desde el monitor serial de Arduino CLI (interfaz de línea de comandos), ejecutado en la Raspberry Pi 5 con Debian 13, las lecturas de analogRead() del voltaje de un capacitor en un circuito RC conectado a la placa Arduino UNO R3.
Declaración 1: Durante la descarga, las lecturas disminuyen de forma exponencial hacia cero.
Declaración 2: Al transcurrir una constante de tiempo de carga, el capacitor alcanza el 100% de la tensión de la fuente.
De acuerdo con el comportamiento del circuito, se puede afirmar que:
- **A.** Solo la declaración 1 es verdadera.
- **B.** Solo la declaración 2 es verdadera.
- **C.** Ambas declaraciones son verdaderas.
- **D.** Ambas declaraciones son falsas.

**Respuesta correcta:** A Solo la declaración 1 es verdadera.

**Justificación:** Los procesos de carga y descarga en condensadores siguen un comportamiento exponencial válido. No obstante, al cumplirse una sola constante de tiempo, el capacitor alcanza el 63.2% de la fuente y no el total.

---

## Pregunta 13

Un Técnico conmuta un LED con un transistor NPN 2N2222 desde un pin digital de Arduino UNO R3 que entrega 5 voltios, mediante una resistencia de base de 1 kiloohmio. El sketch .ino se carga desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Si la unión base-emisor presenta una caída de 0,7 voltios en saturación, qué corriente de base circula aproximadamente?
- **A.** 0,7 miliamperios.
- **B.** 4,3 miliamperios.
- **C.** 5,0 miliamperios.
- **D.** 13,6 miliamperios.

**Respuesta correcta:** B 4,3 miliamperios.

**Justificación:** Aplicando la ley de Ohm en la malla de base del transistor, se resta la caída de tensión base-emisor a la del pin digital. El resultado se divide entre el valor de la resistencia de base configurada.

---

## Pregunta 14

Un Tecnólogo controla un motor de corriente continua con un transistor NPN TIP31 y un diodo 1N4007 conectado en paralelo con el motor, mediante un sketch .ino con modulación por ancho de pulso (PWM) cargado en Arduino UNO R3 desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Se analizan la siguiente afirmación y la siguiente razón:
**AFIRMACIÓN:** El diodo protege al transistor cuando el pin PWM deja de energizar el motor.
**PORQUE**
**RAZÓN:** La bobina del motor genera una tensión inducida de polaridad inversa al interrumpirse la corriente que la atraviesa.
Con base en el análisis, se concluye que:
- **A.** Ambas proposiciones son verdaderas, pero la razón es independiente de la afirmación.
- **B.** Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.
- **C.** La afirmación es verdadera, mientras que la razón es una proposición falsa.
- **D.** La afirmación es falsa, mientras que la razón es una proposición verdadera.

**Respuesta correcta:** B Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.

**Justificación:** Existe una relación directa de causa y efecto donde el diodo de protección absorbe los picos de corriente inversa generados por la bobina del motor. Esto evita daños físicos en el transistor de conmutación.

---

## Pregunta 15

Un Técnico controla la velocidad de un motor de corriente continua mediante modulación por ancho de pulso (PWM) con la función analogWrite() en un sketch .ino para Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos). La base del transistor de potencia se conecta a un pin digital con salida PWM. Cuál pin digital de la placa tiene esta capacidad?
- **A.** Pin digital 4.
- **B.** Pin digital 7.
- **C.** Pin digital 9.
- **D.** Pin digital 12.

**Respuesta correcta:** C Pin digital 9.

**Justificación:** En la estructura de hardware del Arduino UNO R3, los pines habilitados con capacidad de salida PWM mediante circuitería interna están debidamente identificados, siendo el pin 9 uno de ellos.

---

## Pregunta 16

Un Tecnólogo activa un relé electromecánico de 5 voltios, con una bobina que demanda 72 miliamperios, para energizar un motor de corriente continua desde una fuente independiente. Cada pin digital de Arduino UNO R3 suministra como máximo 40 miliamperios. El sketch .ino se carga desde la terminal de la Raspberry Pi 5 con Debian 13 mediante Arduino CLI (interfaz de línea de comandos). Por qué el pin digital controla un transistor de disparo en lugar de conectarse a la bobina?
- **A.** Porque la bobina necesita una tensión alterna que el transistor genera desde el pin.
- **B.** Porque el transistor eleva la tensión del pin de 5 voltios al valor nominal del motor.
- **C.** Porque los contactos del relé requieren una señal modulada con frecuencia superior a 490 hertz.
- **D.** Porque la demanda de la bobina excede la capacidad de corriente que soporta el pin.

**Respuesta correcta:** D Porque la demanda de la bobina excede la capacidad de corriente que soporta el pin.

**Justificación:** La corriente máxima que soporta de forma segura un pin de E/S del microcontrolador es limitada. Puesto que la bobina demanda una intensidad superior, se requiere un transistor de interfaz para proteger la placa.

---

## Pregunta 17

Un Técnico energiza un motor de corriente continua con un relé electromecánico gobernado por un pin digital de Arduino UNO R3, mediante un sketch .ino cargado desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Sobre el circuito se formulan las siguientes declaraciones:
Declaración 1: La bobina del relé y los contactos del motor comparten el mismo circuito eléctrico.
Declaración 2: El diodo en paralelo con la bobina limita el pico de tensión generado al interrumpirse su corriente.
De acuerdo con la especificación, se puede afirmar que:
- **A.** Solo la declaración 1 es verdadera.
- **B.** Solo la declaración 2 es verdadera.
- **C.** Ambas declaraciones son verdaderas.
- **D.** Ambas declaraciones son falsas.

**Respuesta correcta:** B Solo la declaración 2 es verdadera.

**Justificación:** El relé proporciona un aislamiento galvánico que separa lógicamente el control de la potencia, haciendo falsa la primera afirmación. La segunda es correcta porque el diodo limita los picos inductivos.

---

## Pregunta 18

Un Técnico simula un sistema de riego con un potenciómetro como sensor de humedad y un relé que energiza una bomba simulada con un motor de corriente continua. El sketch .ino de Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos), activa el relé cuando la lectura supera 700 y lo desactiva cuando desciende por debajo de 600. Qué situación evita esta diferencia entre los dos umbrales?
- **A.** Los cierres y aperturas repetidos del relé cuando la señal fluctúa alrededor de un único valor.
- **B.** La pérdida de resolución del conversor analógico-digital cuando la lectura supera 512.
- **C.** El reinicio automático de la placa cada vez que el usuario abre el monitor serial.
- **D.** La sobrecarga del puerto USB de la Raspberry Pi 5 durante el proceso de compilación.

**Respuesta correcta:** A Los cierres y aperturas repetidos del relé cuando la señal fluctúa alrededor de un único valor.

**Justificación:** Implementar dos umbrales de conmutación diferenciados introduce histéresis en el sistema. Esto evita el parpadeo o traqueteo constante del relé cuando la señal del sensor experimenta pequeñas oscilaciones.

---

## Pregunta 19

Un Técnico conecta un microinterruptor que cierra el contacto entre el pin 2 y 5 voltios mientras la puerta permanece cerrada, con una resistencia pull-down en el mismo pin. El sketch .ino de Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos), activa un buzzer con la función tone() cuando detecta la apertura. Si la puerta se abre, entonces:
- **A.** El pin 2 lee nivel HIGH y el sketch silencia el buzzer con la función noTone().
- **B.** El pin 2 lee nivel LOW y el sketch silencia el buzzer con la función noTone().
- **C.** El pin 2 lee nivel HIGH y el sketch activa el buzzer con la función tone().
- **D.** El pin 2 lee nivel LOW y el sketch activa el buzzer con la función tone().

**Respuesta correcta:** D El pin 2 lee nivel LOW y el sketch activa el buzzer con la función tone().

**Justificación:** Al abrirse la puerta se interrumpe la alimentación directa de cinco voltios y la resistencia pull-down tira del pin hacia tierra. Esta transición a nivel bajo es interpretada por el programa para activar la alarma.

---

## Pregunta 20

Un Tecnólogo programa una alarma con un buzzer pasivo en un sketch .ino para Arduino UNO R3, compilado y cargado desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Se analizan la siguiente afirmación y la siguiente razón:
**AFIRMACIÓN:** La función tone() permite que un buzzer pasivo emita un sonido de frecuencia definida.
**PORQUE**
**RAZÓN:** La función entrega en el pin un nivel HIGH constante hasta que se ejecuta la función noTone().
Con base en el análisis, se concluye que:
- **A.** Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.
- **B.** La afirmación es verdadera, mientras que la razón es una proposición falsa.
- **C.** Ambas proposiciones son verdaderas, pero la razón es independiente de la afirmación.
- **D.** La afirmación es falsa, mientras que la razón es una proposición verdadera.

**Respuesta correcta:** B La afirmación es verdadera, mientras que la razón es una proposición falsa.

**Justificación:** La función tone genera ondas cuadradas oscilantes para frecuencias audibles en el buzzer pasivo, lo que desmiente que mantenga un nivel alto estático continuo hasta la ejecución de la desactivación.

---

## Pregunta 21

Un Técnico construye un alumbrado inteligente con un divisor de voltaje: una fotorresistencia (LDR) entre 5 voltios y el pin analógico A0 de Arduino UNO R3, y una resistencia de 10 kiloohmios entre A0 y tierra. El sketch .ino se carga desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos). Si la luz ambiental disminuye, entonces la lectura de A0:
- **A.** disminuye porque la LDR aumenta su resistencia y la resistencia fija recibe menos tensión.
- **B.** disminuye porque la LDR reduce su resistencia y la resistencia fija recibe menos tensión.
- **C.** aumenta porque la LDR aumenta su resistencia y la resistencia fija recibe más tensión.
- **D.** aumenta porque la LDR reduce su resistencia y la resistencia fija recibe más tensión.

**Respuesta correcta:** A disminuye porque la LDR aumenta su resistencia y la resistencia fija recibe menos tensión.

**Justificación:** Al reducirse la iluminación ambiental, la fotorresistencia incrementa su resistencia óhmica. Esto provoca una mayor caída de tensión en la LDR y reduce el voltaje proporcional que percibe el pin analógico.

---

## Pregunta 22

Un Tecnólogo construye un indicador de nivel tipo VU-meter con 5 LEDs y un potenciómetro conectado al pin analógico A0 de Arduino UNO R3. El sketch .ino, cargado desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos), aplica la función map() para convertir la lectura de 0 a 1023 en una cantidad de LEDs de 0 a 5, descartando los decimales. Si la lectura vale 450, cuántos LEDs permanecen encendidos?
- **A.** 2 LEDs.
- **B.** 3 LEDs.
- **C.** 4 LEDs.
- **D.** 5 LEDs.

**Respuesta correcta:** A 2 LEDs.

**Justificación:** La función de mapeo convierte proporcionalmente la lectura analógica al rango de salida de los LEDs. Al truncar los decimales resultantes de la operación matemática entera, se determina la cantidad exacta encendida.

---

## Pregunta 23

Un Técnico programa en Arduino UNO R3 un cruce peatonal coordinado: un script en Python ejecutado en la Raspberry Pi 5 con Debian 13 se comunica por puerto serie con el sketch .ino cargado mediante Arduino CLI (interfaz de línea de comandos). Con el semáforo vehicular en verde, el peatón presiona el pulsador. La secuencia de eventos es:
I. El semáforo vehicular pasa a rojo.
II. El semáforo vehicular pasa a amarillo.
III. El semáforo peatonal pasa a verde.
IV. El semáforo peatonal vuelve a rojo y el vehicular a verde.
En qué orden ocurren los eventos?
- **A.** I, II, III, IV.
- **B.** II, III, I, IV.
- **C.** II, I, III, IV.
- **D.** III, II, I, IV.

**Respuesta correcta:** C II, I, III, IV.

**Justificación:** Por normativas de seguridad vial y control secuencial, el sistema de tráfico debe transicionar primero a luz amarilla de advertencia, detenerse en rojo, habilitar el paso peatonal y luego reiniciar el ciclo.

---

## Pregunta 24

Un Tecnólogo ejecuta en la Raspberry Pi 5 con Debian 13 un script en Python que abre el puerto serie de la placa Arduino UNO R3 con la biblioteca pyserial y envía de inmediato el comando para encender un LED. El sketch .ino se cargó previamente con Arduino CLI (interfaz de línea de comandos) y recibe comandos con la función Serial.read(), pero el LED permanece apagado en el primer envío. Cuál es la causa más probable?
- **A.** El método write() de pyserial transmite solo números decimales de punto flotante en cada envío.
- **B.** La placa se reinicia al abrirse el puerto serie y tarda unos segundos en iniciar el sketch.
- **C.** La Raspberry Pi 5 envía los comandos por sus pines de propósito general y omite el puerto USB.
- **D.** El LED necesita una resistencia de 10 kiloohmios para reconocer los datos seriales recibidos.

**Respuesta correcta:** B La placa se reinicia al abrirse el puerto serie y tarda unos segundos en iniciar el sketch.

**Justificación:** Por diseño físico en las placas basadas en microcontroladores AVR con interfaz USB, abrir una conexión serial activa un mecanismo de auto-reset que reinicia la ejecución, demorando la recepción inicial.

---

## Pregunta 25

Un Técnico instala Arduino CLI (interfaz de línea de comandos) en una Raspberry Pi 5 con Debian 13 recién configurada y crea el sketch .ino de un semáforo vehicular para Arduino UNO R3. Al ejecutar el subcomando compile con el identificador arduino:avr:uno, la terminal informa que el soporte de la placa está ausente. Qué acción permite continuar con la compilación?
- **A.** Ejecutar el subcomando board list para registrar la placa en el sistema.
- **B.** Ejecutar el subcomando sketch new para generar una nueva carpeta de sketch.
- **C.** Ejecutar el subcomando upload con el puerto serie de la placa conectada.
- **D.** Ejecutar core update-index y core install con el paquete arduino:avr.

**Respuesta correcta:** D Ejecutar core update-index y core install con el paquete arduino:avr.

**Justificación:** Las instalaciones limpias de la interfaz de comandos carecen de paquetes de arquitectura preconfigurados. Es necesario actualizar los índices y descargar explícitamente el soporte de hardware mediante los comandos de núcleo.
