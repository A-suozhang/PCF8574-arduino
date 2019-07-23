# PCF8574-arduino-esp32
* The Wrapper For IIC Drived IO Extension PCF8574

## Tips
* My .ino file include The PCF8574 from "src/PCF5874.h", If You can put them in the same folder, just include"PCF8574.h" 
  * (My Arduino couldn't recognize It When I did So)
* Implemented A Few Methods Arduino like
  * PCF8574.digitalRead(int i)    -  Get The i-th PIN is HIGH/LOW
  * PCF8574.digitalWrite(int i, HIGH/LOW) - Set ...
  * PCF8574.WriteByte()
  * PCF8574.ReadByte()
  * PCFF8574.get_temp_data()
* The ADDR For instance PCF8574 is 0x00 & 0x01
  * which means That The A0 A1 A2 being 000 & 100 (The addr fed in should be in 0~7)
* The ADDR in Wire.beginTransmission & Wire.requestFrom() is 0x20 & 0x21
  * Which Is The HIGH 7 BIT Of The addr-reg(REFER TO DATASHEET) - (This Is Set By Arduino Wrapper Of IIC!)
  
