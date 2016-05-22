//blinkRiffleMod, Arduino sketch by pdhixenbaugh

int led = 9;
// Judging by other riffle sketches, the blinking LED is number 9


// the setup routine runs once when you press reset:
void setup() {                
  // this runs once when you start the program. Initialize stuff.
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT);     
}

void loop() {
  //This is where you put the main stuff of your project 
  //The goal of this is to verify that you can send sketches by
  //causing your light to blink at a different rate.
  //If it succeeds, the light will blink twice quickly, then pause
  digitalWrite(led,HIGH);
  delay(250);
  digitalWrite(led,LOW);
  delay(250);
  digitalWrite(led,HIGH);
  delay(250);
  digitalWrite(led,LOW);
  delay(1250);  
}
