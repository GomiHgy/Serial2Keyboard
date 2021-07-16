# Serial2Keyboard
SeeeduinoXIAOがRXピンで受信したシリアルデータをキーコードに変換するファームウェアです。

![image](https://user-images.githubusercontent.com/10735253/125961548-8bf36823-7349-4b75-b991-5255efe64b0b.png)

## 通信仕様

- ボーレート:115200bps
- データ:8bit
- パリティ:なし
- ストップビット:1bit
- フロー制御:なし

## micro:bitでの利用例

micro:bitを使った場合の利用例です。

### micro:bitのシリアルを使った場合の例(カスタムブロック付)

![image](https://user-images.githubusercontent.com/10735253/125963230-cb67446a-7194-41f0-aa4e-43ac34def109.png)

micro:bit(TX)->[ASCII(Custom)]->(RX)SeeeduinoXIAO(USB)->[KeyCode]

https://github.com/GomiHgy/serial2keyboard-microbit-serial

### micro:bitの無線を使った場合の例(カスタムブロック付)

![image](https://user-images.githubusercontent.com/10735253/125963372-2694f15d-fd18-44ea-8b40-a41e4ba98205.png)

micro:bit送信機->[radio]->micro:bit受信機(TX)->[ASCII(Custom)]->(RX)SeeeduinoXIAO(USB)->[KeyCode]

送信機 : https://github.com/GomiHgy/serial2keyboard-microbit-transmitter

受信機 : https://github.com/GomiHgy/serial2keyboard-microbit-receiver

## 使用ライブラリ

[Arduino HID Project](https://github.com/NicoHood/HID)
