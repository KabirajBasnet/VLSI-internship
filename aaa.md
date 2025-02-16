# Video

https://github.com/user-attachments/assets/45781803-2735-4791-baa9-396f1416cff0

***
#### CODE USED:
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
# Thankyou for viewing 😊.




