---
lang: ja-JP
layout: wiki
section: twilightmenu
category: updating
title: 更新（3DS）
long_title: TWiLight Menu++を更新（3DS）
description: ニンテンドー3DSでTWiLight Menu++を更新する方法
tabs:
  - 
    universal-updater: Universal-Updater
    manual: 手動
---

v6.8.3より古いバージョンから更新する場合は、DSゲームの`.sav`ファイルを`saves`という新しいフォルダに移動し、`saves`フォルダはDS ROMと同じ場所に置いてください。
{:.alert .alert-info}

v21.0.0より古いバージョンから更新する場合は、DSiウェアタイトルの`.pub`および/または`.prv`ファイルを`saves`という新しいフォルダに移動し、`saves`フォルダはDSウェアROMと同じ場所に置いてください。
{:.alert .alert-info}

{% capture tab-universal-updater %}
1. Universal-Updaterを開く
   - お持ちでない場合は、[インストール](installing-3ds)手順に従ってください
1. アプリのグリッドで「TWiLight Menu++」を見つけます。見つからない場合は、サイドバーの3番目のダブで検索できます
1. <kbd class="face">A</kbd>を押すか、サイドバーのダウンロードアイコンをタップし、`TWiLight Menu++`を選択してインストールします
   - しばらく時間がかかります
{% endcapture %}
{% assign tab-universal-updater = tab-universal-updater | split: "////////" %}

{% capture tab-manual %}
1. 最新の[`TWiLightMenu-3DS.7z`](https://github.com/DS-Homebrew/TWiLightMenu/releases/latest/download/TWiLightMenu-3DS.7z)をダウンロード
1. `TWiLightMenu-3DS.7z`を抽出
1. `_nds`フォルダをSDカードのルートにコピー
1. `BOOT.NDS`ファイルをSDカードのルートにコピー
1. 2つの`.cia`ファイルをSDカードのルートにコピー
1. 3DSで、FBIを使って2つのCIAをインストール
{% endcapture %}
{% assign tab-manual = tab-manual | split: "////////" %}

### 更新

{% assign tabs = tab-universal-updater | concat: tab-manual %}
{% include tabs.html index=0 tabs=tabs %}

### フラッシュカード側の他の手順

TWLMenu++でSDとフラッシュカードの内容を切り替えることができ、フラッシュカードのTWLMenu++はv16.3.0以降である場合は、以下の手順に従ってください。

1. TWLMenu++の設定に行く
1. `TWiLight Menu++を更新します`を選択
1. `本体の(micro)SD > Slot-1のmicroSD`を選択
