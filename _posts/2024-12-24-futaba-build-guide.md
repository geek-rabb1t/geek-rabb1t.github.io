---
layout: post
title:  "Futabaビルドガイド"
date:   2024-12-24 08:07:33 +0000
categories: 
  - build_guide
tags:
  - Futaba
  - Build Guide
banner: "/assets/images/banners/home.jpg"
---
## 準備

組み立て前に同梱物や、追加で必要な部品を確認してください。


### 内容物の確認

| 分類     | 部品                                       | 同梱数 | 写真 |
| -------- | ------------------------------------------ | -----: | ---- |
| ケース   | トップケース                               |      1 |   <font color=red>写真</font>   |
|          | ボトムケース                               |      1 |      |
| フォーム | トップフォーム (右・中・左)                |      1 |      |
|          | ボトムフォーム (右・中・左)                |      1 |      |
| PCB      | メインPCB                                  |      1 |      |
| 電子部品 | トラックパッドモジュール                   |      1 |      |
|          | chocソケット                               |     49 |      |
|          | ロータリーエンコーダー(型番: EC12E2420301) |      1 |      |
|          | マイコンボード (型番: RP2040-Zero)         |      1 |      |
|          | フラットケーブル (0.5mmピッチ6ピン  )      |      1 |      |
| 部品     | クリッカー                                 |      1 |      |
|          | ホイール                                   |      1 |      |
|          | トラックパッドカバー (マット黒アクリル)    |      1 |      |
|          | タッピングビス(短)  - M3 長さ6mm           |      2 |      |
|          | タッピングビス(長)  - M3 長さ8mm           |      6 |      |
|          | ゴム足                                     |     10 |      |


- メインPCBはダイオードとFFCコネクタがあらかじめ実装済みです。

### 自分で用意するもの

| 部品                                       | 必要数 | 補足                                                                   |
| ------------------------------------------ | ------ | ---------------------------------------------------------------------- |
| Kailh ChocV1もしくは、Kailh ChocV2スイッチ | 49     | ChocV2互換のLofree Ghost等、 Kailh x Lofree Low-profileスイッチも対応 |
| Low Profile対応1Uサイズキーキャップ        | 49     | ChocV1とChocV2で軸の形が違うので間違えて買わないよう注意               |


ぎーくらびっとのおススメスイッチ
- [Kailh Deep Sea Silent MINI ロープロファイルスイッチ Islet](https://talpkeyboard.net/items/66a056514c088e035d0344b3)
- [Kailh Deep Sea Silent MINI ロープロファイルスイッチ Whale](https://talpkeyboard.net/items/66a0596a545dc7002b5dea18)
- [Kailh x Lofree Ghost](https://lofree.co.jp/products/ghost-low-profile-pom-switches?variant=50487412556007)

確認済みキーキャップ
- [Tai-Hao Thins](https://talpkeyboard.net/?category_id=66e79046a6782d33e6380dab)
- [XVXロープロファイルキーキャップ](https://amzn.asia/d/cjRH1xz)



## 組み立てに必要な工具や道具


| 道具             | 用途                             |
| ---------------- | -------------------------------- |
| はんだごて       |                                  |
| はんだ           |                                  |
| ニッパー         |                                  |
| ドライバー       |                                  |
| 逆作用ピンセット | chocソケットの取り付けに使います |
| 両面テープ       | トラックパッドの固定に使用します |

## 組み立て方

まず、PCBの表裏について説明します。

- 表面  
表面はキースイッチをはめる面です。  
こちらの面にはマイクロスイッチとロータリーエンコーダーを実装します。
<font color=red>実装前の写真</font>
<font color=red>実装後の写真</font>

- 裏面  
Futabaという文字が印刷されており、あらかじめダイオードやFFCコネクタが実装されている面が裏面です。  
こちらの面には、chocソケットと、マイコンボードを実装します。
<font color=red>実装前の写真</font>
<font color=red>実装後の写真</font>


### 電子部品のはんだ付け

#### chocソケットの取り付け

PCBの裏面で作業します。

chocソケットには向きがあります。向きを間違えるとスイッチが外れやすくなったり、キー入力できない場合があります。ソケットの向きを間違えないように注意してください。

<font color=red>写真</font>

また、PCBが薄いためchocソケットがPCBからはみ出します。そのため、一つ一つ、逆作用ピンセットで抑えながらはんだ付けしてください。

<font color=red>写真</font>

ピンセットで固定するため以下の順番に作業してください。

<font color=red>写真</font>

#### マイコンボード(RP2040-Zero)の取り付け


**事前にマイコンが不良品でないか確認する**


PCBの裏面にRP2040-Zeroに付属のピンヘッダーを差し込み、その上にRP2040-Zeroを載せます。
写真のように、USBコネクタの実装面が見えるように差し込みます。
逆作用ピンセットでにRP2040-Zeroを抑えながら、PCBからはみ出た四隅のピンをニッパーで切ります。
ニッパーで切り落としたら、四隅だけはんだ付けします。

<font color=red>写真</font>

RP2040-Zero からはみ出たピンも同じようにニッパーで切り落としはんだ付けします。

<font color=red>写真</font>

これでPCBとRP2040-Zeroが固定されるので、逆作用ピンセットは外してください。

PCB側の残りのピンを全て切り取り、はんだ付けします。

<font color=red>写真</font>

RP2040-Zeroも同様にはみ出たピンを全て切り取り、はんだ付けします。

<font color=red>写真</font>

#### マイクロスイッチの取り付け

ここからは、PCBの向きが変わります。注意してください。

PCBの表面にマイクロスイッチを差し込みます。
マイクロスイッチを逆作用ピンセットで抑えた状態ではみ出た足をニッパーで切り取ります。

<font color=red>写真</font>

ピンセットで固定したままはんだ付けします。

<font color=red>写真</font>

#### ロータリーエンコーダーの取り付け

PCBの表側からロータリーエンコーダーを差し込みます。
PCBからはみ出した細い3本の足をニッパーで切り取ります。

<font color=red>写真</font>

ニッパーで切り取った足をはんだ付けします。

<font color=red>写真</font>

2本の太い足を切り取り、はんだ付けします。

<font color=red>写真</font>


はんだ付けは以上となります。

### 各種部品の取り付け

#### スイッチの取り付け

PCBの表面の上にトップフォームを重ね、上からスイッチをはめ込みます。

<font color=red>写真</font>

#### クリッカーの取り付け

PCBの表面のからクリッカーをはめます。
写真の赤枠部分をつぶすようにつまみながら、下に押し込みます。

<font color=red>写真</font>

取り外すときは、同じようにつまみながら引き抜きます。

#### ホイールの取り付け

クリッカーが取り付け済みであることを確認してから、エンコーダーにホイールを取り付けます。

<font color=red>写真</font>

### 動作確認

#### ファームウェアの書き込み

#### 各キーの動作確認

全部のキーを入力し、正しく入力できるか確認してください。


##### 特定のキー入力が認識されない場合

キースイッチが正しくは嵌っていないか、ソケットが正しくはんだ付けできていない可能性が高いです。
キースイッチを刺し直しても改善しない場合は、ソケットのはんだ付けをやり直してください。

##### 特定の行または、列の入力が全て認識されない場合

RP2040-Zero が正しく接続されていない可能性があります。はんだ付けをやり直してください。


#### ホイールの動作確認

ホイールの回転とホイールクリックで入力が発生するか確認してください。

##### ホイールの回転で入力できない場合

ロータリーエンコーダーが正しくはんだ付けできているか確認してください。
ロータリーエンコーダーのはんだ付けに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。

##### ホイールクリックで入力できない場合

マイクロスイッチが正しくはんだ付けできているか確認してください。
マイクロスイッチのはんだ付けに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。

#### トラックパッドの動作確認

始めに、PCBからUSBケーブルを抜きます。


<font color=red>写真</font>

FFCコネクタの黒い部分をトラックパッドと平行に引っ張り、ロックを解除します。

<font color=red>写真</font>

フラットケーブルの青い面を上にして、フラットケーブルをまっすぐ差し込みます。

<font color=red>写真</font>

FFCコネクタの黒い部分を押し込み、ロックします。

<font color=red>写真</font>


トラックパッドをトップケースの上に載せます。
この時点では固定しません。

<font color=red>写真</font>

トラックパッドと同様の手順でフラットケーブルをPCBに接続します。

<font color=red>写真</font>

トラックパッドの上にトラックパッドカバー（マットアクリル板）を載せます。
このとき、トラックパッドとカバーの間に隙間ができないよう注意してください。

<font color=red>写真</font>

PCBにUSBケーブルを差し込みます。

<font color=red>写真</font>

トラックパッド上で指を動かし、カーソルが動くか確認してください。
この時点では仮固定の状態なのでカーソルの反応が悪い可能性があります。
強めに触って反応すれば問題ないので、次の手順に進んでください。

<font color=red>写真</font>

##### トラックパッドが反応しない場合

トラックパッド側とPCB側のフラットケーブルコネクタを確認し、ケーブルがまっすぐ奥まで差し込めているか確認してください。
ケーブルに問題がない場合は、RP2040-Zero のはんだ付けを確認してください。

### ケースへの組み込み

#### トラックパッドの固定

写真のようにトラックパッド裏側に両面テープを貼ります。

<font color=red>写真</font>


トラックパッドにフラットケーブルを取り付けます。

<font color=red>写真</font>

両面テープの剥離紙をはがし、トラックパッドをトップケースに固定します。

<font color=red>写真</font>

トラックパッドカバーの保護紙をはがします。
表裏で触り心地が異なります。

<font color=red>写真</font>

#### PCBの取り付け

PCBの表面がトップケース側に来るようにして、PCBをたわませながら、ホイールをトップケースの隙間に差し込みます。
スイッチが干渉して作業しにくい場合は、一部のスイッチを外してください。
このとき、無理な力を入れないでください。

<font color=red>写真</font>

タッピングビス(短)  を使い、 PCBをトップケースに固定します。

<font color=red>写真</font>

フラットケーブルをPCBに差し込み、トラックパッドと接続します。

<font color=red>写真</font>

#### ケースの固定

トップケースに固定されたPCBの上に、ボトムフォームをのせます。ボトムフォームは表裏があるので注意してください。フォームの穴がソケットを避けるようにのせます。

<font color=red>写真</font>

フォームの上からボトムケースを載せて、タッピングビス(長) を使って固定します。

<font color=red>写真</font>

分解して再度組み立てる時には、タッピングビスで新たなネジ山を作らないように注意してください。
一度タッピングビスでネジを切っている場合、最初は逆方向に回して、ネジが下に下がったところから正しい方向に回して締め付けます。こうすることで新たなネジ山を作ることなく締め付けることができます。

#### ゴム足の取り付け

ボトムケースの六角形の凹みに合わせて、ゴム足を6箇所取り付けます。ゴム足取り付け後、表面の保護フィルムをはがしてください。

<font color=red>写真</font>

もしケースが浮く場合は余ったゴム足を追加で貼り付けて調整してください。
ホイールクリックで筐体が動かないよう、少し粘着力が強いゴム足を使っています。
グリップが強すぎて気になる場合は別のゴム足を調達してください。

キットに付属のゴム足は、 [GRIPLUSの六角形のも](https://amzn.asia/d/510jOX4)のです。

#### 最終確認

USBケーブルを差し込み、最終的な動作確認を行ってください。PCに接続しても認識しない場合は、USBケーブルが奥まで差し込まれているか確認してください。奥まで差し込んでいても認識しない場合は、PCBの固定位置を調整してください。

<font color=red>写真</font>

ここまで来たら組み立て完了です。  
出来上がった作品は `#futaba_kbd` タグをつけてSNSに投稿してください。  
Futabaで楽しく快適な自作キーボードライフを過ごしてくださいね～


## 組み立てが終わったら

- [Futabaのカスタマイズ]({% post_url 2024-12-24-futaba-customize-guide %}) ページを見ながら使いやすいようにカスタマイズしてください。
 
