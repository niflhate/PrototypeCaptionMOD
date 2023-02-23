# PrototypeCaptionMOD 取扱説明書

## Todo
ファイル読み込みの並列化

## PrototypeCaptionMODの機能と目的
PrototypeCaptionMODは、Activision社から発売されているWindows用ビデオゲーム『PROTOTYPE』で使う字幕ファイルとフォントファイルを書き換えることができます。英語字幕から日本語字幕に書き換えることを、主な目的としています。

このリポジトリは fork 元である [psychi/PrototypeCaptionMOD](https://github.com/psychi/PrototypeCaptionMOD) に存在した不完全もしくは日本語として不自然な翻訳をある程度緩和し、翻訳量を増やしたものです。
（当方は英語読解はある程度できるものの、翻訳ができるほどの語学力はないため DeepL 翻訳とにらめっこしながら翻訳しました。）

## PrototypeCaptionMODの使用上の注意
字幕変更後にエラーが出て動かなかったらいい感じに csv 内の英語字幕側にある空白を埋めると機能します。

**ゲーム後半になるほどゲームの強制終了が発生しやすくなります**。

経験則ですが、アップグレードを開いて右の方の能力の字幕を読み込むと画面遷移時にフリーズが発生する気がします。
推測の域を出ませんが、漢字がいっぱい表示されると強制終了するイメージです。たぶんバカなんだとおもいます

こういった感じでゲームが強制終了する場合は、日本語字幕を全削除した csv を作成して再度 "PrototypeCaptionMOD/BuildCaptionsAndFonts.bat" を実行してゲームを進行してください。

## PrototypeCaptionMODをインストールする手順

### 1. 『PROTOTYPE』のインストール
Windows用『PROTOTYPE』を任意のディレクトリにインストールしてください。以後このディレクトリを"**Prototype/**"と表記します。

Fork 元である PrototypeCaptionMOD では日本語化 MOD や中国系の謎のソフトが必要でしたが，全部同梱しています．
（著作権的にはアレですが，放棄されたリポジトリもしくはもう怪しいアップローダにしかないソフトであるため......）

### 2. 『PROTOTYPE』データファイルの展開
『PROTOTYPE』が読み込むデータを編集できるようにするため、以下に示したパスにある8個のrcfファイルを以下の手順で展開してください。

* "Prototype/00audio.rcf"
* "Prototype/00woi.rcf"
* "Prototype/01audio.rcf"
* "Prototype/01woi.rcf"
* "Prototype/02woi.rcf"
* "Prototype/03woi.rcf"
* "Prototype/art.rcf"
* "Prototype/movies.rcf"

rcfファイルを展開するには、以下の手順に従ってください。

1. ScarfaceExplorerのメニューバーから「File」→「Open」を選択し、ファイルダイアログでrcfファイルを選択してください。
2. ScarfaceExplorerのメニューバーから「Extract」→「All Files」を選択し、ファイルダイアログで"**Prototype/**"を選択してください。
3. 展開した元のrcfファイルのファイル名を変更してください。元のrcfファイルがなければ、展開されたファイルを読み込むようになるからです。

8個すべてのrcfファイルを展開しファイル名を変更した状態で、『PROTOTYPE』が起動するのを確認してください。

### 3. PrototypeCaptionMODの入手
1. このリポジトリにある緑色の「Download」ボタンを押して、圧縮ファイルをダウンロードして下さい。
2. ダウンロードした圧縮ファイルを任意のディレクトリに展開してください。ただし、**展開先ディレクトリの絶対パス名には、全角文字が含まれない**ようにしてください。以後このディレクトリを"**PrototypeCaptionMOD/**"と表記します。

## 『PROTOTYPE』の字幕を日本語化する手順

### 1. データをコピー
以下に示したパスにある3個のディレクトリを、"**PrototypeCaptionMOD/**"の直下にコピーしてください。

* "Prototype/**art**"
* "Prototype/**Audio**"
* "Prototype/**movie**"

### 2. 字幕のテキストとフォントを日本語に書き換える
"PrototypeCaptionMOD/BuildCaptionsAndFonts.bat"をエクスプローラーでダブルクリックし、実行が終了するまで待機してください。

### 3. 書き換えたデータをコピー
以下に示したパスにある3個のディレクトリを、"**Prototype/**"の直下にコピーしてください。

* "PrototypeCaptionMOD/**art**"
* "PrototypeCaptionMOD/**Audio**"
* "PrototypeCaptionMOD/**movie**"

以上で、『PROTOTYPE』の字幕が日本語で表示されるようになります。『PROTOTYPE』を起動し、ゲーム設定で字幕の表示をONにするのを忘れないでください。
