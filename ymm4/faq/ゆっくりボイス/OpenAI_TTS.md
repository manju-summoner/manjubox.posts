---
title: OpenAI TTSの音声を利用する
date: 2023-11-18
tags: [YMM4]
keywords: [OpenAI]
---
## OpenAI Text-to-Speechとは
OpenAI TTSは、OpenAI社が提供する音声合成サービスです。  
外部連携APIを使用し、YMM4から直接音声を生成できます。  
利用には別途APIキーの取得が必要です。  
- [OpenAIダッシュボード](https://platform.openai.com/)

## 利用方法
1. [OpenAIダッシュボード](https://platform.openai.com/)を開き、APIキーを取得する
   1. OpenAIのアカウントを作成する
   1. [API Keys](https://platform.openai.com/api-keys)をクリックする
   ![スクリーンショット](OpenAI_TTS_1616.png)
   1. `Create new secret key`をクリックする
   ![スクリーンショット](OpenAI_TTS_0125.png)
   1. 任意の名前を入力し、`Create secret key`をクリックする
   ![スクリーンショット](OpenAI_TTS_0208.png)
   1. API Keyをコピーする
   ![スクリーンショット](OpenAI_TTS_0215.png)
1. ゆっくりMovieMakerを起動し、`ファイル(F)`→`設定`→`音声合成`→`OpenAI Text-to-Speech`を開く
1. `APIキー`に、取得したAPIキーを設定する
![スクリーンショット](OpenAI_TTS_0544.png)
1. タイムライン左下のボタンをクリックし、キャラクター設定ウィンドウを開く
![スクリーンショット](OpenAI_TTS_0900.png)
1. `声質`からOpenAIのキャラクターを選択する
![スクリーンショット](OpenAI_TTS_0807.png)

## 利用条件等
- [Usage policies](https://openai.com/policies/usage-policies)