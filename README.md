**En esta práctica ocuparemos un sensor (DTH 22) para obtener la humedad y temperatura a nuestro alrededor y utilizaremos la Esp32 para adquirir los datos y utilizaremos WOKWI para la simulación**

**informacion general del sesor DTH22**
El DHT22 es un sensor de temperatura y humedad con unas prestaciones que lo acercan mucho a los de alta precisión. Lo puedes encontrar fácilmente en tiendas especializadas o grandes superficies, donde No products found.. Eso te permite no tener que depender de un sensor de temperatura y otro de humedad por separado, sino tenerlo todo integrado en un mismo dispositivo.
Lo puedes encontrar suelto o en módulos especialmente diseñados para Arduino, es decir, el DHT22 montado sobre una placa PCB ya lista para usar, sin tener que agregar resistencias pull-up, etc. Hasta aquí todo se parece bastante el DHT11. Y también tendrás una alta fiabilidad y estabilidad en las mediciones debido a la señal digital calibrada que usa.

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



## REFERENCIAS
https://www.hwlibre.com/dht22/




**desarrollado por**


ALBERTO FANDIÑO 
https://github.com



