---
title: Grok TTSの音声を利用する
date: 2026-05-07
tags: [YMM4]
keywords: [Grok, xAI]
---
## Grok TTSとは
[Grok TTS](https://x.ai/)はxAI社によって運営されているクラウド音声合成サービスです。  
外部連携APIを使用し、YMM4から直接音声を生成できます。  
利用には別途APIキーの取得が必要です。  
- [xAI](https://x.ai/)
- [Grok TTS ドキュメント](https://docs.x.ai/docs/models)

## 利用方法
1. [xAI Console](https://console.x.ai/)を開き、アカウントを作成する
1. APIキーを取得する
   1. [API Keys](https://console.x.ai/team/default/api-keys)ページを開く
   1. *Create API Key*をクリックする
   1. 任意の名前を入力し、APIキーを作成する
   1. 表示されたAPIキーをコピーする
1. ゆっくりMovieMaker4を起動する
1. APIキーをYMM4に設定する
   1. *ファイル(F)*→*設定*から設定ウィンドウを開く
   1. *音声合成*→*Grok TTS*を選択する
   1. *APIキー*欄に、*2-4.*でコピーしたAPIキーを貼り付ける
1. *ファイル(F)*→*キャラクターの編集*からキャラクター編集ウィンドウを開く
1. *ボイス*→*声質*欄で、Grok TTSの音声（eve, ara, rex, sal, leo）を選択する
1. キャラクターを選択後、*ここに台詞を入力*欄にセリフを入力し、*追加*ボタンをクリックする

## パラメータ
- **言語**  
  読み上げる言語をBCP-47形式の言語コード（例: `ja`, `en`, `pt-BR`）で指定します。  
  `auto`を指定すると、テキストから自動的に判定されます。

## 利用条件等
- [xAI Terms of Service](https://x.ai/legal/terms-of-service)
- [xAI Acceptable Use Policy](https://x.ai/legal/acceptable-use-policy)

## 関連リンク
- [xAI](https://x.ai/)
- [xAI Console](https://console.x.ai/)
