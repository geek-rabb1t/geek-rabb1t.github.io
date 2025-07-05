---
layout: post
title:  "Futabaカスタマイズガイド"
date:   2025-2-1 00:00:00 +0000
categories: 
  - customize
tags:
  - Futaba
  - Customize Guide
banner: "/assets/images/futaba/DSCF3466_1.jpg"
image: "/assets/images/futaba/DSCF3466_1.jpg"
permalink: /futaba/customize_guide
---


## キーマップ

Vial上でカスタマイズできます。  
デフォルトでは以下のキーマップになっています。
で好きなように変更してください。

### レイヤー0(デフォルトレイヤー)

![layer-0](/assets/images/futaba/customize/layer-0.jpg)

右側はトラックパッドの設定エリアです。
<img src="/assets/images/futaba/customize/layer-0-1.jpg" width="500px"> 

### レイヤー1


![layer-1](/assets/images/futaba/customize/layer-1.jpg)

### レイヤー2


![layer-2](/assets/images/futaba/customize/layer-2.jpg)


## トラックパッド

Vial上でカスタマイズできます。  
一部の項目はレイヤー0(デフォルトレイヤー) でのみ設定可能です。

タップやスワイプジェスチャの挙動に加え、カーソル速度やスクロール速度などを設定可能です。


### カーソルに関する設定

レイヤー0(デフォルトレイヤー) で設定します。  
他のレイヤーに設定しても機能しないので注意してください。

<img src="/assets/images/futaba/customize/layer-0-1-cursor.jpg" width="500px"> 

項目ごとに決まったキーコードのみ指定可能です。
無効なキーコードが指定された場合は初期値を使います。

この項目はキーボードを再接続するまで反映されません。

| 項目           | Vial上の表示        | 指定可能な値      | 初期値  | 説明                                                                           |
| -------------- | ------------------- | ----------------- | ------- | ------------------------------------------------------------------------------ |
| カーソル速度   | Cursor Speed        | `Val 1` - `Val 9` | `Val 5` | カーソルの移動速度を設定します。数値が大きいほど速くなります。                 |
| カーソルの加速 | Cursor Acceleration | `ON`, `OFF`       | `OFF`   | カーソルの加速有無を設定します。                                               |
| 慣性カーソル   | Inertia Cursor      | `ON`, `OFF`       | `ON`    | カーソル移動中に指を離したときにそのままカーソルを移動するかどうか設定します。 |
| カーソル補正   | Cursor Correction   | `Val 1` - `Val 9` | `Val 2` | カーソル補正の強さを設定します。 \                                             |
| \|             | \|                  | \|                | \|      | 数値を大きくすると補正が強くなりますが、遅延が大きくなります。                 |

### スクロールに関する設定

レイヤー0(デフォルトレイヤー) で設定します。
他のレイヤーに設定しても機能しないので注意してください。

<img src="/assets/images/futaba/customize/layer-0-1-scroll.jpg" width="500px"> 

項目ごとに決まったキーコードのみ指定可能です。
無効なキーコードが指定された場合は初期値を使います。

この項目はキーボードを再接続するまで反映されません。

| 項目           | Vial上の表示        | 指定可能な値      | 初期値  | 説明                                                                           |
| -------------- | ------------------- | ----------------- | ------- | ------------------------------------------------------------------------------ |
| スクロール速度   | Scroll Speed        | `Val 1` - `Val 9` | `Val 4` | スクロール速度を設定します。数値が大きいほど速くなります。                 |
| 垂直スクロールの反転 | Reverse Vertical Scroll | `ON`, `OFF`       | `ON`   | 垂直方向のスクロールを反転するかどうか設定します。                                               |
| 水平スクロールの反転 | Reverse Horizontal Scroll | `ON`, `OFF`       | `OFF`   | 水平方向のスクロールを反転するかどうか設定します。                                               |
| 慣性スクロール   | Inertia Scroll      | `ON`, `OFF`       | `ON`    | スクロール中に指を離したときにそのままスクロールを継続するかどうか設定します。 |
| スクロールのみ   | Scroll Only   |  `ON`, `OFF`       | `OFF`  | ONにすると、カーソル移動が無効になりスクロールのみになります。 |


### タップ

レイヤーごとに個別の設定が可能です。  
1本指から4本指までのタップ挙動を設定できます。  

<img src="/assets/images/futaba/customize/layer-0-1-tap.jpg" width="500px"> 

デフォルトは以下の設定になっています。

| 項目 | Vial上の表示 | 初期値 | 説明 |
| ---- | ------------ | ------ | ---- |
| 1本指タップ | One Finger Tap             |  Mouse1      |  左クリック    |
| 2本指タップ | Two Finger Tap             |  Mouse2      |  右クリック    |
| 3本指タップ | Three Finger Tap             |  Mouse3      |  ホイールクリック    |
| 4本指タップ | Four Finger Tap             | Win + S      |  検索機能へのショートカット    |

### スワイプジェスチャ

レイヤーごとに個別の設定が可能です。  
3本指、4本指のスワイプジェスチャの挙動を設定できます。    

#### 3本指

![layer-0-3finger](/assets/images/futaba/customize/layer-0-3finger.jpg)

デフォルトでは以下のキーバインドになっています。

| スワイプ方向 |イメージ | 説明 |
|-----|---|---|
| 上 |  <img src="/assets/images/futaba/customize/3finger-up.jpg" width="200px"> | タスクビュー(Win + Tab) |
| 下 | <img src="/assets/images/futaba/customize/3finger-down.jpg" width="200px">| デスクトップ表示(Win + D) |
| 左 |<img src="/assets/images/futaba/customize/3finger-left.jpg" width="200px"> | ブラウザの戻る(マウスのボタン4) |
| 右 |<img src="/assets/images/futaba/customize/3finger-right.jpg" width="200px"> | ブラウザの進む(マウスのボタン5) |

#### 4本指

![layer-0-4finger](/assets/images/futaba/customize/layer-0-4finger.jpg)

デフォルトでは以下のキーバインドになっています。


| スワイプ方向 |イメージ | 説明 |
|-----|---|---|
| 上 | <img src="/assets/images/futaba/customize/4finger-up.jpg" width="200px"> | タスクビュー(Win + Tab) |
| 下 |<img src="/assets/images/futaba/customize/4finger-down.jpg" width="200px"> | デスクトップ表示(Win + D) |
| 左 |<img src="/assets/images/futaba/customize/4finger-left.jpg" width="200px"> | 左のデスクトップへ移動(Win + Ctrl + ←) |
| 右 |<img src="/assets/images/futaba/customize/4finger-right.jpg" width="200px"> | 右のデスクトップへ移動(Win + Ctrl + →) |

## オリジナルファームウェアの作成

Futabaのファームウェアのソースは以下のリポジトリにあります。  
ライセンスの範囲であれば、自由に改変してかまいません。

[https://github.com/geek-rabb1t/vial-qmk/tree/gr_master/keyboards/geek_rabb1t/futaba](https://github.com/geek-rabb1t/vial-qmk/tree/gr_master/keyboards/geek_rabb1t/futaba)


### ファームウェアの書き込み方法

一度、PCから切断し、Futabaの裏側に空いている穴をシャープペンシル等で押しながらUSBケーブルを接続してください。

![ファームウェア書き込みモードへの移行](/assets/images/futaba/DSCF3451_1.jpg)

ストレージデバイスとして認識するので、ファームウェアをドラッグドロップして書き込んでください。

![ファームウェアの書き込み](/assets/images/futaba_build_guide/screenshot_1.png)

## ホイールを軽くする

使用するロータリーエンコーダーを変更することでホイールの操作を軽くすることができます。  
遊舎工房さん等で取り扱いのある[低トルクタイプのロータリーエンコーダー(EC12E2440301)](https://shop.yushakobo.jp/products/2141)が対応品です。
