---
title: プラグインを作成する
date: 2023-09-01
tags: [YMM4]
---
> **Warning**
> こちらはプラグインの作成方法を解説しているページです。  
> 配布されているプラグインをYMM4に追加する方法は[プラグインを使用する](./how_to_use.md)をご確認ください。

## プラグインのサンプル
- [サンプルプラグイン集](https://github.com/manju-summoner/YukkuriMovieMaker4PluginSamples)

## YMM4にプラグインを作成する
1. [VisualStudio](https://visualstudio.microsoft.com/ja/)をインストールする
1. .NET10のクラスライブラリプロジェクトを作成する
1. プロジェクトの作成後、プロジェクトファイルの`<TargetFramework>`を`net10.0-windows10.0.19041.0`に変更し、その下に`<UseWPF>true</UseWPF>`を追加する
```xml
<PropertyGroup>
    <TargetFramework>net10.0-windows10.0.19041.0</TargetFramework>
    <UseWPF>true</UseWPF>

    ...省略...

</PropertyGroup>
```

## プロジェクト参照を追加する
1. ソリューションエクスプローラーから`依存関係`を右クリックし、`プロジェクト参照の追加(R)`をクリックする。
1. 参照マネージャーウィンドウ下部の`参照(B)`ボタンをクリックする。
1. YMM4をインストールしているフォルダ内にある`YukkuriMovieMaker.Plugin.dll`と`YukkuriMovieMaker.Controls.dll`を選択し、OKボタンをクリックする。
1. `OK`ボタンをクリックし、参照マネージャーを閉じます。
1. プラグインの実装中に`CS0012: 型'T' は、参照されていないアセンブリに定義されています。アセンブリ 'アセンブリ名, Version=x.x.x.x, Culture=xxx, PublicKeyToken=xxx' に参照を追加する必要があります。`とエラーが表示された場合、必要に応じてYMM4フォルダ内にある`アセンブリ名.dll`を参照に追加してください。
1. 作成するプラグインに応じて必要なクラスを実装する

## 開発者モードを有効にする（v4.33.0.0以降）
YMM4の開発者モードを有効にすると、未解放のDirectXオブジェクトを検出可能になります。
1. YMM4を起動する
1. `設定`→`開発者モード`→`開発者モードを有効にする（要再起動）`を有効にする
1. YMM4を終了する

## 作成したプラグインを読み込む
1. プラグインをビルドする
1. ビルドフォルダ内の`プラグイン名.dll`をYMM4のプラグインフォルダに配置する  
   ※ YMM4フォルダ内に存在しないdllを参照している場合、そのdllもコピーしてください。
- 参考: [プラグインを使用する](./how_to_use.md)

## プラグインの配布用パッケージ化
プラグインを`.ymme`形式で配布することにより、ワンクリックでプラグインをインストールできるようになります。
1. 作成したプラグインをzipで圧縮する
1. zipファイルの拡張子を`.ymme`に変更する
1. `.ymme`ファイルを配布する

## リポジトリのトピック
プラグインをGitHubで公開する場合、検索性向上のためリポジトリの[Topics欄](https://docs.github.com/ja/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)に以下のトピックを設定することを推奨します。

| 種類 | トピック |
| --- | --- |
| 共通 | [ymm4-plugin](https://github.com/topics/ymm4-plugin) |
| 音声読み込みプラグイン | [ymm4-audio-source](https://github.com/topics/ymm4-audio-source) |
| 映像読み込みプラグイン | [ymm4-video-source](https://github.com/topics/ymm4-video-source) |
| 画像読み込みプラグイン | [ymm4-image-source](https://github.com/topics/ymm4-image-source) |
| 立ち絵プラグイン | [ymm4-tachie](https://github.com/topics/ymm4-tachie) |
| 動画出力プラグイン | [ymm4-video-writer](https://github.com/topics/ymm4-video-writer) |
| 音声エフェクト | [ymm4-audio-effect](https://github.com/topics/ymm4-audio-effect) |
| 映像エフェクト | [ymm4-video-effect](https://github.com/topics/ymm4-video-effect) |
| 音声合成プラグイン | [ymm4-voice](https://github.com/topics/ymm4-voice) |
| AIテキスト補完プラグイン | [ymm4-text-completion](https://github.com/topics/ymm4-text-completion) |