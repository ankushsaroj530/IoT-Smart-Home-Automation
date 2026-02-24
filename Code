
#define BLYNK_TEMPLATE_ID "YourTemplateID"
#define BLYNK_TEMPLATE_NAME "SmartHome"
#define BLYNK_AUTH_TOKEN "YourAuthToken"

#include <WiFi.h>
#include <BlynkSimpleEsp32.h>

char ssid[] = "YourWiFiName";
char pass[] = "YourWiFiPassword";

#define RELAY_PIN 23

BLYNK_WRITE(V0) {
  int relayState = param.asInt();
  digitalWrite(RELAY_PIN, relayState);
}

void setup() {
  Serial.begin(115200);
  pinMode(RELAY_PIN, OUTPUT);
  digitalWrite(RELAY_PIN, LOW);
  Blynk.begin(BLYNK_AUTH_TOKEN, ssid, pass);
}

void loop() {
  Blynk.run();
}
