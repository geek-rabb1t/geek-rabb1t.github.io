---
layout: post
title:  "Futabaビルドガイド"
date:   2025-2-1 00:00:01 +0000
categories: 
  - build_guide
tags:
  - Futaba
  - Build Guide
banner: "/assets/images/futaba_build_guide/DSCF3446.jpg"
image: "/assets/images/futaba_build_guide/DSCF3446.jpg"
permalink: /futaba/build_guide
---

## 準備

組み立て前に同梱物や追加で必要な部品、必要な工具を確認してください。


### 内容物の確認

全ての写真はクリックして拡大可能できます。

| 分類     | 部品                                       | 同梱数 | 写真                                                                       |
| -------- | ------------------------------------------ | -----: | -------------------------------------------------------------------------- |
| ケース   | トップケース                               |      1 | <img src="/assets/images/futaba_build_guide/DSCF3283.jpg" width="100px">   |
| ^^       | ボトムケース                               |      1 | <img src="/assets/images/futaba_build_guide/DSCF3285.jpg" width="100px">   |
| フォーム | トップフォーム (右・中・左)                |      1 | <img src="/assets/images/futaba_build_guide/DSCF3290.jpg" width="100px">   |
| ^^       | ボトムフォーム (右・中・左)                |      1 | <img src="/assets/images/futaba_build_guide/DSCF3292.jpg" width="100px">   |
| PCB      | メインPCB                                  |      1 | <img src="/assets/images/futaba_build_guide/DSCF3281.jpg" width="100px">   |
| 電子部品 | トラックパッドモジュール                   |      1 | <img src="/assets/images/futaba_build_guide/DSCF3294_1.jpg" width="100px"> |
| ^^       | chocソケット                               |     49 | <img src="/assets/images/futaba_build_guide/DSCF3313_1.jpg" width="100px"> |
| ^^       | ロータリーエンコーダー(型番: EC12E2420301) |      1 | <img src="/assets/images/futaba_build_guide/DSCF3307_1.jpg" width="100px"> |
| ^^       | マイコンボード (型番: RP2040-Zero)         |      1 | <img src="/assets/images/futaba_build_guide/DSCF3295_1.jpg" width="100px"> |
| ^^       | マイクロスイッチ                           |      1 | <img src="/assets/images/futaba_build_guide/DSCF3318_1.jpg" width="100px"> |
| ^^       | フラットケーブル (0.5mmピッチ6ピン  )      |      1 | <img src="/assets/images/futaba_build_guide/DSCF3330.jpg" width="100px">   |
| ^^       | ピンヘッダ (2.54mmピッチ40ピン  )          |      1 | <img src="/assets/images/futaba_build_guide/DSCF3346.jpg" width="100px">   |
| 部品     | クリッカー                                 |      1 | <img src="/assets/images/futaba_build_guide/DSCF3305_1.jpg" width="100px"> |
| ^^       | ホイール                                   |      1 | <img src="/assets/images/futaba_build_guide/DSCF3296_1.jpg" width="100px"> |
| ^^       | トラックパッドカバー (マット黒アクリル)    |      1 | <img src="/assets/images/futaba_build_guide/DSCF3320_1.jpg" width="100px"> |
| ^^       | タッピングビス(短)  - M3 長さ6mm           |      2 | <img src="/assets/images/futaba_build_guide/DSCF3321_2.jpg" width="100px"> |
| ^^       | タッピングビス(長)  - M3 長さ8mm           |      6 | <img src="/assets/images/futaba_build_guide/DSCF3321_3.jpg" width="100px"> |
| ^^       | ゴム足                                     |     10 | <img src="/assets/images/futaba_build_guide/DSCFXXX.jpg" width="100px">    |



### 自分で用意するもの

| 部品                                       | 必要数 | 補足                                                                  |
| ------------------------------------------ | ------ | --------------------------------------------------------------------- |
| Kailh ChocV1もしくは、Kailh ChocV2スイッチ | 49     | ChocV2互換のLofree Ghost等、 Kailh x Lofree Low-profileスイッチも対応 |
| Low Profile対応1Uサイズキーキャップ        | 49     | ChocV1とChocV2で軸の形が違うので間違えて買わないよう注意              |


ぎーくらびっとのおススメスイッチ
- [Kailh Deep Sea Silent MINI ロープロファイルスイッチ Islet](https://talpkeyboard.net/items/66a056514c088e035d0344b3)
- [Kailh Deep Sea Silent MINI ロープロファイルスイッチ Whale](https://talpkeyboard.net/items/66a0596a545dc7002b5dea18)
- [Kailh x Lofree Ghost](https://lofree.co.jp/products/ghost-low-profile-pom-switches?variant=50487412556007)

確認済みキーキャップ
- [Tai-Hao Thins](https://talpkeyboard.net/?category_id=66e79046a6782d33e6380dab)
- [XVXロープロファイルキーキャップ](https://amzn.asia/d/cjRH1xz)



## 組み立てに必要な工具や道具


| 道具                              | 用途                                   |
| --------------------------------- | -------------------------------------- |
| はんだごて                        | 部品のはんだ付けに使用                 |
| はんだ                            | 部品のはんだ付けに使用                 |
| ニッパー                          | はみ出したピンヘッダの切り落としに使用 |
| No.1(PH1)サイズのプラスドライバー | ケースのねじ止めに使用                 |
| 逆作用ピンセット                  | はんだ付け中の部品を固定するのに使用   |
| 両面テープ                        | トラックパッドの固定に使用             |

## 組み立て手順

まず、PCBの表裏について説明します。

| 面  | 実装前                                                                   | 実装後                                                                   | 説明                                                   |
| --- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------ |
| 表  | <img src="/assets/images/futaba_build_guide/DSCF3282.jpg" width="200px"> | <img src="/assets/images/futaba_build_guide/DSCF3382.jpg" width="200px"> | 表面はキースイッチをはめる面です。\                    |
| \|  | \|                                                                       | \|                                                                       | マイクロスイッチとロータリーエンコーダーを実装します。 |
| 裏  | <img src="/assets/images/futaba_build_guide/DSCF3281.jpg" width="200px"> | <img src="/assets/images/futaba_build_guide/DSCF3385.jpg" width="200px"> | Futabaと印刷されています。\                            |
| \|  | \|                                                                       | \|                                                                       | 一部の部品は実装済みです。                             |



### 電子部品のはんだ付け

#### chocソケットの取り付け

PCBの裏面で作業します。

chocソケットには向きがあります。向きを間違えるとスイッチが外れやすくなったり、キー入力できない場合があります。ソケットの向きを間違えないように注意してください。

![ソケットの向き](/assets/images/futaba_build_guide/DSCF3334.jpg)

また、PCBが薄いためchocソケットがPCBからはみ出します。そのため、一つ一つ、逆作用ピンセットで抑えながらはんだ付けしてください。

![逆作用ピンセットで抑える](/assets/images/futaba_build_guide/DSCF3342.jpg)

ピンセットで固定するため以下の順番に作業してください。

![はんだ付け順](/assets/images/futaba_build_guide/DSCF3385_1.jpg)

#### マイコンボード(RP2040-Zero)の取り付け


#### あらかじめ、マイコンにファームウェアを書き込みます。

マイコンにUSBケーブルを接続し、PCと接続します。  
ストレージデバイスとして認識するので、エクスプローラーで開き、以下のリンク先のファイルをコピーします。  
ストレージとして認識しない場合、RESETとBOOTボタンを同時に押してください。

<font color=red>ファームウェア公開後、ここにリンクを貼る</font>

![ファームウェアの書き込み](/assets/images/futaba_build_guide/screenshot_1.png)

キット付属のピンヘッダをニッパーで切り分けます。
切り分けた後のピンヘッダ

- 9本足： 2個
- 5本足： 1個

![切り取り後のピンヘッダ](/assets/images/futaba_build_guide/DSCF3347.jpg)

PCBの裏面にRP2040-Zeroに切り分けたピンヘッダーを差し込み、その上にRP2040-Zeroを載せます。  
写真のように、USBコネクタの実装面が見えるように差し込みます。

![マイコンの固定](/assets/images/futaba_build_guide/DSCF3348.jpg)

逆作用ピンセットでにRP2040-Zeroを抑えながら、PCBからはみ出た四隅のピンをニッパーで切ります。
ニッパーで切り落としたら、四隅だけはんだ付けします。

![はみ出しを切り落とす](/assets/images/futaba_build_guide/DSCF3360.jpg)

RP2040-Zero からはみ出たピンも同じようにニッパーで切り落としはんだ付けします。

![四隅のはんだ付け後](/assets/images/futaba_build_guide/DSCF3365.jpg)

これでPCBとRP2040-Zeroが固定されるので、逆作用ピンセットは外してかまいません。  
PCB側の残りのピンを全て切り取り、はんだ付けします。

![PCB側のマイコンはんだ付け後](/assets/images/futaba_build_guide/DSCF3367.jpg)

RP2040-Zeroも同様にはみ出たピンを全て切り取り、はんだ付けします。

![マイコンはんだ付け後](/assets/images/futaba_build_guide/DSCF3370.jpg)

#### マイクロスイッチの取り付け

**ここから部品を配置する面が変わります。**  
**間違えないよう注意してください。**

PCBの表面にマイクロスイッチを差し込みます。
マイクロスイッチを逆作用ピンセットで抑えた状態ではみ出た足をニッパーで切り取ります。

![マイクロスイッチの固定](/assets/images/futaba_build_guide/DSCF3371.jpg)

ピンセットで固定したままはんだ付けします。

![マイクロスイッチのはんだ付け](/assets/images/futaba_build_guide/DSCF3374.jpg)

#### ロータリーエンコーダーの取り付け

PCBの表側からロータリーエンコーダーを差し込みます。
PCBからはみ出した細い3本の足をニッパーで切り取ります。

![ロータリーエンコーダの固定](/assets/images/futaba_build_guide/DSCF3377.jpg)

ニッパーで切り取った足をはんだ付けします。

![ロータリーエンコーダのはんだ付け](/assets/images/futaba_build_guide/DSCF3378.jpg)

2本の太い足を切り取り、はんだ付けします。

![ロータリーエンコーダの足のはんだ付け](/assets/images/futaba_build_guide/DSCF3393.jpg)

はんだ付けは以上となります。

### 各種部品の取り付け

#### スイッチの取り付け

PCBの表面の上にトップフォームを重ねます。

![フォームを重ねる](/assets/images/futaba_build_guide/DSCF3387.jpg)

上からスイッチをはめ込みます。

![ロータリーエンコーダのはんだ付け](/assets/images/futaba_build_guide/DSCF3389.jpg)

#### クリッカーの取り付け

PCBの表面のからクリッカーをはめます。
写真の赤枠部分をつぶすようにつまみながら、下に押し込みます。

![クリッカーの取り付け](/assets/images/futaba_build_guide/DSCF3392.jpg)

取り外すときは、同じようにつまみながら引き抜きます。

#### ホイールの取り付け

クリッカーが取り付け済みであることを確認してから、エンコーダーにホイールを取り付けます。

![ホイールの取り付け](/assets/images/futaba_build_guide/DSCF3397.jpg)


この時点ではまだトラックパッドは取り付けません。  

### Vial の起動

Chrome等WebHIDに対応したブラウザの場合、 以下のURLにアクセスして ブラウザ版のアプリを起動します。

https://vial.rocks/

`Start Vial` ボタンが表示される場合、そのままボタンを押して、 Vialを開始します。

![Start Vial](/assets/images/futaba_build_guide/screenshot_2.png)

このようなダイアログが表示されたら、`Futaba` を選択します。

![ペアリング](/assets/images/futaba_build_guide/screenshot_3.png)


ボタンが表示されない場合はWebHID非対応ブラウザなので、デスクトップアプリを使用してください。  
非対応ブラウザの場合は以下のURLから `Download Vial` を選んで、デスクトップアプリをインストールできます。

https://get.vial.today/

ここでは利用者の多そうなブラウザ版で説明します。
デスクトップ版も同じ操作です。

### キー入力とホイールの動作確認

まず、マイコンにUSBケーブルを刺し、PCに接続します。

![ロック解除](/assets/images/futaba_build_guide/DSCF3398.jpg)

Vialを起動します。

Matrix testerタブを選択し、右下のunlockボタンを押します。  
以下のダイアログが表示されたら左上と右上のキーを押しながらロックを解除します。

![ロック解除画面](/assets/images/futaba_build_guide/screenshot_5.png)


Vialのロック解除は赤枠の2キーを長押しします。

![ロック解除で押すキー](/assets/images/futaba_build_guide/DSCF3389_1.jpg)

#### 各キーの動作確認

全部のキーを入力し、正しく入力できるか確認してください。
ロータリーエンコーダーの回転とトラックパッドの入力はテストできないので、下のスクリーンショットの状態になったらOKです。

![キー入力確認](/assets/images/futaba_build_guide/screenshot_7.png)

上手く動かない場合、ページ下部の[トラブルシューティング](#トラブルシューティング) を参考に対応してください。

#### ホイールの動作確認

ホイールの回転とホイールクリックで入力が発生するか確認してください。

ホイールクリックは、通常のキー入力と同じように Matrix testerで確認できます。

ホイールの回転には、カーソルの上キーと下キーが割り当てられています。  
テキストエディタなどでカーソルが上下に移動するか確認してください。

上手く動かない場合、ページ下部の[トラブルシューティング](#トラブルシューティング) を参考に対応してください。

#### トラックパッドの取り付けと動作確認

**始めに、マイコンからUSBケーブルを抜きます。**  
トラックパッド裏面（部品が実装済みの面）のFFCコネクタの黒い部分をトラックパッドと平行に引っ張り、ロックを解除します。

![FFCコネクタのロック解除](/assets/images/futaba_build_guide/DSCF3403.jpg)

フラットケーブルの青い面を上にして、フラットケーブルをまっすぐ差し込みます。

![フラットケーブルを差し込む](/assets/images/futaba_build_guide/DSCF3406.jpg)

FFCコネクタの黒い部分を押し込み、ロックします。

![コネクタのロック](/assets/images/futaba_build_guide/DSCF3409.jpg)


トラックパッドをトップケースの上に載せます。
この時点では固定しません。

![ケースに置く](/assets/images/futaba_build_guide/DSCF3410.jpg)

トラックパッドと同様の手順でフラットケーブルをPCBに接続します。

![PCB側のフラットケーブル接続](/assets/images/futaba_build_guide/DSCF3482.jpg)

トラックパッドの上にトラックパッドカバー（マットアクリル板）を載せます。
PCBにUSBケーブルを差し込みます。

トラックパッド上で指を動かし、カーソルが動くか確認してください。
この時点では仮固定の状態なのでカーソルの反応が悪い可能性があります。
反応すれば問題ないので、次の手順に進んでください。

![ドラックパッドの動作確認](/assets/images/futaba_build_guide/DSCF3418.jpg)

上手く動かない場合、ページ下部の[トラブルシューティング](#トラブルシューティング) を参考に対応してください。

### ケースへの組み込み

#### トラックパッドの固定

トラックパッド裏側に両面テープを貼ります。  
作業の邪魔になる場合は一度フラットケーブルを外してください。  
写真のように、白いシルクに沿って縦に貼り付けて下さい。

![両面テープの貼り付け](/assets/images/futaba_build_guide/DSCF3421.jpg)

トラックパッドからはみ出る部分はカッターなどで切り落とします。
![はみ出た個所を切り落とす](/assets/images/futaba_build_guide/DSCF3422.jpg)

フラットケーブル外している場合は、ここで取り付けます。

両面テープの剥離紙をはがし、トラックパッドをトップケースに固定します。

![ケースへの固定](/assets/images/futaba_build_guide/DSCF3432.jpg)


#### トラックパッドカバーの固定

トラックパッドカバーの保護紙をはがします。  
表裏で触り心地が異なります。触り心地の良い面が表側になるようにしてください。

裏側になる面一面に両面テープを貼り付けます。両面テープは重ねず、全面に貼るようにしてください。

![トラックパッドカバーへの両面テープの貼り付け](/assets/images/futaba_build_guide/DSCF3427.jpg)

はみ出た部分をカッターなどで切り落とします。

![両面テープの切り落とし](/assets/images/futaba_build_guide/DSCF3430.jpg)

両面テープをはがし、トラックパッドに貼り付けます。

![トラックパッドカバーの貼り付け](/assets/images/futaba_build_guide/DSCF3434.jpg)

#### PCBの取り付け

PCBの表面がトップケース側に来るようにして、PCBをたわませながら、ホイールをトップケースの隙間に差し込みます。
スイッチが干渉して作業しにくい場合は、一部のスイッチを外してください。
また、無理に差し込まないでください。

裏側から
![PCBの取り付け](/assets/images/futaba_build_guide/DSCF3440.jpg)

表から

![PCBの取り付け](/assets/images/futaba_build_guide/DSCF3441.jpg)

フラットケーブルを外している場合、PCBに差し込みトラックパッドと接続します。

![フラットケーブルの取り付け](/assets/images/futaba_build_guide/DSCF3443.jpg)


タッピングビス(短)  を使い、 PCBをトップケースに固定します。

![PCBの固定](/assets/images/futaba_build_guide/DSCF3446.jpg)

#### ケースの固定

トップケースに固定されたPCBの上に、ボトムフォームをのせます。ボトムフォームは左右・表裏があるので注意してください。フォームの穴がソケットを避けるようにのせます。

![ボトムフォームの配置](/assets/images/futaba_build_guide/DSCF3448.jpg)

フォームの上からボトムケースを載せて、タッピングビス(長) を使って固定します。

![ボトムフォームの配置](/assets/images/futaba_build_guide/DSCF3450.jpg)

分解して再度組み立てる時には、タッピングビスで新たなネジ山を作らないように注意してください。
一度タッピングビスでネジを切っている場合、最初は逆方向に回して、ネジが下に下がったところから正しい方向に回して締め付けます。こうすることで新たなネジ山を作ることなく締め付けることができます。

#### ゴム足の取り付け

ボトムケースの六角形の凹みに合わせて、ゴム足を6箇所取り付けます。ゴム足取り付け後、表面の保護フィルムをはがしてください。

![ゴム足の貼り付け](/assets/images/futaba_build_guide/DSCF3451.jpg)

ケースが浮く場合は余ったゴム足を追加で貼り付けて調整してください。
実際、ビルドガイドの撮影に使ったケースは歪みが多かったため、ケース下側に3枚、上側に2枚貼り付け、真ん中は貼り付けていません。

ホイールクリックで筐体が動かないよう、少し粘着力が強いゴム足を使っています。
グリップが強すぎて気になる場合は別のゴム足を調達してください。

キットに付属のゴム足は、 [GRIPLUSの六角形のも](https://amzn.asia/d/510jOX4)のです。

#### 最終確認

USBケーブルを差し込み、最終的な動作確認を行ってください。PCに接続しても認識しない場合は、USBケーブルが奥まで差し込まれているか確認してください。

![PCBの固定](/assets/images/futaba_build_guide/DSCF3456.jpg)


USBケーブルを奥まで差し込んでいても認識しない場合は、PCBの位置を微調整してください。
一度ボトムケースを開け、PCB固定用のネジを少し緩め固定位置を調整してください。


ここまで来たら組み立て完了です。  

![Futaba完成](/assets/images/futaba_build_guide/DSCF3459.jpg)

## 組み立てが終わったら

[Futabaのカスタマイズ]({% post_url 2025-2-1-futaba-customize-guide %}) ページを見ながら使いやすいようにカスタマイズしてください。

出来上がった作品は `#futaba_kbd` タグをつけてSNSに投稿してください。  
Futabaで楽しく快適な自作キーボードライフを過ごしてくださいね～ 


 ---

## トラブルシューティング

上手く動かない場合は以下のトラブルシューティングを参考に対応してください。  
それでも解決しない場合は、作者まで連絡してください。解決できるようサポートします。

### 認識しないキーがある場合
#### 特定のキー入力が認識されない場合

キースイッチが正しくは嵌っていないか、ソケットが正しくはんだ付けできていない可能性が高いです。  
キースイッチを刺し直しても改善しない場合は、ソケットのはんだ付けをやり直してください。

#### 特定の行または、列の入力が全て認識されない場合

RP2040-Zero が正しく接続されていない可能性があります。はんだ付けをやり直してください。

### ホイールの回転でキー入力が発生しない場合

ロータリーエンコーダーが正しくはんだ付けできているか確認してください。  
ロータリーエンコーダーのはんだ付けに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。

### ホイールクリックで入力できない場合

まず、クリッカーが正しく取り付けられているか確認してください。  
正しく取り付けられていれば、ロータリーエンコーダーを押すことでマイクロスイッチの入力ができるはずです。

次に、マイクロスイッチが正しくはんだ付けできているか確認してください。  
マイクロスイッチのはんだ付けに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。

##### トラックパッドが反応しない場合

トラックパッド側とPCB側のフラットケーブルコネクタを確認し、ケーブルがまっすぐ奥まで差し込めているか確認してください。
ケーブルに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。  

動作確認時に、ケースに載せていない場合、トラックパッド下の素材の影響を受ける場合があります。
反応しない場合は手順通り、ケースに載せてから再度確認してください。
