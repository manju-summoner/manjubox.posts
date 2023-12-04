---
title: YMM v4.22以前に作成したプラグインがv4.23以降でビルドできない
date: 2023-12-04
tags: [YMM4]
---
## 背景
ゆっくりMovieMaker v4.23.0.0で.NET7から.NET8に移行したた関係で、v4.22.x.x以前に作成されたプロジェクトファイルをv4.23.0.0以降でビルドすると、以下のようなエラーが表示されビルドできなくなっています。
```
CS1705 アセンブリ'YukkuriMovieMaker.Plugin' (...)は、参照されているアセンブリ '...'より新しいバージョンを含む'...'を使用します
MSB3277 "..." の異なるバージョン間で、解決できない競合が見つかりました。
```
以前にビルドしたdllは引き続きYMM v4.23.0.0以降でも使用できますが、再ビルドを行う場合はプロジェクトファイルをYMM v4.23以降用に編集する必要があります。

## 移行手順
以下の手順を実行し、プロジェクトファイルをYMM v4.23.0.0以降用に編集する必要があります。

1. プロジェクトファイルをダブルクリックまたは`右クリック`→`プロジェクト ファイルを編集`
1. `<TargetFramework>`を`net8.0-windows10.0.19041.0`に変更
1. `ビルド(B)`→`ソリューションのクリーン(C)`を実行

```
<PropertyGroup>
    　　　　　  <!-- ↓ここをnet7.0からnet8.0に変更 -->
    <TargetFramework>net8.0-windows10.0.19041.0</TargetFramework>
    <UseWPF>true</UseWPF>

    ...省略...

</PropertyGroup>
```

## 関連文書
- [ゆっくりMovieMaker v4.22.x.x以前に作成されたプロジェクトファイルの移行手順](https://github.com/manju-summoner/YukkuriMovieMaker4PluginSamples/blob/master/Migration.md)