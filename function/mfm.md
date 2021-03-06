---
title: Misskey Flavored Markdown
description: Misskeyで使えるMarkdown風の構文
published: true
date: 2021-02-08T07:52:25.969Z
tags: 
editor: markdown
dateCreated: 2020-09-20T08:21:41.404Z
---

**Misskey Flavored Markdown**または**MFM**とは、Misskey内の様々な場所で使用できる専用のマークアップ言語だ。ここでは、Misskeyで使用可能なMFM構文の一覧が確認できる。

# MFMが適用される部分
- [ノート](/function/note)
> ノートメニューで`内容をコピー`すると元のテキストがクリップボードにコピーされるため、メモ帳等にペーストすることでどのようなMFMが使われているかが確認できる。
{.is-info}
- [プロフィールの自己紹介](/function/user_profile)
- [トーク](/function/messaging)のメッセージ
- [ページ](/function/page)
- [インスタンス](/instances)の説明文やお知らせなど
> MFMはMisskeyサーバ同士であれば他のサーバでも表示されるが、ActivityPub対応の他のSNSサービスで装飾等が全て表示されるとは限らない。
{.is-warning}

# 基本的なMFM
実はこのMFM、メンションやハッシュタグといったMisskeyの身近なところでも使われている。
## メンション
アットマーク`@` + ユーザー名で、特定のユーザーにメンションを送ることができる。
![mention.png](/ja_jp/mfm/mention.png)
```
@ai
```

## ハッシュタグ
ナンバーサイン`#` + タグ名で、ハッシュタグを付けることができる。
![ss_hashtag.png](/ja_jp/mfm/ss_hashtag.png)
```
#Misskey自己紹介部
```
> アットマーク`@`やナンバーサイン`#`の後に文字を入力すると候補リストが出現する。 このリストは文字を入力していくにつれて絞り込まれていくので、もし探しているユーザーやハッシュタグがリスト内に見つかったら、矢印キーやTabを使って選択し、`Enter`キーで入力を完了することもできるぞ。さすがMisskey！
{.is-info}

![ss_hashtag2.png](/ja_jp/mfm/ss_hashtag2.png)


## 文字装飾
MFMといえばこれを連想する者が多い。テキストを特定の記号や文字列で囲うことにより文章を読みやすくしたり、文脈を明確にしたりできる機能だ。

### 太字
テキストをアステリスク記号二つ`**`と`**`で囲むと、文字を**太く表示**して**強調する**ことができる。
![ss_bold.png](/ja_jp/mfm/ss_bold.png)
```
今のはメラゾーマではない、**メラ**だ…
```
　
### 斜体
テキストを`<i>`と`</i>`で囲むと、文字を *斜体* にすることができる。
![ss_italic.png](/ss_italic.png)
```
<i>Misskey</i>で<i>Fediverse</i>の世界が広がります。
```
　
### 削除線
テキストをチルダ二つ`~~`と`~~`で囲むと、~~打ち消し~~**削除線**を加えることができる。
![ss_strikethrough.png](/ja_jp/mfm/ss_strikethrough.png)
```
~~でも藍ちゃんのならちょっと見たいかも~~
```
　
### 小さい字
テキストを`<small>`と`</small>`で囲うと文字を <small>小さく</small> 表示させることができる。
![ss_small.png](/ja_jp/mfm/ss_small.png)
```
へ、編集してくれたって別にあんたのコトなんて何とも思ってないんだからね！
<small>･･････でもほんのちょっとだけ嬉しい、かも･･･</small>
```
　
### 中央寄せ
文章を`<center>`と`</center>`で囲うと中央に寄せて表示することができる。
![ss_center3.png](/ja_jp/mfm/ss_center3.png)
```
<center>殺伐としたスレにインド象が！</center>
<center>（しまうま）</center>
<center>🐶</center>
<center>「にゃーん！！」</center>
<center>　ハ　ム　ス　タ　ー　</center>
```

### 文字反転
テキストを反転させることができる。角括弧とコマンドを使用するMisskey.v12の新機能らしい。
#### 左右反転
テキストを`[flip.h ` と`]`で囲うことによって左右反転表示させることができる。
ちなみにこの`.h`は "horizontal(ly)"（水平方向に）の略字である。
![ss_flip.png](/ja_jp/mfm/ss_flip.png)
```
牛耕式（ぎゅうこうしき）とは
[flip.h 主に古代ギリシアなどでの写本]
や銘文に用いられた書記方式の
[flip.h 一種である。　　　　　　　　]

ギリシア語ではβουστροφηδόν
[flip.h （ボウストロフェードン）と　　]
　　呼ばれ、語源は："βοῦς"（ボウス、牛）＋
[flip.h "στροφή"（ストローフェ、引き返す）に　　　]
　　　副詞化接尾辞の "-δόν"（〜のようなさま）
[flip.h が加わり「（畑などを耕す）牛が　　　　　　]
　　　　　　引き返すさま」という意から来ている。
```
#### 上下反転
テキストを`[flip.v ` と`]`で囲うことによって上下反転表示させることができる。
ちなみにこの`.v`は "vertical(ly)"（垂直方向に）の略字である。
![ss_flip_v.png](/ja_jp/mfm/ss_flip_v.png)
```
水面を　反射するのが　ヴァーティカル。
[flip.v 水面を　反射するのが　ヴァーティカル。]
```
#### 上下左右反転（180度回転）
テキストを`[flip.h,v ` と`]`で囲うことによって上下左右反転表示（180度回転）させることができる。
![ss_fliphv.png](/ja_jp/mfm/ss_fliphv.png)
```
かの有名なラパ・ヌイの
[flip.h,v 未解読古代文字「ロンゴ]
ロンゴ」はなんと逆牛耕
[flip.h,v 式（リバース・ブストロ]
フェドン）で書かれている。
```
> もし`[flip`の後に続く`.h`や`.v`を省略した場合は自動的に左右反転（`.h`）扱いとなる。
{.is-info}

![ss_flip_ex.png](/ja_jp/mfm/ss_flip_ex.png)
```
[flip 救急車(AMBULANCE) ]
```

## テキストの引用
行頭に`> `を付けると内容が引用であることを示すことができる。
![ss_quote.png](/ja_jp/mfm/ss_quote.png)
```
> シャミ子が悪いんだよ
↑言ってない
```
また、`>> `で二重引用を示すこともできる。
![ss_doublequote.png](/ja_jp/mfm/ss_doublequote.png)
```
>> シャミ子が悪いんだよ
> ↑言ってない
たまたまそういうとこが描かれてないだけで普通に言ってるんだよなぁ
```

# 高度なMFM
高度と言っても内部処理が高度なだけで、構文自体は非常に書きやすい親切設計となっている。
## 検索窓
文末に`検索`の一言を添えるだけで入力済みの検索ボックスを表示させることができる。
> 検索窓召喚の文字列は`検索`のほかにも`[検索]`、`Search`、`[Search]`などがある。いずれも文末に置くだけで等しく効果を発揮するぞ。
{.is-info}

![ss_search.png](/ja_jp/mfm/ss_search.png)
```
藍ちゃん　戦闘レベル　検索

AiScript とは [検索]

Is Misskey Mastodon? Search

What is a Miskist? [Search]
```

## URL
URLを貼ると自動的にリンク付けされる。
![ss_link.png](/ja_jp/mfm/ss_link.png)
```
https://misskey.io/mfm-cheat-sheet
```
　
## リンク
リンクにしたいテキストを角括弧`[` `]`で囲い、そのすぐ隣に丸括弧`(` `)`で囲んだURLを書き足すことにより、角括弧内の文を丸括弧内のURLに紐づけることが出来る。
![ss_link2.png](/ja_jp/mfm/ss_link2.png)
```
[省略しています。全て読むにはこのリンクをクリック！](https://dic.nicovideo.jp/a/%E5%85%A8%E3%81%A6%E8%AA%AD%E3%82%80%E3%81%AB%E3%81%AF%E3%81%93%E3%81%AE%E3%83%AA%E3%83%B3%E3%82%AF%E3%82%92%E3%82%AF%E3%83%AA%E3%83%83%E3%82%AF%21)
```

> 角括弧の手前に疑問符`?`を追加するとリンクカードを隠すことができる。一つのノート内に非常な多くのリンクを書く時やネタバレ防止機能としては重宝すると同時に、リンク先の内容を隠蔽する目的で使うこともできる。Misskeyに限った話ではないが、ネットで見かける「いますぐアクセス！」などと書かれたあやしいリンクには要注意だ！
{.is-info}

![ss_link3_edited.png](/ja_jp/mfm/ss_link3_edited.png)
```
【Pleromaへいますぐアクセス！】
ツイッターのリンクはこちら！！
→　?[mstdn.jp](https://misskey.io)
```
　
## カスタム絵文字
コロン`:` `:`でカスタム絵文字名を囲むと、カスタム絵文字を表示させることができる。
![ss_customemoji.png](/ja_jp/mfm/ss_customemoji.png)
```
:ai_icon:
```
> カスタム絵文字はメンションやハッシュタグのように、コロン`:`を打ち込んだ瞬間、候補リストが出現し、文字を入力するにつれだんだんと候補が絞り込まれていく仕組みだ！もちろん、お目当ての絵文字がリスト内に表示されたらそれを選ぶと入力を確定できるから大変便利だ。すごいぞMisskey！!
{.is-info}

![ss_customemoji_list.png](/ja_jp/mfm/ss_customemoji_list.png)

　
## インラインコード
プログラムなどのコードを行内（インライン）でグレイヴアクセント`` ` ``と`` ` ``に囲んであげるとシンタックスハイライトしてくれる。
![ss_inlinecode.png](/ja_jp/mfm/ss_inlinecode.png)
```
`　<:"Hello, AiScript!"　`
```
　
## ブロックコード
複数行のコード等をシンタックスハイライトしたい場合、三連グレイヴアクセント` ``` `と` ``` `で囲むとコードブロックを作成することができる。どうやら[Prism.js](https://prismjs.com/)を使用しているらしく<small>[要検証]</small> 、もしそうであればなんと**236言語**のシンタックスハイライティングに対応していることとなる。ヤバいぞMisskey！
![ss_blockcode.png](/ja_jp/mfm/ss_blockcode.png)
``````
```
~ (#i, 100) {
	<: ? ((i % 15) = 0) "FizzBuzz"
		.? ((i % 3) = 0) "Fizz"
		.? ((i % 5) = 0) "Buzz"
		. i
}
```
``````

> インラインコードやブロックコード内の文章はMFMが適用されず、（ほぼ）何を書いてもそのまま反映されるので、特殊な構文とかの引用のほか、アスキーアートなどにも使えるかもしれない…！
{.is-info}

![ss_blockcode_ai.png](/ja_jp/mfm/ss_blockcode_ai.png)

# アニメーション
MFM最大の特徴と言っても過言ではないのがこのアニメーションだ。Misskey.v12で使えるようになった角括弧とコマンドの組み合わせでなんとノート内のテキストを動かすことができる機能だ！書き方は全アニメーションに共通し 簡潔かつ規則的だが、中にはカンマ`,`の使用によってパラメータの設定をできるようなものもある。簡単なのに奧深い…それがMFMアニメーションだっ。


## びよんびよん（ゼリー）
テキストを`[jelly`と`]`で囲うと、ゼリーのような『びよんびよん』アニメーションを加えることができる。
![ss_jelly.gif](/ja_jp/mfm/ss_jelly.gif)
```
[jelly ﾌﾟﾙﾌﾟﾙ]
　[jelly 🍮]
```

## ジャーン（ファンファーレ）
テキストを`[tada`と`]`で囲うと、なんかすごい『ジャーン！』みたいなアニメーションを加えることができる。
![ss_tada3.gif](/ja_jp/mfm/ss_tada3.gif)
```
[tada \ﾍｲﾗｯｼｬｲ/]
[tada SUSHI][tada 🍣][tada 食べたい][tada 🙏] [tada この世][tada 🌏]の[tada 終わり][tada 👋]の[tada 日]は [tada SUSHI][tada 🍣][tada 食べたい][tada 🙏] [tada 最後][tada 💥💣]の[tada 晩餐][tada 🍴]に[tada 😇][tada SUSHI][tada 🍣][tada 食べたい][tada 🙏] [tada 特別][tada 🎂🎉🏆💏]な[tada あの日][tada 📆]には [tada SUSHI][tada 🍣][tada 食べたい][tada 🙏🙏] [tada トロ🐟][tada タコ🐙][tada ウニ✳︎][tada いくら💰] [tada 🔊][tada ﾃｰﾚｰﾚｰ↑][tada (セ〜〜〜ル)][tada (都会のオアスシ)]
```


## ジャンプ

```
[jump ]
```

## バウンス
テキストを`[bounce`と`]`で囲うことで、ボールのような『ぽよんぽよん』アニメーション加えることができる。
![ss_bounce.gif](/ja_jp/mfm/ss_bounce.gif)
```
[bounce 🏈]　[bounce 🏀]　[bounce 🤢]　[bounce ⚾]　[bounce 🧶]
```


## ぶるぶる（シェイク）
テキストを`[shake`と`]`で囲うと、その場で震える『ぶるぶる』アニメーションを加えることができる。
![ss_shake.gif](/ja_jp/mfm/ss_shake.gif)
```
[shake 🥶]「寒すぎてサムになったわ」
```
 ---
> 長い文字列を一緒くたにしちゃうと中心を起点としてアニメーション化されてしまう。
{.is-warning}

🍮🍮🍮🍮🍮🍮🍮🍮
```
[jelly 🍮🍮🍮🍮🍮🍮🍮🍮]
```
> そういうときは個別に書くと、意外と思ったような動きになるかもしれない。
{.is-success}

🍮🍮🍮🍮🍮🍮🍮🍮
```
[jelly 🍮][jelly 🍮][jelly 🍮][jelly 🍮][jelly 🍮][jelly 🍮][jelly 🍮][jelly 🍮]
```


## ブレ（ツイッチ）
テキストを`[twitch`と`]`で囲うと、激しい動きの『ブレ』アニメーションを加えることができる。 ~~（めっちゃ荒ぶるよｗ）~~
🕴🏡🕴🏢
```
[twitch 🕴🏡🕴🏢]
```
> 【『ブレ（ツイッチ）』と『ぶるぶる（シェイク）』の違い】
> 『ブレ』は全てのテキストが等しく動くのに対し、『ぶるぶる』は中心を起点として端っこの最も移動が多く、真ん中の移動距離が少ない動きをする。
{.is-info}

# アニメーション（回転）
回転するアニメーションを与えることができる。もっとも基本的な回転は`[spin `と`]`に囲うことで使用できるZ軸右回転だが、最新版でパラメータの指定ができるようになり、非常に高度な設定ができるようになった。

## Z軸回転
Z軸（モニターからみて中心の点）を起点に回転を行います。
### Z軸右回転（時計回り）
`[spin.z,right`と`]`で囲うと時計回りに回転します。
```
[spin.z,right 🕒🕕🕘]
```
### Z軸左回転（反時計回り）
`[spin.z,left`と`]`で囲うと反時計回りに回転します。
```
[spin.z,left 🌏🌀🌍]
```
### Z軸交互回転
`[spin.z,alternate`と`]`で囲うと時計回りと反時計回りを交互に繰り返します。
```
[spin.z,alternate 📀⚙💿]
```

## X軸回転
X軸（モニターからみて横軸）を起点に回転を行います。
### X軸右回転
`[spin.x,right`と`]`
```
[spin.x,right 🍮]
```
### X軸左回転
```
[spin.x,left 🍮]
```
### X軸交互回転
```
[spin.x,alternate 🍮]
```

## Y軸回転
Y軸（モニターからみて縦軸）を起点に回転を行います。
### Y軸右回転
```
[spin.y,right 🍮]
```
### Y軸左回転
```
[spin.y,left 🍮]
```
### Y軸交互回転
```
[spin.y,alternate ]
```
 ---
> もし`[spin`の後に続く軸指定子を省略した場合は自動的にZ軸回転（`.z`）扱いとなる。また、`,`の後に続く回転方向指定子を省略した場合は自動的に右回転（`right`）扱いとなる。
{.is-info}
```
ㅤ　[spin.z 🍮] = [spin.z,right 🍮]
　[spin.right 🍮] = [spin.z,right 🍮]
∴[spin 🍮] = [spin.z,right 🍮]
```

## 回転速度
`[spin`等の構文に`,speed=`を書き足すことで回転速度を指定することができる。
```
[spin.y,left,speed=12s 🌓　　　☀　　　🌏]
```
また、`ms`でミリ秒指定も可能。
```
[spin.y,left,speed=100ms 🌓　　　☀　　　🌏]
```
# LaTeX表現
Misskeyが最強のSNSサイトと呼ばれる理由の一つがこのLaTeXだ。
バックスラッシュと丸括弧`\(`と`\)`で囲うことにより、膨大な数のTeX関数を使うことができる。

> LaTeXは非常に多くの関数があり、ここで紹介されているものはごく一部に過ぎない。関数の完全なリストは[公式ドキュメント](https://katex.org/docs/supported.html)からチェックできる。
{.is-info}

## フォント

### サンズセリフフォント
`\sf`
### ボールドフォント
`\bf`
### イタリック
`\it`
### タイプライターテキスト
`\tt`
### ブラックボード（黒板太字）
`\Bbb`
### カリグラフィック
`\cal`
### スクリプト（数学書体）
`\mathscr{}`

## サイズ

### Huge
`\Huge`
### huge
`\huge`
### LARGE
`\LARGE`
### Large
`\Large`
### large
`\large`
### normalsize
`\normalsize`
### small
`\small`
### footsizenote
`\footsizenote`
### scriptsize
`\scriptsize`
### tiny
`\tiny`

## カラー
色はHTML標準色名を使える他、直接16進数カラーコードを指定できる。

### テキストカラー
`\textcolor{}{}`で使用できる。始めの中括弧で`{`色`}`を指定し、二番目の中括弧に`{`テキスト`}`を入れることができる。
![ss_textcolor.png](/ja_jp/mfm/ss_textcolor.png)
```
🍫\(\textcolor{chocolate}{チョコレート}\)🍫うめぇｗｗｗ
```
### カラーボックス
`\fcolorbox{}{}`で使用できる。始めの中括弧で`{`色`}`を指定し、二番目の中括弧に`{`テキスト`}`を入れることができる。
![ss_colorbox.png](/ja_jp/mfm/ss_colorbox.png)
```
\(\colorbox{yellow}{大事なことなのでハイライトしました}\)
```
#### 枠ありカラーボックス
`\fcolorbox{}{}{}`で使用できる。最初の中括弧には`{`縁の色`}`、二番目の中括弧には`{`内箱の色`}`、そして三番目の中括弧には`{`テキスト`}`が入る。
![ss_fcolorbox.png](/ja_jp/mfm/ss_fcolorbox.png)
```
\(\fcolorbox{red}{yellow}{検閲により削除されました}\)
```

## その他

### ボックス
`\boxed{`と`}`でボックスを作ることができる。

# 外部リンク
- https://yuzulia.xyz/@aqz/pages/mfm 
[Yuzulia-MisSocial](/ja/instances/yuzulia_xyz)の@aqz氏によって書かれたMFM一覧表。かなり昔からある一覧表であり、また [ページ](/function/page)で書かれているのでソースを簡単に見ることができる。

- https://misskey.io/mfm-cheat-sheet
Misskey.io公式のチートシート。最新のMFMが実例ともに記載されている。

- https://katex.org/docs/support_table.html
アルファベット順にソートされたTeX関数の一覧。

- https://katex.org/docs/supported.html
ロジカルグループでソートされたTeX関数の一覧表集。

- https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#Color_keywords
HTML標準色名表。






