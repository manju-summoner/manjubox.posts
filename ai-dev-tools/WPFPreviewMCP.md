---
title: WPFPreviewMCP
date: 2026-06-26
tags: [AI開発ツール]
description: WPFデスクトップアプリの画面観察・操作をLLMから行えるようにするMCPサーバー
---
## 概要
Claude Code の Web 版 Preview（ブラウザの観察・操作 MCP）を、WPF デスクトップアプリ向けに汎用再現する MCP サーバーです。  
WPF には Chrome DevTools Protocol に相当する観察レイヤーが無いため、対象プロセス内にエージェントを注入し、Visual Tree・DependencyProperty・スクリーンショット・ログなどへアクセスします。

## 特徴
- **ソース改変不要** — `DOTNET_STARTUP_HOOKS` でエージェントを注入します（.NET 5+ の WPF アプリが対象）。
- **インプロセス** — DependencyProperty の実効値やバインディング情報の取得、任意の C# コード実行が可能です。
- **100% C#/.NET 10** — MCP サーバー・エージェント・サンプルアプリすべて .NET で実装されています。

## 動作環境
- Windows OS（WPF 依存）
- .NET 10 SDK
- .NET 5 以降の WPF デスクトップアプリ

## 提供ツール一覧
|ツール|説明|
|:--|:--|
|`preview_start`|exe をエージェント注入付きで起動する|
|`preview_list`|稼働中のアプリ一覧を表示する|
|`preview_snapshot`|Visual Tree のスナップショットを取得する|
|`preview_screenshot`|ウィンドウを PNG でキャプチャする|
|`preview_inspect`|DependencyProperty の実効値・バインディングを確認する|
|`preview_click`|UI 要素をクリック操作する|
|`preview_fill`|TextBox 等へ値を設定する|
|`preview_eval`|プロセス内で C# 式を評価する|
|`preview_console_logs`|ログ・例外情報を取得する|

## セキュリティ
- HTTP は 127.0.0.1 ループバック限定＋ランダムポート。
- 起動時にセッショントークンを生成。
- CSRF 対策として、不正な Origin/Referer 付きリクエストは 403 で拒否。

## 必要要件
- .NET 10 SDK

## MCP設定例
`.mcp.json` または `~/.claude.json` に以下を追加します。

```json
{
  "mcpServers": {
    "wpf-preview": {
      "command": "dotnet",
      "args": ["<リポジトリパス>\\src\\WpfPreview.Mcp\\bin\\Debug\\net10.0\\wpfpreview-mcp.dll"],
      "env": {
        "WPFPREVIEW_AGENT_DLL": "<リポジトリパス>\\src\\WpfPreview.Agent\\bin\\Debug\\net10.0-windows\\WpfPreview.Agent.dll"
      }
    }
  }
}
```

## ライセンス
MIT License

## ソースコード
- [manju-summoner / WPFPreviewMCP](https://github.com/manju-summoner/WPFPreviewMCP)
