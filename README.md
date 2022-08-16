# reading-analog-digital-input-value-
simulate analog &amp; digital input value circuits

-by using tinkercad website-	

FOR ANALOG INPUT VALUE CIRCUIT :

tools:
   ¬ Arduino Uno R3
   ¬ breadboard
   ¬ power supply
   ¬ potentiometer
   ¬ multimeter
   ¬ 8 wires
   
   
   
code: 

// the setup routine runs once when you press reset:
int AnalogSensorPin = A0;

void setup() {
  // initialize serial communication at 9600 bits per second:
  Serial.begin(9600);
  pinMode(AnalogSensorPin, INPUT);
}

// the loop routine runs over and over again forever:
void loop() {
  // read the input on analog pin 0:
  int integer_value = analogRead(AnalogSensorPin);
  float actual_voltage_value = (float)integer_value*(5.0/(1024-1));

  
  // print out the value you read:
  Serial.print(" Analog Integer Value = ");
  Serial.print(integer_value);
  Serial.print(",  Actual Voltage Value = ");
  Serial.print(actual_voltage_value);
  Serial.println();
  delay(1);        // delay in between reads for stability
}




Pic for circuit :
![analog input value circuit](https://user-images.githubusercontent.com/100563503/184835320-ac4f189f-6f08-4e98-8cf9-9cddd50cd655.png)


Run :


https://user-images.githubusercontent.com/100563503/184837032-fff853ad-2dd4-40c9-95fd-9aa4d2fd8ce0.mp4






FOR DIGITAL INPUT SIGNAL CIRCUIT:


tools:
- 
