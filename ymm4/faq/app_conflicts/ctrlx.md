---
title: テキストの切り取りをすると、YMM4がプチフリーズし切り取り動作も行われない
date: 2023-10-22
tags: [YMM4]
keywords: [Ctrl+X,切り取,カット,CtrlX]
---
## 発生する問題
テキスト入力欄でCtrl+Xキーを押すなどしてテキストを切り取ると、YMM4がプチフリーズし、切り取りも行えない。

## 発生する環境
WindowsUpdateが原因で症状が発生している可能性があります。
この問題はWPFというUIライブラリを使用しているアプリ全般で発生し、YMM4の過去のバージョンに遡って問題が発生しています。  
将来のWindowsUpdateで問題が解消されることをお待ちいただけると幸いです。