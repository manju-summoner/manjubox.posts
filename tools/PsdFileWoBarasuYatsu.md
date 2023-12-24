---
title: Psdファイルをバラすやつ
date: 2023-12-25
tags: [小道具]
---
## 概要
Psdファイルの各レイヤーをpng画像として出力するツールです。

# Psdファイルをバラすやつ
Psdファイルの各レイヤーをpng画像として出力します。

# ダウンロード
<Download url="https://object-storage.tyo1.conoha.io/v1/nc_4fac3ef0e6d843249e0ab2f1fc3e8f85/public/PsdFileWoBarasuYatsu.zip">Psdファイルをバラすやつをダウンロード</Download>

# 使い方
## ファイルをD&Dする場合
1. `PsdFileWoBarasuYatsu.exe`にPsdファイルをD&Dする

## 対話モードで実行する場合
1. `PsdFileWoBarasuYatsu.exe`を実行する
2. 表示されるメッセージに従ってファイルパスやオプションを指定する

## コマンドラインで実行する場合
PsdFileWoBarasuYatsu.exe "Psdファイルのパス" [オプション]

### オプション一覧
|オプション|説明|
|:--|:--|
|-o, --output|出力先フォルダのパス|
|-s, --single|レイヤー構造を無視して単一フォルダに出力する|
|-n, --numbering|出力する画像ファイル名の先頭に連番を付与する|
|-c, --crop|レイヤー画像の透過部分を切り詰める|

## ソースコード
- [manju-summoner / PsdFileWoBarasuYatsu](https://github.com/manju-summoner/PsdFileWoBarasuYatsu)