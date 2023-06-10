---
title: Windows11環境でBluetooth接続した際にAACではなくAPT-Xで接続されるようにする
date: 2023-06-11
tags: [メモ]
---
# 目的
Windows11からAACコーデックでのBluetooth接続がサポートされたが、APT-XよりもAACコーデックの優先度が高く設定されており、イヤホンがAPT-Xコーデックに対応している場合でもAACコーデックで接続されてしまう。  
筆者の環境では、APT-Xで接続できていた頃と比べ遅延が大きく口パクやSEのズレが気になったり、低音が続く音声を再生している場合にプツプツとノイズが混じった音が再生されるといった問題が発生していた。  
Bluetooth接続時に使用するコーデックの優先順位を変更する方法は（おそらく、今のところ）存在しないため、AACコーデックを無効化することでAPT-Xで接続されるようにする。  

# 無効化方法
1. レジストリエディタを起動する
1. `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\BthA2dp\Parameters`に移動する
1. `BluetoothAacEnable`の値を`0`にする
  1. キーが存在しない場合は背景部分を右クリック → 新規 → DWORD（32ビット値）
1. Bluetoothを無効化し、再度有効化する

# 参考
- [Any chance to get back Aptx Codec on Windows 11?](https://www.reddit.com/r/Windows11/comments/qouxsp/any_chance_to_get_back_aptx_codec_on_windows_11/)