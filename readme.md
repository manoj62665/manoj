it works basicaly on gas sensor 
it senses the gases by diffusion rate in room 
the mechanisim it is mainly works on the electrochemical cel

const int analogInPin=A0;
const int ledPin=13;
const int buzzerpin=13;
int sensorValue=0;
void setup()
  {
    
    Serial.begin(9600);
    pinMode(ledPin,OUTPUT);
    pinMode(buzzerpin,OUTPUT);
}
void loop()
{
  sensorValue=analogRead(analogInPin);
  if(sensorValue>=250)
  {
    digitalWrite(ledPin,HIGH);
    digitalWrite(buzzerpin,HIGH);
  }
  else
  {
    digitalWrite(ledPin,LOW);
    digitalWrite(buzzerpin,LOW);
   
  }
Serial.print("sensor=");
Serial.println(sensorValue);
delay(1000);
}
