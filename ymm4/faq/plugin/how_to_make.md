---
title: プラグインを作成する
date: 2023-09-01
tags: [YMM4]
---
## YMM4にプラグインを作成する
1. [VisualStudio](https://visualstudio.microsoft.com/ja/)をインストールする
1. .NET7のクラスライブラリプロジェクトを作成する
1. プロジェクトの作成後、プロジェクトファイルの`<TargetFramework>`を`net7.0-windows10.0.19041.0`に変更し、その下に`<UseWPF>true</UseWPF>`を追加する
```xml
<PropertyGroup>
    <TargetFramework>net7.0-windows10.0.19041.0</TargetFramework>
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

## 作成したプラグインを読み込む
1. プラグインをビルドする
1. ビルドフォルダ内の`プラグイン名.dll`をYMM4のプラグインフォルダに配置する  
   ※ YMM4フォルダ内に存在しないdllを参照している場合、そのdllもコピーしてください。
- 参考: [プラグインを使用する](./how_to_use.md)

## プラグインのサンプル
- [サンプルプラグイン集](https://github.com/manju-summoner/YukkuriMovieMaker4PluginSamples)