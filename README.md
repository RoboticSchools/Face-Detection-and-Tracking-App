```C++
int leftEye, rightEye, mouth, faceVisible, headHorizontal, headVertical;

void setup() {
  Serial.begin(115200);
}

void loop() {
  if (Serial.available()) {
    char data[50];
    Serial.readBytesUntil('\n', data, sizeof(data));
    sscanf(data, "L%d,R%d,M%d,F%d,H%d,V%d", 
           &leftEye, &rightEye, &mouth, &faceVisible, &headHorizontal, &headVertical);

    Serial.print("Left Eye = "); Serial.print(leftEye);
    Serial.print("  Right Eye = "); Serial.print(rightEye);
    Serial.print("  Mouth = "); Serial.print(mouth);
    Serial.print("  Face Visible = "); Serial.print(faceVisible);
    Serial.print("  Head H = "); Serial.print(headHorizontal);
    Serial.print("  Head V = "); Serial.println(headVertical);
  }
}

```
