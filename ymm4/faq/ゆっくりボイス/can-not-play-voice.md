---
title: 生成済みの合成音声が再生されなくなる
date: 2024-04-21
tags: [YMM4]
---
## 発生する問題
- YMM4を起動後しばらくすると、生成済みの合成音声が再生されなくなる

## 原因
お使いのPCにインストールされているセキュリティソフト等によって、生成された合成音声のキャッシュファイルが削除されている可能性があります

## 対策
- YMM4の実行ファイルをセキュリティソフトの例外リストに追加する
- キャッシュファイルが保存されているフォルダをセキュリティソフトの例外リストに追加する
  - *ヘルプ(H)*→*その他*→*作業フォルダを開く*から、キャッシュファイルが保存されているフォルダを確認できます