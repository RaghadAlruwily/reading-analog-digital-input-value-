# reading-analog-digital-input-value-
simulate analog &amp; digital input value circuits

-by using tinkercad website-	

FOR ANALOG INPUT VALUE CIRCUIT :

tools:
-  Arduino Uno R3
-  breadboard
-  power supply
-  potentiometer
-  multimeter  
-  8 wires
   
   
   
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
- Arduino Uno R3
- breadboard
- LED
- Pushbutton
- Resistor X220
- Resistor X10
- 6 wires


code:
// C++ code
//
int buttonState = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
}

void loop()
{
  // read the state of the pushbutton
  buttonState = digitalRead(2);
  // check if pushbutton is pressed. if it is, the
  // button state is HIGH
  if (buttonState == HIGH) {
    digitalWrite(13, HIGH);
  } else {
    digitalWrite(13, LOW);
  }
  delay(10); // Delay a little bit to improve simulation performance
}




Pic for circuit :

![digital circuit](https://user-images.githubusercontent.com/100563503/185045897-85c3c85e-646b-49e6-bb66-f76ea35eabf0.png)



Run :



https://user-images.githubusercontent.com/100563503/185046018-13fa6f51-e1c0-46db-a3f4-85e39481aa4e.mp4

