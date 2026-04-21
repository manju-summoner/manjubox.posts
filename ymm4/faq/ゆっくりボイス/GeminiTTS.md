---
title: Gemini TTSの音声を利用する
date: 2026-04-21
tags: [YMM4]
keywords: [Gemini, Google]
---
## Gemini TTSとは
[Gemini TTS](https://ai.google.dev/gemini-api/docs/speech-generation)はGoogle社によって運営されているクラウド音声合成サービスです。  
外部連携APIを使用し、YMM4から直接音声を生成できます。  
利用には別途APIキーの取得が必要です。  
- [Google AI Studio](https://aistudio.google.com/)
- [Gemini API 音声生成ドキュメント](https://ai.google.dev/gemini-api/docs/speech-generation)

## 利用方法
1. [Google AI Studio](https://aistudio.google.com/)にGoogleアカウントでログインする
1. APIキーを取得する
   1. [API Keys](https://aistudio.google.com/apikey)ページを開く
   1. *APIキーを作成*（Create API key）をクリックする
   1. 利用するGoogle Cloudプロジェクトを選択、または新規作成する
   1. 表示されたAPIキーをコピーする
1. ゆっくりMovieMaker4を起動する
1. APIキーをYMM4に設定する
   1. *ファイル(F)*→*設定*から設定ウィンドウを開く
   1. *音声合成*→*GeminiTTS*を選択する
   1. *APIキー*欄に、*2-4.*でコピーしたAPIキーを貼り付ける
   1. *モデル*欄で、使用するモデル（例: `gemini-2.5-flash-preview-tts`）を選択する
   1. *Tier*欄で、契約している料金プランの階層を設定する
1. *ファイル(F)*→*キャラクターの編集*からキャラクター編集ウィンドウを開く
1. *ボイス*→*声質*欄で、Gemini TTSの音声（Zephyr, Puck, Kore など）を選択する
1. キャラクターを選択後、*ここに台詞を入力*欄にセリフを入力し、*追加*ボタンをクリックする

## パラメータ
- **モデル（設定）**  
  使用する音声合成モデルを指定します。  
  利用可能なモデルや品質・料金は[Gemini APIの料金ページ](https://ai.google.dev/gemini-api/docs/pricing)を参照してください。
- **Tier（設定）**  
  契約プランに応じたレート制限の階層を指定します（0: Free, 1〜3: 有料プラン）。  
  値が大きいほど1分あたりに送信できるリクエスト数が増えます。
- **読み上げ指示（Prompt）**  
  話し方の指示を自由記述で指定できます。  
  例: `楽しそうに話して`、`落ち着いた口調で`

## 利用条件等
- [Gemini API 利用規約](https://ai.google.dev/gemini-api/terms)
- [Google API 利用規約](https://developers.google.com/terms)

## 関連リンク
- [Google AI Studio](https://aistudio.google.com/)
- [Gemini API 音声生成ドキュメント](https://ai.google.dev/gemini-api/docs/speech-generation)
- [利用可能な音声一覧](https://ai.google.dev/gemini-api/docs/speech-generation#voices)
