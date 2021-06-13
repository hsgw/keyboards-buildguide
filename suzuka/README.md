Suzuka ビルドガイド
=======================

お買い上げありがとうございます。      
組立前に必ずこちらのビルドガイドを確認して下さい。   
部品の不足やご質問などがありましたら、urkwtky@gmail.com、または[Twitter(@hsgw)](https://twitter.com/hsgw)までご連絡下さい。

## キーレイアウト
![layout](imgs/suzuka_keymap.png)

## キットに含まれるもの

| 種類               | 値            | 個数 |
|--------------------|---------------|------|
| 抵抗               | 10k           | 5    |
| ダイオード         |               | 92   |
| LED                | 3mm 青        | 3    |
| TRRSコネクタ       |               | 2    |
| MX用ソケット       |               | 92   |
| タクタイルスイッチ |               | 2    |
| ゴム足             |              | 8    |
| M2 10mm スペーサ   |               | 19   |
| M2 5mmネジ         |               | 38   |

## その他に必要なもの

| 種類               | 値           | 個数 |
|--------------------|--------------|------|
| スイッチ           |  CherryMX互換 | 92   |
| 2Uスタビライザー   |              | 4    |
| Pro micro          | コンスルー付 | 2    |
| キーキャップセット | ※注意参照   |      |

## 必要なキーキャップについて
一般的な日本語配列用キーキャップに加えて、2.25Uキーキャップが2個必要です
2.25Uキーキャップ例
https://talpkeyboard.stores.jp/items/5e2d1d65cf327f287ef2d785

## 組み立て
### 抵抗のはんだづけ
10kΩ抵抗をはんだづけします   
裏側から差し込んで表面(スイッチ側)ではんだづけします

***左側基板のR4は実装済みです***   
左側はLED付近に3つ、右側はPro Micro付近に1つあります

(左側)

![r1](imgs/r1.jpg)

(右側)

![r2](imgs/r2.jpg)

### ダイオードのはんだづけ
ダイオードをはんだづけします   
抵抗と同じく裏側から差し込んで表面(スイッチ側)ではんだづけします

***ダイオードには極性(向き)があります***   
基板上にマーキングがある方向とダイオードの帯を揃えてはんだづけして下さい

### スイッチソケットのはんだづけ
スイッチソケットをはんだづけします   
パッドとソケットのどちらもしっかり温めてはんだが流れていることを確認しながら実装して下さい

### LEDのはんだづけ
LEDをはんだづけします

***LEDはスイッチ側から差し込んで実装します！！！***   
片方の足だけをはんだづけして、真っ直ぐかつ奥までしっかり差し込めているか確認してからもう片方をはんだ付けして下さい。

![led](imgs/led.jpg)

***LEDには極性があります！！！！！***     
LEDの足の長い方(アノード)が基板の丸いパッド側に実装します。

### リセットスイッチとTRRSコネクタのはんだづけ
リセットスイッチとTRRSコネクタをはんだづけします   
裏面から差し込んで表面ではんだづけします

### Pro Micro
Pro Microは部品のない面が外側になるようにコンスルーをはんだづけしたあとキーボード基板の裏面から差し込みます

![promicro](imgs/promicro1.jpg)
![promicro](imgs/promicro2.jpg)

### 動作確認
Pro Microを差し込んだら、ファームウェアを書き込んで動作確認をします   
ファームウェアはこちらのリポジトリに入っています

https://github.com/hsgw/qmk_firmware/tree/dm9_split/
https://github.com/hsgw/qmk_firmware/tree/dm9_split/keyboards/dm9records/suzuka

ビルドコマンドは
```
make dm9records/suzuka:default
(同時に書き込むなら)
make dm9records/suzuka:default:flash
```

ファームウェアが書き込めたら、キーボードとして認識されるかどうか、スイッチソケットの両端をピンセットなどでショートさせて正しく入力されるかを確認して下さい

### スイッチとスイッチプレートの取り付け
スイッチプレートにはめ込みながらメイン基板にスイッチを取り付けていきます   
スイッチの足が真っ直ぐでないとソケットに入らず曲がってしまうので取り付ける前に確認して真っ直ぐに整えながら差し込んで下さい

### 動作確認
スイッチを押して正しく動作するか確認します
入力されないキーがある場合はソケットが正しくはんだづけされているか、スイッチの足が曲がっていないか確認して下さい

### ボトムプレートの取り付け
ボトムプレートへスペーサをネジ止めします   
全てのスペーサがボトムプレートへ固定されたあとメイン基板+スイッチプレートを重ねて上からネジ止めします