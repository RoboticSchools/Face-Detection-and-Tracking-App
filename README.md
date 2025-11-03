### Microbit Code to Receive the Data from Face Detection and Tracking App

[Open in MakeCode Editor](https://makecode.microbit.org/_TYEayHArWU2o)

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/baebb085-ff00-4a14-9508-a98efe41bee0" />

---

### Arduino Code to Receive the Data from Face Detection and Tracking App

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
