# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

トイプードル「ころも」のSNSリンクハブページ。GitHub Pages でホスティングする静的HTML。
TikTokからYouTubeへの導線が主な目的。

## 技術スタック

- 静的HTML / CSS / 最小限のJS（ビルドツール・npmなし）
- 外部ライブラリはCDN経由のみ
- ホスティング：GitHub Pages（`miriwo0104/toyp-koromo-hub`）

## ファイル構成

- `design-a.html`：ふんわり可愛い系（パステルカラー）
- `design-b.html`：シンプルモダン系（ホワイト基調）
- `design-c.html`：ナチュラル系（アースカラー）
- デザイン確定後、採用ファイルを `index.html` にリネームして公開

## アカウント管理

| サービス | 使用アカウント |
|---|---|
| GitHub | エンジニア個人アカウント（miriwo0104） |
| Cloudflare | エンジニア個人アカウント（ドメイン取得・DNS管理） |
| Google Analytics（GA4） | ころも用Googleアカウント（測定ID: G-RHJBLSEVLV） |

## 今後のTODO

- [ ] デザイン（A/B/C）を奥さんと選ぶ
- [ ] ドメイン取得（Cloudflare Registrar、`toyp-koromo.com` 候補）
- [ ] CNAME設定 + GitHub Pages カスタムドメイン設定
