# Ponderada IOT 2
Imagem do circuito RC feito no TinkerCad:

<img src="Exquisite Habbi (1).png" alt="I" style="width: 500px;">

Esse circuito mostra como um capacitor carrega e
descarrega ao longo do tempo, o Arduino está lendo
essa variação de tensão no capacitor (via uma
entrada analógica).

Codigo do circuito RC:

``` 
int pinoNoRC=0;
int valorLido = 0;
float tensaoCapacitor = 0, tensaoResistor;
unsigned long time;
void setup(){
Serial.begin(9600);
}
void loop() {
time=millis();
valorLido=analogRead(pinoNoRC);
tensaoResistor=(valorLido*5.0/1023); // 5.0V / 1023 degraus = 0.0048876
tensaoCapacitor = abs(5.0-tensaoResistor);
Serial.print(time); //imprime o conteúdo de time no MONITOR SERIAL
Serial.print(" ");
Serial.print(tensaoResistor);
Serial.print(" ");
Serial.println(tensaoCapacitor);
delay(400);
}
```
Aqui esta a imagem dos Graficos Gerados pelo gemini:

<img src="download.png" alt="I" style="width: 500px;">
<img src="download (1).png" alt="I" style="width: 500px;">


Tambem fiz a Montagem Fisica:
<img src="IMG_2264.jpg" alt="I" style="width: 500px;">

