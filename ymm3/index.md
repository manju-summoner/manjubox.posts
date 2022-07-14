---
title: ゆっくりMovieMaker3
date: 2014-09-14
tags: [YMM3]
excerpt: ゆっくり実況プレイ動画用編集支援ソフト「ゆっくりMovieMaker3」の配布ページです
---

> **Note**
> 後継となる[ゆっくりMovieMaker4](../ymm4/index.md)が正式リリースされました。  
> 今後、YMM3の更新及びサポートは行われないため、[YMM4](../ymm4/index.md)への移行をご検討ください。

<NiconicoPlayer id="sm20953272" title="ゆっくり実況がすごく簡単に作れるようになった【ゆっくりMovieMaker3】"/>

「ゆっくり実況プレイ動画」用の動画編集支援ソフトです。  
セリフ追加のほか、簡単な編集機能を搭載しています。

## 動作環境
- Windows XP 以上
- .NET Framework 4 以上
- DirectX9.0c 以上
- PixelShader2.0 / 3.0

## 対応ファイル形式
- 動画ファイル
  - .avi .mp4 .wmv .mpg .mpeg
- 画像ファイル
  - .bmp .jpg .jpeg .png
- 音声ファイル
  - .wav .mp3
- [カスタムボイス](./tips/yukkuri/h201342223491450.md)
  - .wav .mp3
- [キャラ素材](#キャラ素材について)
  - キャラ素材スクリプト Ver4c に対応したキャラ素材
  - **※キャラ素材スクリプトVer5以降専用のキャラ素材は動作しません**

## ダウンロード
**本ソフトを使用して実況動画を作成し、ニコニコ動画で動画を公開する場合、動画の親作品に[sm20953272](http://www.nicovideo.jp/watch/sm20953272)の登録をお願いします。 [>>登録方法](./tutorial/output/h20134199232488.md) / [>>キャラ素材を使用している場合](#キャラ素材について)**

<Download url="https://object-storage.tyo1.conoha.io/v1/nc_4fac3ef0e6d843249e0ab2f1fc3e8f85/public/YukkuriMovieMaker_v3.4.8.1.exe">ゆっくりMovieMaker3（.exe版）をダウンロード</Download>
<Download url="https://object-storage.tyo1.conoha.io/v1/nc_4fac3ef0e6d843249e0ab2f1fc3e8f85/public/YukkuriMovieMaker_v3.4.8.1.zip">ゆっくりMovieMaker3（.zip版）をダウンロード</Download>

### 追加ファイル
#### IPADicを使用した「漢字→読み」変換を利用する場合
<Download url="https://object-storage.tyo1.conoha.io/v1/nc_4fac3ef0e6d843249e0ab2f1fc3e8f85/public/YukkuriMovieMaker_v3_ipadic.exe">追加ファイル（IPADic）をダウンロード</Download>

#### UniDicを使用した「漢字→読み」変換を利用する場合  
「発音」に自動的にアクセントが付与されるようになります。
<Download url="https://object-storage.tyo1.conoha.io/v1/nc_4fac3ef0e6d843249e0ab2f1fc3e8f85/public/YukkuriMovieMaker_v3_unidic.exe">追加ファイル（UniDic）をダウンロード</Download>

### ゆっくりMovieMaker4
- [ゆっくりMovieMaker4配布ページ](../ymm4/index.md)

## キャラ素材について
<NiconicoCard id="sm22479399" title="【キャラ素材】アニメーション機能紹介"/>

セリフに合わせて自動的に口パク・瞬きを行うアニメーション素材です。   
キャラ素材を利用する場合、事前に素材のダウンロードや初期設定を行う必要があります。

- [キャラ素材を入手する（外部リンク：nicotalk&キャラ素材配布所）](http://www.nicotalk.com/charasozai.html)
- [キャラ素材を使用するための準備](./tutorial/charasozai/index.md)

### ゆっくりMovieMakerで動作するキャラ素材について
キャラ素材スクリプトVer4cで動作するキャラ素材を使用する必要があります。  
**キャラ素材スクリプトVer5以降専用のキャラ素材はYMM上では動作しません。**

### 規約遵守のお願い
[![スクリーンショット](index-1.jpg)](http://www.nicotalk.com/charasozai.html#rule)

### コンテンツツリー登録のお願い（ニコニコ動画へ投稿する場合）
キャラ素材を使用する場合、以下の動画をコンテンツツリーに登録して下さい。

- [sm20953272（ゆっくりMovieMakerの紹介動画）](http://www.nicovideo.jp/watch/sm20953272)
- [sm27609245（キャラ素材の紹介動画）](http://www.nicovideo.jp/watch/sm27609245)
- [im1696493](http://seiga.nicovideo.jp/seiga/im1696493)
- 使用したキャラ素材側で指定されている作品

**キャラ素材の仕様及びAviUtl用スクリプトはゆっくりMovieMaker独自の機能ではありません。**
キャラ素材の動作仕様及びAviUtl用スクリプトは、[ズーズ](https://twitter.com/vocatalk)様によって[nicotalk](http://www.nicotalk.com/)用に製作されたものをお借りしています。  
YMMの紹介・解説をする際やキャラ素材を配布する際、キャラ素材がYMMの独自機能であったり、仕様及び製作者が饅頭遣いであると誤認されるような書き方をしないでください。

## 対応音声合成エンジン
### AquesTalk / AquesTalk2
ゆっくり実況プレイ動画でお馴染みの、スタンダードなゆっくりボイスです。
- [AquesTalk - 組み込み用 規則音声合成エンジン ](http://www.a-quest.com/products/aquestalk.html)

### 唄詠（SAPI）
好みのUTAU音源を選択して喋らせることが出来る、UTAU音源用のTTSエンジンです。
- [唄詠 | 翔星ワールド ](http://shinta.coresv.com/software/utayomi_jpn/)
- [UTAU音源ライブラリ一覧（ニコニコ大百科）](http://dic.nicovideo.jp/a/utau%E9%9F%B3%E5%A3%B0%E3%83%A9%E3%82%A4%E3%83%96%E3%83%A9%E3%83%AA%E4%B8%80%E8%A6%A7)

### その他、SAPI対応音声合成エンジン
その他、SAPIに対応している音声合成エンジンを使用可能です。

### カスタムボイス機能
ゆっくりMovieMakerの「カスタムボイス」機能を使用することで、上記一覧に載っていない音声合成エンジンで出力した音声ファイルも、ゆっくりボイスとして使用することが可能です。
- [詳細](./tips/yukkuri/h201342223491450.md)

## 外部アプリケーション
YMM3で利用可能な外部アプリの一覧です。（[掲載依頼はこちら](../%E3%81%8A%E5%95%8F%E3%81%84%E5%90%88%E3%82%8F%E3%81%9B.md)）
- 利用方法や不具合に関しては各アプリの開発者へお問い合わせください。
- 外部アプリは自己責任で利用してください。  
  このページへの掲載は安全性を保証するものではありません。

### ゆっくりMovieMaker3用ExcelVBAマクロ
Excelで作成した台本をもとに、タイムラインにボイスアイテムを配置するExcelマクロです。

配布元：[ゆっくりMovieMaker3入力を自動化するExcelVBAマクロ【ゆっくり解説】](http://tamajimu.sytes.net/archives/930)  
開発者：[ゆっくり亭](https://twitter.com/Tamaji1234)様


## 関連サイト
- [AviUtlのお部屋](http://spring-fragrance.mints.ne.jp/aviutl/)
- [nicotalk&キャラ素材配布所](http://www.nicotalk.com/charasozai.html)
- [キャラ素材配布ページ – nicotalk&キャラ素材配布所](http://www.nicotalk.com/charasozai.html)
- [唄詠｜翔星ワールド](https://shinta.coresv.com/software/utayomi_jpn/)
- [VIPで初心者がゲーム実況するには@ Wiki – ゆっくりMovieMaker](https://www18.atwiki.jp/live2ch/pages/339.html)
- [【AviUtl】ゆっくりムービーメーカーの使い方【解説･実況】](https://aviutl.info/yukkuri-moviemaker/)