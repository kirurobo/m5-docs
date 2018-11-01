# M5Stick

## 概要

<mark>**M5Stick**</mark>は1.3インチのOLEDスクリーン(64x128)、LED、ボタン、ブザー、IR送信機と80mAhの電池を内蔵した開発用ボードです。小型なのでウェアラブルデバイスとして使用したり、壁などに固定して利用することが可能です。

M5Stickは２種類のモデルがあります。通常版とMPU9250版です。MPU9250版には９軸のIMUが搭載され、さらに`WATCH BELT`、`WALL`、`BRICK`が付属します。

## 特徴

- サポートプログラミング
  - Arduino
  - UIFlow (Blockly / MicroPython)
- ウェアラブル
- MEMS IMU(MPU9250版のみ)

## スペック

|項目|詳細|
|:---|:---|
|Core|M5Stick|
|カラー|白 (通常版) / 灰 (MPU9250版)|

## ピンマップ

|項目|PIN|
|:---|:---|
|LED|GPIO19|
|ボタン|GPIO25|
|ブザー|GPIO26|
|IR|GPIO17|
|SCL|GPIO13|
|SDA|GPIO25|

**MPU9250版**

|項目|PIN|
|:---|:---|
|SCL|GPIO21|
|SDA|GPIO22|

## パッケージ内容

### 通常版・MPU9250版共通

- 1x M5Stick 内蔵 80mAh バッテリー
- 1x USB Type-C ケーブル

### MPU9250版のみ

- 付属品
  - `WATCH BELT`
  - `WALL`
  - `BRICK`

## ドキュメント

- **サンプルコード**
  - [Arduino](https://github.com/m5stack/M5Stack/tree/master/examples/Stick/FactoryTest)

- **データシート**
  - [ESP32](https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_cn.pdf)
  - [MPU9250](https://www.invensense.com/wp-content/uploads/2015/02/PS-MPU-9250A-01-v1.1.pdf)

- **クイックスタート　(Arduino)**
  - 近日公開...

<figure>
    <img src="assets/img/product_pics/core/minicore/m5stick/m5stick_01.jpg" height="300" width="300">
</figure>

<figure>
    <img src="assets/img/product_pics/core/minicore/m5stick/m5stick_02.jpg" height="300" width="300">
</figure>

<figure>
    <img src="assets/img/product_pics/core/minicore/m5stick/m5stick_03.jpg" height="300" width="300">
</figure>

## 関連情報

- [M5Stick 購入](https://www.aliexpress.com/store/product/M5Stack-Official-New-M5Stick-Mini-Development-Kit-ESP32-1-3-OLED-80mAh-Battery-Inside-Buzzer-IR/3226069_32947692973.html)