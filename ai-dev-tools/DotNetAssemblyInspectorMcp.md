---
title: DotNetAssemblyInspectorMcp
date: 2026-06-26
tags: [AI開発ツール]
description: .NETアセンブリ(.dll/.exe)をリフレクションで解析しMCPツールとしてLLMに提供するMCPサーバー
---
## 概要
.NET アセンブリ（`.dll` / `.exe`）を `MetadataLoadContext` で読み取り専用に解析し、その結果を Model Context Protocol (MCP) ツールとして LLM クライアントへ提供する stdio ベースの MCP サーバーです。  
ソースコードが無いサードパーティ製アセンブリでも、型やメンバーの情報を LLM から直接問い合わせられます。

## 特徴
- **メタデータ専用ロード** — `MetadataLoadContext` を使用した読み取り専用解析。対象コードは実行されません。
- **自動依存解決** — .NET ランタイムと同一フォルダの自動プローブに対応。
- **構造化エラー返却** — 依存解決に失敗した場合、原因の推測を含む JSON 形式で返します。

## 提供ツール一覧
|ツール|説明|
|:--|:--|
|`list_types`|アセンブリ内の型を列挙する|
|`get_type`|単一の型の詳細を取得する|
|`list_members`|メンバーを列挙する|
|`get_method_signature`|メソッドの完全なシグネチャ詳細を取得する|
|`get_xml_doc`|XML ドキュメントコメントを取得する|
|`get_assembly_info`|アセンブリの識別情報を取得する|
|`search_members`|正規表現でメンバーを横断検索する|
|`list_extension_methods`|拡張メソッドを列挙する|

## 必要要件
- .NET 10 SDK

## ビルド方法
```powershell
pwsh -File .\build.ps1                       # Release ビルド
pwsh -File .\build.ps1 -Configuration Debug  # Debug ビルド
```

## MCP設定例
```json
{
  "mcpServers": {
    "dotnet-inspector": {
      "command": "C:\\path\\to\\DotNetAssemblyInspectorMcp\\bin\\Release\\net10.0\\DotNetAssemblyInspectorMcp.exe"
    }
  }
}
```

## ライセンス
MIT License

## ソースコード
- [manju-summoner / DotNetAssemblyInspectorMcp](https://github.com/manju-summoner/DotNetAssemblyInspectorMcp)
