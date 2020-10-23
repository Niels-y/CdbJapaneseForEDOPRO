[日本語](README_ja.md)

# CdbJapaneseForEdopro

Card data based on the English card data of YGOPro `Project Ignis` (`EDOPRO`), with Japanese card names and text added.

#### note

* The behavior of the effect follows the card data of `Project Ignis`. Therefore, it is expected that it does not interfere with the game on the general server of `Project Ignis`.
 
#### Untranslated cards

1. Cards not yet been added to the Japanese card data for translation
1. Cards with different internal-ID for Japanese card data for translation and English card data
   * e.g. ID change with the release of pre-release cards
   * e.g. Cards with an internal ID for each of the multiple illustrations (could be both translated-illustrations and untranslated-illustrations)
1. Other Reasons

#### Examples of Translations

* card name: `Ｅ・ＨＥＲＯ フレイム・ウィングマン(Elemental HERO Flame Wingman)`
* card text:
```
「Ｅ・ＨＥＲＯ フェザーマン」＋「Ｅ・ＨＥＲＯ バーストレディ」
このカードは融合召喚でしか特殊召喚できない。
①：このカードが戦闘でモンスターを破壊し墓地へ送った場合に発動する。
そのモンスターの元々の攻撃力分のダメージを相手に与える。
"Elemental HERO Avian" + "Elemental HERO Burstinatrix"
Must be Fusion Summoned and cannot be Special Summoned by other ways. When this card destroys a monster by battle and sends it to the Graveyard: Inflict damage to your opponent equal to the ATK of the destroyed monster in the Graveyard.
```

## Usage

1. Open `C:\ProjectIgnis/config/configs.json` with a text editor.
1. Add the following content after line 13, and save.
1. Run `Project Ignis`. Then the `repositories/Japanese` folder is created automatically and the Japanese card data is downloaded.

Content to be added
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

#### screenshot

<img width="564" alt="edit_config_json_notepad_mini" src="https://user-images.githubusercontent.com/72937182/96492130-21f7cf80-127e-11eb-8334-12a9de35da60.png">

#### How to stop

How to avoid loading translation card data temporarily
* Change `"should_read": true` in the second line from the bottom of the added content to `"should_read": false`.

How to delete translation card data
* Restore the `config/configs.json`. And delete the `repositories/Japanese` folder.

## Data changed by translation

* card name
* card text

That's all.

## supplement
* Card names and text are in both Japanese and English for the following reasons.
  * Some cards have not been translated. Untranslated cards cannot be searched in Japanese, but can be searched in English. Therefore, the English card names and text are left behind.
* If the current `Project Ignis` card data has changed since the translation, it will probably be reflected as follows.
  * atk, category: not reflected. They remain fixed to those of the translation card data.
  * effect: reflected. The latest behavior of `Project Ignis`.

