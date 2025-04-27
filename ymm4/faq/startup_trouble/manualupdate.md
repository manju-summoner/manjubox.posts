---
title: 手動アップデート（再インストール）する
date: 2022-05-12
tags: [YMM4]
keywords: [アップデート, 更新, 再インストール, インストール, インストーラ]
---
## 症状
- 自動アップデートに失敗する
- YMM4が起動しない
- Unable to load one or more of the requested types. Could not load file or assembly '<アセンブリ名>'. Format of the executable (.exe) or library (.dll) is invalid.と表示される

## 手動アップデート（再インストール）手順
> **Note**
> この方法を実行しても設定（キャラクター設定など）はリセットされません。

1. YMM4を終了させる
1. 設定ファイルをバックアップする**（推奨）**  <br/><small>念のため、作業前に設定ファイルをバックアップしておくことをおすすめします。</small>  
   1. YMM4フォルダ内の*user*フォルダを任意の場所にコピーする
   1. アップデート後に設定が初期化されるなどの問題が発生した場合、既存の*user*フォルダを削除し、バックアップした*user*フォルダをYMM4フォルダにコピーすることで元の状態に戻せます。
1. [ゆっくりMovieMaker4配布ページ](../../index.md)からYMM4を再ダウンロードする
1. ダウンロードしたzipファイルを展開（解凍）する
![スクリーンショット](manualupdate_1543.png)
1. 展開したファイルを元のYMM4フォルダにコピーする
![スクリーンショット](manualupdate_1711.png)
1. *ファイルを置き換える(R)*を選択する
![スクリーンショット](manualupdate_1830.png)
1. コピー完了後、YMM4を起動する