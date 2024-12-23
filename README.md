**En esta práctica ocuparemos un sensor (DTH 22) para obtener la humedad y temperatura a nuestro alrededor y utilizaremos la Esp32 para adquirir los datos y utilizaremos WOKWI para la simulación**

**CODIGO A UTILIZAR **
```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}
```



**SIMULACION EN WOKI**
!![](https://github.com/FANDINO7/PRACTICA-CON-SENSOR-DHT22-/blob/main/DH22%20SESOR%20DE%20TEMPERATURA%20.jpg?raw=true)

**Instrucciones de operación**
1Iniciar el Simulador 2.- Visualizar la obtención de los datos en el monitor serial 3.- Obtener la temperatura y la humedad dando click dos veces a nuestro sensor DHT22

**Resultados**
!![](https://github.com/FANDINO7/PRACTICA-CON-SENSOR-DHT22-/blob/main/resultados.jpg?raw=true)
