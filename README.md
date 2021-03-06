Gluin Gateway App for Arduino
---------------

## 概要
GluinにArduinoをデバイスとして登録し、値の受け渡しを中継するFirefox OSアプリです。
Arduinoの任意のピンから入力した値をGluinへ送信したり、Gluinから受信した値をArduinoの任意のピンへ出力することができます。
アプリとArduinoはTCP Socketで通信を行っています。

## 手順
1. Arduinoには[CommandServer](https://github.com/dadaa/arduino.js/blob/master/core/sketch/CommandServer/CommandServer.ino)を書き込む。
2. FirefoxのWebIDEで、このアプリをシミュレータや端末にインストールする。
3. Xbee WiFiや[ArduinoProxy](https://github.com/Babibubebon/ArduinoProxy)などを用いて、ArduinoがSerial<=>TCP Socketで通信できるようにする。
4. このアプリを起動し、[Settings]タブでTCP Socket通信のIPアドレス・ポート番号を入力し、[Test & Set]ボタンで「OK」と表示されることを確認する。
5. [Devices]タブでArduinoにつなげるパーツを追加・設定する。
6. [Settings]タブでGluinの認証情報を入力し、Gluinに登録されることを確認する。
7. [Start]ボタンを押して、Gluinと値が同期されていれば成功。
