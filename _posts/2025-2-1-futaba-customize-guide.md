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
permalink: /futaba/customize_guide
---


## キーマップ

Vial上でカスタマイズできます。  
デフォルトでは以下のキーマップになっていますので好きなように変更してください。

### レイヤー0(デフォルトレイヤー)

<font color=red>Vialのマッピング間違ってる。</font>
![layer-0](/assets/images/futaba/customize/layer-0.jpg)

### レイヤー1


![layer-1](/assets/images/futaba/customize/layer-1.jpg)

### レイヤー2


![layer-2](/assets/images/futaba/customize/layer-2.jpg)

### レイヤー3(カスタマイズレイヤー)

![layer-3](/assets/images/futaba/customize/layer-3.jpg)

## トラックパッド

デフォルトのキーマップの場合、以下のキーを押してカスタマイズレイヤーに入ります。

![to-layer-3](/assets/images/futaba/customize/to-layer-3.jpg)

カスタマイズレイヤーからもとのデフォルトのレイヤーに戻るには、ホイールクリックを押してください。  
カスタマイズレイヤーでは赤枠のキーでトラックパッドの動作を変更できます。

![layer-3-note](/assets/images/futaba/customize/layer-3-note.jpg)


| キー | 説明 |
|-----|-----|
|TglV| 垂直スクロールの方向を反転します。 |
|TglH| 水平スクロールの方向を反転します。 |
|En3T| 3本指タップを有効化します。3本指タップではマウスのホイールクリック扱いになります。 |
|Dis3T| 3本指タップを無効にします。 |


### スワイプジェスチャ

3本指、4本指のスワイプジェスチャはVial上で変更可能です。  
デフォルトでは以下のキーバインドになっています。

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

## オリジナルファームウェアの作成

Futabaのファームウェアのソースは以下のリポジトリにあります。  
ライセンスの範囲であれば、自由に改変してかまいません。

[https://github.com/geek-rabb1t/vial-qmk/tree/futaba/keyboards/futaba](https://github.com/geek-rabb1t/vial-qmk/tree/futaba/keyboards/futaba)


### ファームウェアの書き込み方法

一度、PCから切断し、Futabaの裏側に空いている穴をシャープペンシル等で押しながらUSBケーブルを接続してください。

![ファームウェア書き込みモードへの移行](/assets/images/futaba/DSCF3451_1.jpg)

ストレージデバイスとして認識するので、ファームウェアをドラッグドロップして書き込んでください。

![ファームウェアの書き込み](/assets/images/futaba_build_guide/screenshot_1.png)

## ホイールを軽くする

使用するロータリーエンコーダーを変更することでホイールの操作を軽くすることができます。  
遊舎工房さん等で取り扱いのある[低トルクタイプのロータリーエンコーダー(EC12E2440301)](https://shop.yushakobo.jp/products/2141)が対応品です。
