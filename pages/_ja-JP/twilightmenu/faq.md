---
lang: ja-JP
layout: faq
section: twilightmenu
category: other
title: よくある質問とトラブルシューティング
long_title: TWiLight Menu++のよくある質問とトラブルシューテイング
description: TWiLight Menu++のよくある質問とトラブルシューティング
---

もっとよくある質問ため、[GBAtempスレッド](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/)にアクセスしてください。
{:.alert .alert-info}

#### TWiLight Menu++を起動する時に、3DSが黒い画面で動かなく、クラッシュする、電源を切るなどのはなぜですか？
TWL_FIRMは何らかの方法で破損している可能性があります。 このガイドに従って問題を解決してください：[ https://3ds.hacks.guide/troubleshooting#dsi--ds-functionality-is-broken-after-completing-the-guide](https://3ds.hacks.guide/troubleshooting#dsi--ds-functionality-is-broken-after-completing-the-guide)

#### TWiLight Menu++を起動する時に、白い画面が表示されるを修正するにはどうすればいいですか？
- 本体を再起動
- それがうまくいかない場合は、SDカードを32KBクラスタ／割り当てサイズでFAT32にフォーマットしてください
- それでもうまくいかない場合は、別のSDカードをお試してください

#### Acekard・Wood UIのテーマはどこですか？
Acekard（Wood UIとも呼ばれる）のテーマは、バグの動作とSDカードの破損の原因で削除されました。 修正をお待ちください。 このテーマの返還の進行状況は、[このPR](https://github.com/DS-Homebrew/TWiLightMenu/pull/1109)にあります。

#### ゲームを起動する時に、TWiLight Menu++が再起動したりGuru Meditation Errorを与えたりを修正するにはどうすればいいですか？
TWLMenu++設定に移動し、`最近プレイしたリストを更新する`を無効にする。

#### SDカードからDSゲームを読み込みようとすると、白い画面が表示されるのはなぜですか？
nds-bootstrapの良くある質問ページの[I'm having issues with my ROM(s), what should I do?](../nds-bootstrap/faq?faq=im-having-issues-with-my-roms-what-should-i-do)を参照してください。

#### チートはどうのように使いますか？
`sd:/_nds/TWiLightMenu/extras/`フォルダ内に`usrcheat.dat`ファイルの形式でチートデータベースが必要です。 最新のチートデータベースは、[DeadSkullzJr'sのNDS(i)チートデータベース](https://gbatemp.net/threads/488711/)。
- 3DSでは、このデータベースはUniversal-Updaterアプリに「NDS(i) Cheat Databases」として利用てきます。 これにより自動的に必要な場所にインストールされます。

あるいは、[r4cce](http://hp.vector.co.jp/authors/VA013928/soft.html)を使って独自のチートデータベースを作成できます。

#### DSiテーマの上画面にカスタム画像を表示するにはどうすればいいですか？
`sd:/_nds/TWiLightMenu/dsimenu/photos/`内のランダムな`.png`画像はメニューが読み込まれるたびに表示されます。 該当する画像がない場合は、代わりにnds-bootstrapで撮影されたスクリーンショットが使用されます。

- 画像は208x156以下である必要があります
- エラーがある場合は、画像サイズのエラーの可能性が最も高いです。 サイズを小さくするには、[tinypng](https://tinypng.com)を使ってください

#### ゲームを入手するにはどうすればよいですか？
[Universal-DB](https://db.universal-team.net/ds)と[GameBrew](https://www.gamebrew.org/wiki/List_of_all_DS_homebrew#Games)から自作ゲームをダウンロードできます。 小売ゲームのダンプを取得するには：
- DSでは、[GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases)を使ってGBAゲームをダンプでき、Slot-2フラッシュカートを持っている場合はDSゲームをダンプできます。 Slot-1フラッシュカードのみを持っていてDSゲームをダンプしたい場合は、 [Wooddumper](https://digiex.net/attachments/wooddumper_r89-zip.14735/)を使用できます。DSと互換性のあるWi-Fi接続とROMを受信する別のデバイスのFTPクライアントが必要です。
- DSiでは、[GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases)を使ってDSゲームとDSiウェアをダンプできます
- 3DSでは、[GodMode9](https://github.com/d0k3/GodMode9/releases)を使ってDSゲーム、DSiウェア、バーチァルコンソールのゲームをダンプできます

#### ゲームカードからSDカードにセーブファイルを取得するまたは逆にことはできますか？
はい、DSiと3DSで[GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases)、3DSで[Checkpoint](https://github.com/FlagBrew/Checkpoint/releases)を使えます

#### TWiLight Menu++の言語を変更するにはどうしたらよいですか？
1. TWiLight Menu++設定を開きます。これを行うには、TWiLight Menu++を読み込んでいる間に<kbd>SELECT</kbd>を押し続けます
1. <kbd class="l">L</kbd>または<kbd class="face">Y</kbd>を1回（フラッシュカード・3DS上）または2回（DSi上）を押します
1. 言語が表示されるまで最初のオプションを変更し、設定を終了します
   - DSゲームの言語とTWiLight Menu++にそれのタイトルを制御するため、次の2つのオプションを変更することもできます

#### これはDS(i)エミュレータですか？
いいえ、これはエミュレータではありません。 メニューとDSゲーム（nds-bootstrapを介して読み取り）は、本体のDS・DSiモードでネイティブに実行されます。 唯一のエミュレートされる本体は、過去の本体です。しかし、GBAは部分的です（グラフィクスのようないくつかの部分はネイティブに実行されている）

#### TWiLight Menu++はどのシステムに対応ですか？
[TWiLight Menu++で対応されているシステムのリスト](../ds-index/emulators#twilight-menuで対応されているシステムのリスト)を参照してください。

#### Slot-1ゲームのエクスプロイトでTWiLight Menu++を起動できますか？
いいえ。 DSiウェアではないため、Slot-1カードを使用する場合はSDアクセスができません。

#### ゲームを見つける・見ることができないのはなぜですか？
見つからないことができない複数の理由があります。
- ゲームを`_nds`フォルダに配置した場合、TWiLight Menu++では永久に見えないためアクセスできません。 SDカード上の任意な他の場所に移動してください
- フォルダ内に39個以上のアイテムがあり、メニュー上のスロットがすべて取られている場合は、ゲームは次のページにある可能性があります。 <kbd class="l">L</kbd>・<kbd class="r">R</kbd>または<kbd>SELECT</kbd>+<kbd>左</kbd>・<kbd>右</kbd>を使ってページを切り替える
- ゲームやフォルダが隠されている場合は、TWiLight Menu++のGUI設定から「隠しファイルの表示」をオンにする必要があります
- エミュレーション/HB設定でゲームタイプを非表示に設定すると、メニューには表示されません。 これらの設定を変更して表示します
- ゲームがアーカイブ（`ZIP`、`RAR`、`7Z`など）にある場合は、TWiLight Menu++では使用できません。 アーカイブからゲームを解凍して使用します
- ゲームが[対応されている拡張子](../ds-index/emulators#list-of-systems-supported-by-twilight-menu)のにずれかを使わない場合は、ファイルの名前を変更して拡張子を変更する必要があります

#### TWiLight Menu++設定にアクセスするにはどうすればいいですか？
TWiLight Menu++設定にアクセスする方法は、設定によって異なります。
- **DSクラシックメニュー：**下画面の下のDSアイコンをタップします
- **ニンテンドーDSi/セガサターン/Homebrew Launcherのテーマ：SELECTメニューを使う：**<kbd>SELECT</kbd>を押して設定アプレットを起動します（D-PADを使ってオプションをハイライトします）
- **SELECTメニューを使わないニンテンドーDSi/セガサターン/Homebrew Launcherのテーマ：**<kbd>SELECT</kbd>を押してDSクラシックメニューになります
- **ニンテンドー3DSのテーマ：**下画面の左上のスパナのアイコンをタップします
- **R4オリジナルテーマ：**<kbd>START</kbd>（ファイルブラウザにいている）を押し、<kbd>SELECT</kbd>を押します

また、TWiLight Menu++を起動する時に<kbd>SELECT</kbd>を押して、設定に直接アクセスすることができます。
