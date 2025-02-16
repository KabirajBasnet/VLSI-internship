# Introdcution
Vsd squadron mini provided me with an opportunity to learn and gain experience in building programs,circuits and chip designs.
Using, this opportunity I build an auotmatic L.P.G gas detector using vsd-squadron and  minimal components for cheap and reliable usasge in every home.
***
![Screenshot 2025-02-16 110658](https://github.com/user-attachments/assets/1cd01742-b3ea-4c8a-a0c7-7d5026c6c6c9)
***
# Circuit diagram:
![Screenshot 2025-02-16 112819](https://github.com/user-attachments/assets/85141fab-7af2-468b-83c7-f668f36ddbbe)
***
# Code used:
~~~
bool GAS_VAL = LOW;
#define BUZZER_PIN1 PD3  
#define BUZZER_PIN2 PD4 
#define LED_PIN PD6
#define gassensor PC4      

void setup() {     
  pinMode(BUZZER_PIN1, OUTPUT); 
  pinMode(BUZZER_PIN2, OUTPUT); 
  pinMode(LED_PIN, OUTPUT);   
  pinMode(gassensor, INPUT);       
}
void loop() {  
  GAS_VAL = digitalRead(gassensor); 
  if (GAS_VAL == LOW) { 
  
    digitalWrite(BUZZER_PIN1, HIGH);  
    digitalWrite(LED_PIN, HIGH);        
  } 
  else if (GAS_VAL == HIGH){
    digitalWrite(BUZZER_PIN1, LOW);  
    digitalWrite(LED_PIN, LOW);        
  }
  delay(10); 
}
~~~
***
# Pins used:
1) Taking 5 V pin as common vcc.
2) Then taking ground pin(gnd) as common ground.
3) Give the MQ-6 sensor vcc and gnd, from common source ,then connect PC4 pin to the digital (d/o) output of the MQ-6 sensor.
4) Using the PD6 pin , we connect it to the L.E.D for turning it on/off.
5) We connect the resistor(220 ohms) acrros the led and the ground.
6) Using the PD3 pin , we connect it to the buzzer for turning it on/off.
***
# Working of the circuit:
   When, a gas like L.P.G,propane(i.e flammable gases) comes in contact with the MQ-6 sensor the sensor detects it and sends a output signal to pin PC4.Then, the vsd squadron mini takes the input and then sends  output via the two pins PD3 and PD6, which turns on/off the led and the buzzer.
*** 
# Conclusion:
   I would like to thank Kunal sir and the whole VSLI and SAMSUNG team for giving me this opportunity to build this wondurl circuit using VSD-sqaudron mini.
***
# Thankyou for viewing 😊.
