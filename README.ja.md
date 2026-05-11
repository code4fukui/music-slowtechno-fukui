# SlowTechno FUKUI

福井をテーマにしたAI生成のスローテクノ音楽を収録したオープンデータプロジェクトです。楽曲は[Suno](https://suno.com/)を使用して作成されました。

このリポジトリでは、生成された音楽をオープンデータとして提供するほか、Webベースのプレイヤーと、Sunoのプレイリストをダウンロードしてアーカイブするためのスクリプトを提供しています。

## 視聴

- **[インタラクティブWebプレイヤー (GitHub Pages)](https://code4fukui.github.io/music-slowtechno-fukui/)**
- **[Sunoのオリジナルプレイリスト](https://suno.com/playlist/1f0f31ae-87b3-438a-ac53-240320b1477e)**

Webプレイヤーでは、トラックリスト、アルバムアート、歌詞、および生成に使用されたプロンプトを表示できます。

## 音楽について

各楽曲は福井の文化からインスピレーションを得ています。例えば、「ソースカツドンの街」という曲は、以下のプロンプトから生成されました。

> フクイといえばソースカツドン,slow techno

Sunoのモデルは、楽曲のスタイルについて以下のような詳細な説明を生成しました。
> 抑え気味の4つ打ちのパルス、ドライなキックとソフトなクラップが落ち着いたグルーヴを刻むスローテクノ。Aメロはつぶやくような日本語のリードボーカル、短いベースのパルス、フィルターのかかったベルの刻みで音数を少なく保ち、Bメロは上昇するノイズとエコーの余韻とともに展開し、サビはレイヤーされたユニゾンのダブルとチャントのようなバッキングの繰り返しによって、より広がりのあるサウンドに着地する。

## データ

このリポジトリには以下が含まれます:
- `audio/`: 各トラックのMP3音声ファイル。
- `image/` & `image_large/`: 各トラックのジャケットアート。
- `playlist.json`: 歌詞や生成メタデータを含む完全なプレイリストデータ（ローカルファイルパス付き）。
- `playlist_org.json`: Sunoから取得したオリジナルプレイリストデータ（リモートURL付き）。

## 使い方: Sunoプレイリストのダウンロード

提供されているDenoスクリプトを使用すると、公開されている任意のSunoプレイリストとそのアセット（音声、画像）をローカルにダウンロードできます。

```sh
deno run -A https://code4fukui.github.io/music-opendata-fukui/download.js https://suno.com/playlist/YOUR_PLAYLIST_URL
```
*このリポジトリのプレイリストを使用した例:*
```sh
deno run -A https://code4fukui.github.io/music-opendata-fukui/download.js https://suno.com/playlist/1f0f31ae-87b3-438a-ac53-240320b1477e
```

## クレジット
- 楽曲生成: [Suno](https://suno.com/)
- Webプレイヤーのソースコード: [music-handaduke](https://github.com/code4fukui/music-handaduke/)

## ライセンス
このプロジェクトはオープンデータとして提供されています。
