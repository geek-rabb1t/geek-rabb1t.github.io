---
layout: post
title:  "GR-Trackpad65 実験キット ビルドガイド"
date:   2025-3-1 00:00:01 +0000
categories: 
  - build_guide
tags:
  - GR-Trackpad65 実験キット
  - Build Guide
banner: "/assets/images/grt65-expkit/DSCF3742.jpg"
image: "/assets/images/grt65-expkit/DSCF3742.jpg"
permalink: /grt65-expkit/build_guide
---

## 準備

組み立て前に同梱物や追加で必要な部品、必要な工具を確認してください。


### 内容物の確認

全ての写真はクリックして拡大可能できます。

| 分類     | 部品                                    | 同梱数 | 写真                                                                       |
| -------- | --------------------------------------- | -----: | -------------------------------------------------------------------------- |
| プレート | トッププレート                          |      1 | <img src="/assets/images/grt65-expkit/DSCF3665.jpg" width="100px">   |
| PCB      | メインPCB                               |      1 | <img src="/assets/images/grt65-expkit/DSCF3663.jpg" width="100px">   |
| 電子部品 | トラックパッドモジュール                |      1 | <img src="/assets/images/futaba_build_guide/DSCF3294_1.jpg" width="100px"> |
| ^^       | マイコンボード (型番: RP2040-Zero)      |      1 | <img src="/assets/images/futaba_build_guide/DSCF3295_1.jpg" width="100px"> |
| ^^       | フラットケーブル (0.5mmピッチ6ピン) \ |      1 | <img src="/assets/images/futaba_build_guide/DSCF3330.jpg" width="100px">   |
| ^^       | ピンヘッダ (2.54mmピッチ40ピン  )       |      1 | <img src="/assets/images/futaba_build_guide/DSCF3346.jpg" width="100px">   |
| 部品     | トラックパッドカバー (マット黒アクリル) |      1 | <img src="/assets/images/futaba_build_guide/DSCF3320_1.jpg" width="100px"> |
| ^^       | キャップボルト - M2 長さ10mm             |      4 | <img src="/assets/images/grt65-expkit/DSCF3735_1.jpg" width="100px"> |
| ^^       | 低頭小ねじ  - M2 長さ3.5mm        |      4 | <img src="/assets/images/grt65-expkit/DSCF3735_2.jpg" width="100px"> |
| ^^       | 両メネジスペーサー - M2 長さ6mm             |      4 | <img src="/assets/images/grt65-expkit/DSCF3734_1.jpg" width="100px"> |
| ^^       | 中空スペーサー  - M2 長さ3.5mm        |      4 | <img src="/assets/images/grt65-expkit/DSCF3734_2.jpg" width="100px"> |
| ^^       | ゴム足                                  |     4 | <img src="/assets/images/grt65-expkit/DSCF3733.jpg" width="100px">   |

注意: 付属のフラットケーブルは、写真のものより短い場合があります。

### 自分で用意するもの

#### ロープロファイルスイッチを使う場合

| 部品                                       | 必要数 | 補足                                                                  |
| ------------------------------------------ | ------ | --------------------------------------------------------------------- |
| Kailh ChocV1もしくは、Kailh ChocV2スイッチ | 3      | ChocV2互換のLofree Ghost等、 Kailh x Lofree Low-profileスイッチも対応 |
| Low Profile対応1Uサイズキーキャップ        | 3      | ChocV1とChocV2で軸の形が違うので間違えて買わないよう注意              |

#### Cherry MXまたは、MX互換スイッチを使う場合

| 部品                              | 必要数 | 補足                                                                     |
| --------------------------------- | ------ | ------------------------------------------------------------------------ |
| Cherry MXまたは、MX互換スイッチ   | 3      | ChocV2互換のLofree Ghost等、 Kailh x Lofree Low-profileスイッチも対応    |
| Cherry MX対応1Uサイズキーキャップ | 3      | ChocV1とChocV2で軸の形が違うので間違えて買わないよう注意                 |
| 中空スペーサー  - M2              | 4      | スイッチ、キーキャップの組み合わせに合う長さを調達してください \ |
| \|                                | \|     | スペーサーの長さによっては、キャップボルトも必要になります。       |


## 組み立てに必要な工具や道具


| 道具                              | 用途                                   |
| --------------------------------- | -------------------------------------- |
| はんだごて                        | 部品のはんだ付けに使用                 |
| はんだ                            | 部品のはんだ付けに使用                 |
| ニッパー                          | はみ出したピンヘッダの切り落としに使用 |
| No.0(PH0)サイズのプラスドライバー | ケースのねじ止めに使用                 |
| H1.5 サイズの6角ドライバー | ケースのねじ止めに使用（なくても何とかなります）                 |
| 逆作用ピンセット                  | はんだ付け中の部品を固定するのに使用   |
| 両面テープ                        | トラックパッドの固定に使用             |
| やすり                        | 切断面のバリ取りに使用             |

## 組み立て手順

まず、PCBの表裏について説明します。

| 面  | 実装前                                                                   | 実装後                                                                   | 説明                                                   |
| --- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------ |
| 表  | <img src="/assets/images/grt65-expkit/DSCF3663.jpg" width="200px"> | <img src="/assets/images/grt65-expkit/DSCF3737_1.jpg" width="200px"> | Front sideと印刷されています。こちらははんだ付けを行う面です。\                    |
| \|  | \|                                                                       | \|                                                                       | あらかじめ一部の部品が実装済みです。 |
| 裏  | <img src="/assets/images/grt65-expkit/DSCF3664.jpg" width="200px"> | <img src="/assets/images/grt65-expkit/DSCF3736_1.jpg" width="200px"> | Back sideと印刷されています。                           |


### 足パーツを折る

最初に、足となるパーツを手で折ります。  
足パーツは画像の赤枠の部分です。

![足パーツ](/assets/images/grt65-expkit/leg.jpg)

少し力をかけると簡単に折ることができます。

![足を折る](/assets/images/grt65-expkit/DSCF3667.jpg)


### マイコンボード(RP2040-Zero)の取り付け

#### ファームウェアの書き込み

はんだ付け前にマイコンにファームウェアを書き込みます。

マイコンにUSBケーブルを接続し、PCと接続します。  
ストレージデバイスとして認識するので、リンク先からダウンロードしたファームウェアをコピーします。  

ビルド済みファームウェアへのリンク:  
[https://github.com/geek-rabb1t/grt65-expkit/raw/refs/heads/master/firmware/geek_rabb1t_grt65_exp_kit_vial.uf2](https://github.com/geek-rabb1t/grt65-expkit/raw/refs/heads/master/firmware/geek_rabb1t_grt65_exp_kit_vial.uf2)

ストレージとして認識しない場合、RESETとBOOTボタンを同時に押してください。

![ファームウェアの書き込み](/assets/images/futaba_build_guide/screenshot_1.png)

#### マイコンのはんだ付け手順
 
キット付属のピンヘッダをニッパーで切り分けます。
切り分けた後のピンヘッダ

- 9本足： 2個
- 5本足： 1個

![切り取り後のピンヘッダ](/assets/images/futaba_build_guide/DSCF3347.jpg)

PCBの表面にUSBコネクタを上にしたRP2040-Zeroを置きます。
PCBの裏面からピンヘッダーの足の短い方を差し込みます。

![マイコンの固定](/assets/images/grt65-expkit/DSCF3682.jpg)

別アングルから見るとこんな感じです。
![マイコンの固定](/assets/images/grt65-expkit/DSCF3678.jpg)

逆作用ピンセットでRP2040-Zeroを抑えながら、マイコンとピンヘッダをはんだ付けします。

![マイコンのはんだ付け](/assets/images/grt65-expkit/DSCF3687.jpg)

PCBの裏面にはみ出たピンヘッダをニッパーで切り取ります。

![はみ出しを切り落とす](/assets/images/grt65-expkit/DSCF3691.jpg)

残りの足も同じようにはんだ付けし、不要なピンヘッダを切り取ります。

![残りのはんだ付け](/assets/images/grt65-expkit/DSCF3700.jpg)

全てのピンヘッダを切り落としたら、PCBとピンヘッダもはんだ付けします。

![裏面のはんだ付け](/assets/images/grt65-expkit/DSCF3702.jpg)

### スイッチの取り付け

PCBの裏面からスイッチを差し込み、足をはんだ付けします。

![裏面のはんだ付け](/assets/images/grt65-expkit/DSCF3739_1.jpg)

### トラックパッドの取り付け

#### トラックパッドの固定

トラックパッド裏側に両面テープを貼ります。  
白線で囲った枠の外であればどこに貼り付けてもかまいません。

![トラックパッドに両面テープを貼り付ける](/assets/images/futaba_build_guide/DSCF3422.jpg)

トッププレートの Trackpad Here と書いてある場所にトラックパッドを載せて固定します。

![トッププレートに固定](/assets/images/grt65-expkit/DSCF3707.jpg)

#### トラックパッドカバーの固定

トラックパッドカバーの保護紙をはがします。  
表裏で触り心地が異なります。触り心地の良い面が表側になるようにしてください。

裏側になる面一面に両面テープを貼り付けます。両面テープは重ねず、全面に貼るようにしてください。

![トラックパッドカバーへの両面テープの貼り付け](/assets/images/futaba_build_guide/DSCF3427.jpg)

はみ出た部分をカッターなどで切り落とします。

![両面テープの切り落とし](/assets/images/futaba_build_guide/DSCF3430.jpg)

両面テープをはがし、トラックパッドに貼り付けます。

![トラックパッドカバーの貼り付け](/assets/images/grt65-expkit/DSCF3709.jpg)


#### フラットケーブルの接続

トラックパッド裏面（部品が実装済みの面）のFFCコネクタの黒い部分をトラックパッドと平行に引っ張り、ロックを解除します。

![FFCコネクタのロック解除](/assets/images/grt65-expkit/DSCF3711.jpg)

フラットケーブルの青い面を上にして、フラットケーブルをまっすぐ差し込みます。

![フラットケーブルを差し込む](/assets/images/grt65-expkit/DSCF3712.jpg)

FFCコネクタの黒い部分を押し込み、ロックします。

![コネクタのロック](/assets/images/grt65-expkit/DSCF3713.jpg)

同じようにして、PCB側にもフラットケーブルを接続します。

![PCB側のケーブル接続](/assets/images/grt65-expkit/DSCF3715.jpg)


### ねじ止め

キャップボルトと両メネジスペーサーを使って、トッププレート、中空スペーサー、PCBを固定します。

![ネジの順番](/assets/images/grt65-expkit/DSCF3721.jpg)

足パーツはM2ネジで固定します。

![足パーツの固定](/assets/images/grt65-expkit/DSCF3722.jpg)

はみ出したフラットケーブルはトッププレートとPCBの隙間に入れ邪魔にならないようにします。

![フラットケーブルの処理](/assets/images/grt65-expkit/DSCF3723.jpg)


足パーツにゴム足を付けたら完成です。

![ゴム足](/assets/images/grt65-expkit/DSCF3725.jpg)


## 動作確認


### Vial の起動

Chrome等WebHIDに対応したブラウザの場合、 以下のURLにアクセスして ブラウザ版のアプリを起動します。

 [https://vial.rocks/](https://vial.rocks/)

`Start Vial` ボタンが表示される場合、そのままボタンを押して、 Vialを開始します。

![Start Vial](/assets/images/futaba_build_guide/screenshot_2.png)

このようなダイアログが表示されたら、`GRT65-expkit` を選択します。

![ペアリング](/assets/images/futaba_build_guide/screenshot_3.png)


ボタンが表示されない場合はWebHID非対応ブラウザなので、デスクトップアプリを使用してください。  
非対応ブラウザの場合は以下のURLから `Download Vial` を選んで、デスクトップアプリをインストールできます。

 [https://get.vial.today/](https://get.vial.today/)

ここでは利用者の多そうなブラウザ版で説明します。
デスクトップ版も同じ操作です。

### キー入力の確認

Matrix testerタブを開き、ロックを解除します。
Vialのロック解除は3つのスイッチを長押しします。

#### 各キーの動作確認

全部のキーを入力し、正しく入力できるか確認してください。  
下のスクリーンショットの状態になったらOKです。（ロック解除できている時点で入力できています。）

トラックパッドのスワイプジェスチャについてはマトリックステスターではテストできません。

![キー入力確認](/assets/images/grt65-expkit/screenshot_1.png)

上手く動かない場合、ページ下部の[トラブルシューティング](#トラブルシューティング) を参考に対応してください。  
トラックパッドは指の移動にあわせてカーソルが動けばOKです。

## 組み立てが終わったら

出来上がった作品は `#grt65_expkit` タグをつけてSNSに投稿してください。  
余計な部分を切り取れば、ブレッドボードで実験できるように設計しているので色々遊んでみてくださいね～

![完成写真](/assets/images/grt65-expkit/DSCF3732_2.jpg)

---
## カスタマイズ

### デフォルトのキーマップ

デフォルトのキーマップは以下の通りです。  
上から順に以下の設定が並んでいます。

- トラックパッドの3本指スワイプジェスチャの設定
- トラックパッドの4本指スワイプジェスチャの設定
- トラックパッド下の物理スイッチの設定

![デフォルトキーマップ](/assets/images/grt65-expkit/screenshot_2.png)

### スワイプジェスチャ
  
デフォルトのスワイプジェスチャは以下のキーバインドになっています。
Vial上で変更可能です。

#### 3本指

| スワイプ方向 |イメージ | 説明 |
|-----|---|---|
| 上 |  <img src="/assets/images/futaba/customize/3finger-up.jpg" width="200px"> | タスクビュー(Win + Tab) |
| 下 | <img src="/assets/images/futaba/customize/3finger-down.jpg" width="200px">| デスクトップ表示(Win + D) |
| 左 |<img src="/assets/images/futaba/customize/3finger-left.jpg" width="200px"> | ブラウザの戻る(マウスのボタン4) |
| 右 |<img src="/assets/images/futaba/customize/3finger-right.jpg" width="200px"> | ブラウザの進む(マウスのボタン5) |

#### 4本指


| スワイプ方向 |イメージ | 説明 |
|-----|---|---|
| 上 | <img src="/assets/images/futaba/customize/4finger-up.jpg" width="200px"> | タスクビュー(Win + Tab) |
| 下 |<img src="/assets/images/futaba/customize/4finger-down.jpg" width="200px"> | デスクトップ表示(Win + D) |
| 左 |<img src="/assets/images/futaba/customize/4finger-left.jpg" width="200px"> | 左のデスクトップへ移動(Win + Ctrl + ←) |
| 右 |<img src="/assets/images/futaba/customize/4finger-right.jpg" width="200px"> | 右のデスクトップへ移動(Win + Ctrl + →) |


### オリジナルキーコード

デフォルトのキーマップに割り当てはありませんが、Userタブに以下のオリジナルキーコードが用意されています。

| キー | 説明 |
|-----|-----|
|CHi| このキーを押している間、カーソルの移動速度が2倍になります。 |
|CLw| このキーを押している間、カーソルの移動速度が半分になります。 |
|TglV| 垂直スクロールの方向を反転します。 |
|TglH| 水平スクロールの方向を反転します。 |
|En3T| 3本指タップを有効化します。3本指タップではマウスのホイールクリック扱いになります。 |
|Dis3T| 3本指タップを無効にします。 |

TglV, TglH, En3T, Dis3T は入力するたびに、マイコンの設定が書き変わります。

例えば、垂直スクロールの方向を変えたい場合、一時的に `TglV` キーを割り当てて一度キー入力を行えばスクロール方向が反転します。
接続し直すたびに設定する必要はありません。

---

## トラブルシューティング

上手く動かない場合は以下のトラブルシューティングを参考に対応してください。  
それでも解決しない場合は、作者まで連絡してください。解決できるようサポートします。

### 認識しないキーがある場合
#### 特定のキー入力が認識されない場合

キースイッチもしくは、マイコンのはんだ付けに失敗している可能性が高いです。  
はんだ付けを確認してください。

##### トラックパッドが反応しない場合

トラックパッド側とPCB側のフラットケーブルコネクタを確認し、ケーブルがまっすぐ奥まで差し込めているか確認してください。
ケーブルに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。  

動作確認時に、ケースに載せていない場合、トラックパッド下の素材の影響を受ける場合があります。
反応しない場合は手順通り、ケースに載せてから再度確認してください。
