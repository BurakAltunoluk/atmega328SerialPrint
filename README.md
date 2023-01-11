# atmega328SerialPrint


```C++

char val;
int ledPin = 13;

void setup() {

 pinMode(ledPin,OUTPUT); 
 Serial.begin(9600);
 
}

void loop() {

if (Serial.available()) {
 val = Serial.read();
 
 if (val == '1') {

   digitalWrite(13,HIGH);
  
 } else if (val == '2') {

    digitalWrite(13,LOW);
    
    }
  }
}
