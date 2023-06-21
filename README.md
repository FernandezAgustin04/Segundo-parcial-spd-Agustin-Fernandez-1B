# Segundo-parcial-spd-Agustin-Fernandez-1B
## Librerías utilizadas

El código utiliza las siguientes librerías:

- `LiquidCrystal.h`: Librería para controlar pantallas LCD.
- `Servo.h`: Librería para controlar servomotores.
- `IRremote.h`: Librería para recibir señales infrarrojas.

## Definición de pines

Se definen los siguientes pines para la conexión de los componentes:

- `TEMPERATURE_PIN`: Pin analógico utilizado para leer la temperatura.
- `RS_PIN`, `EN_PIN`, `D4_PIN`, `D5_PIN`, `D6_PIN`, `D7_PIN`: Pines utilizados para controlar la pantalla LCD.
- `SERVO_PIN`: Pin utilizado para controlar el servo.
- `LED_PIN1`, `LED_PIN2`: Pines utilizados para controlar los LEDs.
- `POWER_BUTTON_PIN`: Pin utilizado para detectar el botón de encendido/apagado.
- `IR_PIN`: Pin utilizado para recibir las señales infrarrojas.

## Constantes

Se definen las siguientes constantes:

- `TEMPERATURA_LIMIE`: Límite de temperatura para detectar un posible incendio.
- `VERANO_TEMP_LIMITE`: Límite de temperatura para la temporada de verano.
- `INVIERNO_TEMP_LIMITE`: Límite de temperatura para la temporada de invierno.
- `OTONO_TEMP_LIMITE`: Límite de temperatura para la temporada de otoño.
- `PRIMAVERA_TEMP_LIMITE`: Límite de temperatura para la temporada de primavera.

## Variables globales

Se declaran las siguientes variables globales:

- `temperatura`: Almacena el valor de la temperatura actual.
- `estacion`: Almacena el valor de la estación actual.
- `systemActive`: Indica si el sistema está activo o no.
- `deteccion_fuego`: Indica si se ha detectado un posible incendio.
- `lcdActive`: Indica si la pantalla LCD está activa o no.
- `servo`: Objeto para controlar el servo.
- `lcd`: Objeto para controlar la pantalla LCD.
- `estado_led1`, `estado_led2`: Indican el estado de los LEDs.
- `power_button_presionado`: Indica si el botón de encendido/apagado ha sido presionado.
- `irReceiver`: Objeto para recibir señales infrarrojas.
- `irResults`: Almacena los resultados de las señales infrarrojas recibidas.
- `temperaturaAnterior`: Almacena el valor anterior de la temperatura.

## Función setup()

La función `setup()` se ejecuta una vez al inicio. Realiza las siguientes acciones:

- Inicializa la pantalla LCD.
- Configura los pines de los LEDs como salidas.
- Habilita la recepción de señales infrarrojas.
- Imprime las etiquetas de temperatura y estación en la pantalla LCD.
- Inicia la comunicación serial.
- Adjunta el servo al pin correspondiente.

## Función loop()

La función `loop()` se ejecuta continuamente en un ciclo. Realiza las siguientes acciones:

- Lee el valor del sensor de temperatura y lo convierte a grados Celsius.
- Si la temperatura actual es diferente a la anterior, actualiza la pantalla LCD con la nueva temperatura y estación según los límites establecidos.
- Controla los LEDs según la temperatura actual.
- Imprime la temperatura actual por el puerto serial.
- Si se recibe una señal infrarroja, realiza acciones según el código de la señal.

