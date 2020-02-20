# Github-new-project
Colour sensor- Minor Project

int ledG = 10;
int ledB = 11;
int ledR = 12;
float lRead = A0;
void setup()
{
pinMode(ledG,OUTPUT);
pinMode(ledB,OUTPUT);
pinMode(ledR,OUTPUT);
pinMode(lRead,INPUT);
Serial.begin(115200);
}

void loop()
{
/*Green Code*/
digitalWrite(legG,HIGH);
delay(3000);
lRead = analogRead(lRead);
resist = (lRead*5000)/(lRead+5000);
if(resist>=85 && resist<=510)
{
Serial.println("GREEN");
Serial.println();
}
digitalWrite(legG,LOW);    

/*Blue Code*/
digitalWrite(legB,HIGH);
delay(3000);
lRead = analogRead(lRead);
resist = (lRead*5000)/(lRead+5000);
if(resist>=155 && resist<=710)
{
Serial.println("BLUE");
Serial.println();
}
digitalWrite(legB,LOW);    

/*Red Code*/
digitalWrite(legR,HIGH);
delay(3000);
lRead = analogRead(lRead);
resist = (lRead*5000)/(lRead+5000);
if(resist>=95 && resist<=585)
{
Serial.println("RED");
Serial.println();
}
digitalWrite(legR,LOW);    
}
