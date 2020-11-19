---
title: 閲覧注意（NSFW）
description: 閲覧注意とは、ドライブのファイルに付けるフラグである。
published: true
date: 2020-11-19T08:30:27.921Z
tags: 
editor: markdown
dateCreated: 2020-09-20T08:02:53.535Z
---

**閲覧注意**または**NSFW**（Not safe for work）とは、[ドライブ](/function/drive)のファイルに付けるフラグである。

他のユーザーのために、職場や公共の場で閲覧するのに適切でないと思われるファイルにはこのフラグをつけるべきである。[Misskey](/software/misskey)では、[モデレーター](/function/moderator)がこのフラグを付ける場合もある。

ファイルに閲覧注意が設定されていると、以下の画像のようにファイルが表示されるべき部分に「閲覧注意」と書かれた黒い覆いが表示され、不適切なファイルが突然表示されることを防ぐ。クリックまたはタップするとファイルが表示される。

![](https://pd2.arkjp.net/misskey/drive/1f1bd999-6d46-4896-9a62-f68360f6acc4.png)

閲覧注意の変更はリモートには伝達されず、投稿が送信されたときの設定で固定される。

# 設定・解除方法
- ドライブを開き、ファイルのメニュー（デスクトップ: 右クリック、モバイル: ファイル詳細画面）から
- 投稿画面での添付ファイルをクリックしメニューを表示

# ソフトウェア間の差異
Misskeyでは、ドライブ機能を有効に利用するため閲覧注意をファイルごとに設定できる。さらに、アップロード後に閲覧注意を切り替えることができる。
[Mastodon](/software/mastodon)では、投稿ごとにしか閲覧注意を設定できず、後から変更することはできない。

このため、MisskeyからMastodonに情報が伝達する際、複数のファイルが添付されていた場合1つでも閲覧注意が設定されているとすべてのファイルが閲覧注意と伝わる（Misskey同士なら問題ない）。