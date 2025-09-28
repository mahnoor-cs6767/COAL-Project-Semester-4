extern "C" {
  void adc_init();
  uint16_t adc_read();
}

const int ledPin = 13;
const int threshold = 400;

void setup() {
  Serial.begin(9600);
  adc_init();
  pinMode(ledPin, OUTPUT);
}

void loop() {
  uint16_t sensorValue = adc_read();

  if (sensorValue < threshold) {
    digitalWrite(ledPin, HIGH);
    Serial.println("Dark detected");
  } else {
    digitalWrite(ledPin, LOW);
    Serial.println("Light detected");
  }
  delay(500);
}