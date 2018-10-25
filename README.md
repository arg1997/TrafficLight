# TrafficLight

const int buttonPin = 1;
const int RED =  A5;
const int ORANGE = A4;
const int GREEN = A3;

int led1 = 4;
int led2 = 5;
int led3 = 6;
int led4 = 7;
int led5 = 8;
int led6 = 9;
int led7 = 10;
int led8 = 11;
int led9 = 12;
int led10 = 13;


int buttonState = 0;
int state = 0;


void setup() {

  pinMode(RED, OUTPUT);
  pinMode(ORANGE, OUTPUT);
  pinMode(GREEN, OUTPUT);

  pinMode(buttonPin, INPUT);

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(led5, OUTPUT);
  pinMode(led6, OUTPUT);
  pinMode(led7, OUTPUT);
  pinMode(led8, OUTPUT);
  pinMode(led9, OUTPUT);
  pinMode(led10, OUTPUT);
}

void loop() {

  digitalWrite(GREEN, HIGH);

  buttonState = digitalRead(buttonPin);



  if (buttonState == LOW) {

    digitalWrite(GREEN, LOW);

    for (int i = 4; i < 14; i++) {
      digitalWrite(GREEN, HIGH);
      digitalWrite(i, LOW);
      delay(500);
      digitalWrite(i, HIGH);

    }
    digitalWrite(GREEN, LOW);
    digitalWrite(ORANGE, HIGH);
    delay(1000);
    digitalWrite(ORANGE, LOW);

    digitalWrite(RED, HIGH);

    for (int i = 4; i < 14; i++) {
      
      digitalWrite(i, HIGH);
      delay(500);
      digitalWrite(i, LOW);
    }
     
      digitalWrite(RED, LOW);

    }
  
  }

