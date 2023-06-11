---
title: Windows11環境でBluetooth接続した際にAACではなくaptXで接続されるようにする
date: 2023-06-11
tags: [メモ]
---
# 背景
Windows11からAACコーデックでのBluetooth接続がサポートされたが、aptXよりもAACコーデックの優先度が高く設定されており、イヤホンがaptXコーデックに対応している場合でもAACコーデックで接続されてしまう。  
筆者の環境では、aptXで接続できていた頃と比べ遅延が大きく口パクやSEのズレが気になったり、低音が続く音声を再生している場合にプツプツとノイズが混じった音が再生されるといった問題が発生していた。  
Bluetooth接続時に使用するコーデックの優先順位を変更する方法は（おそらく、今のところ）存在しないため、AACコーデックを無効化することでaptXで接続されるようにする。  

# 無効化方法
1. レジストリエディタを起動する
1. `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\BthA2dp\Parameters`に移動する
1. `BluetoothAacEnable`の値を`0`にする
   - キーが存在しない場合は背景部分を`右クリック`→`新規`→`DWORD（32ビット値）`
1. Bluetoothを無効化し、再度有効化する

# 現在接続されているコーデックの確認方法
OSの機能としては搭載されていない。  
Windows ADKをインストールする必要があり確認手順も面倒だが、一応以下のページの方法で確認できる。  
- 参考：[Windows 11(10)でBluetoothの接続コーデックを確認する](https://redo495.blog/8341/)

接続コーデックを確認できるBluetoothレシーバー等を持っているのであれば、楽なのでそちらを使ったほうが良い。

# 参考
- [Any chance to get back Aptx Codec on Windows 11?](https://www.reddit.com/r/Windows11/comments/qouxsp/any_chance_to_get_back_aptx_codec_on_windows_11/)