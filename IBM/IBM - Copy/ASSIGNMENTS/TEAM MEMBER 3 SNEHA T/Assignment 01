void setup()
{
  Serial.begin(9600);
  pinMode(13,OUTPUT);
  pinMode(4,INPUT);
  pinMode(12,OUTPUT);
}
void loop()
{
  int p=digitalRead(4);
  double a=analogRead(A0);
  double c=(((a/1024)*5)-0.5)*100;
  Serial.println(c);
    Serial.println(p);

  if(c>=36.7 && p==1)
  {
    tone(12,c);
    delay(1000);
    Serial.println("AS YOUR TEMPERATURE IS VERY HIGH,YOU ARE NOT ALLOWED");
    digitalWrite(13,LOW); 
  }
  else if(c<=36.7 && p==1)
  {
    noTone(12);
    delay(1000);
    Serial.println("YOU CAN NOW VISIT OUR PLACE");
    digitalWrite(13,HIGH); 
  }
  else
    noTone(12);
    digitalWrite(13,LOW);
}
    
  
  
  
  