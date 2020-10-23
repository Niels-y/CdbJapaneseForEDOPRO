[English](README.md)

# CdbJapaneseForEdopro

ADS `Project Ignis` (`EDOPRO`) の英語カードデータをベースに、一部のカードに **日本語の名前とテキストを追加** したカードデータ。

#### 備考

* 効果の挙動は`Project Ignis`のカードデータに従っている。そのため、`Project Ignis` の一般サーバー上ではゲームに支障をきたすことはないと考えられる。
 
#### 翻訳されていないカード

1. 翻訳用日本語カードデータにまだ追加されていないカード
1. 翻訳用日本語カードデータと英語カードデータの内部IDが異なるカード
   * 例. プレリリースカードのリリースに伴うID変更
   * 例. 複数のイラストのそれぞれに内部IDが付与されたカード (翻訳されたイラストと翻訳されていないイラストの両方があるかもしれない)
1. その他の理由

#### 翻訳の例

* カード名: `Ｅ・ＨＥＲＯ フレイム・ウィングマン(Elemental HERO Flame Wingman)`
* テキスト:
```
「Ｅ・ＨＥＲＯ フェザーマン」＋「Ｅ・ＨＥＲＯ バーストレディ」
このカードは融合召喚でしか特殊召喚できない。
①：このカードが戦闘でモンスターを破壊し墓地へ送った場合に発動する。
そのモンスターの元々の攻撃力分のダメージを相手に与える。
"Elemental HERO Avian" + "Elemental HERO Burstinatrix"
Must be Fusion Summoned and cannot be Special Summoned by other ways. When this card destroys a monster by battle and sends it to the Graveyard: Inflict damage to your opponent equal to the ATK of the destroyed monster in the Graveyard.
```

## 使い方

1. `C:\ProjectIgnis/config/configs.json` をテキストエディタで開く。
1. 13行目の後に以下の内容を追加して保存する。
1. `Project Ignis` を実行する。すると自動的に `repositories/japanese` フォルダが作成され日本語のカードデータがダウンロードされる

追加する内容
```

		{
			"url": "https://github.com/Niels-y/CdbJapaneseForEdopro",
			"repo_name": "Japanese CardData",
			"repo_path": "./repositories/japanese",
			"has_core": false,
			"core_path": "",
			"data_path": "data",
			"script_path": "",
			"should_update": true,
			"should_read": true
		},
```

#### スクリーンショット

<img width="564" alt="edit_config_json_notepad_mini" src="https://user-images.githubusercontent.com/72937182/96492130-21f7cf80-127e-11eb-8334-12a9de35da60.png">

#### 停止方法

翻訳カードデータを一時的に読み込まない方法
* 追加した内容の下から2行目の `"should_read": true` を `"should_read": false` に変更する。

翻訳カードデータを削除する方法
* `config/configs.json` を元に戻す。そして `repositoriesjapanese` フォルダを削除する。

## 翻訳により変更されたデータ

* card name
* card text

That's all.

## 補足
* カード名とテキストは、以下の理由で日本語と英語の両方がある。
  * 翻訳されていないカードもある。未翻訳のカードは日本語では検索できないが、英語では検索できる。そのため、英語のカード名とテキストは残している。
* 現在の`Project Ignis`のカードデータが翻訳後に変更されている場合は、おそらく以下のように反映される。
  * 攻撃力、カテゴリ: 反映されない。翻訳カードデータに固定されたまま。
  * 効果: 反映される。 `Project Ignis` の最新の挙動。

