PassGer
====================================================================================================
説明
----------------------------------------------------------------------------------------------------
簡易なパスワード生成アプリ。

パスワードに使う文字の種類を一文字ごとに指定できます。

![pic1](docs/images/screenshot-1_ja.png)

また文字の種類ごとに使用したい文字を指定できます。  
たとえば、`[`や`]`をパスワードに使用したくない人もいるでしょう。

![pic2](docs/images/screenshot-2_ja.png)

セキュリティの観点からこのアプリは保存機能を持っていません。

GNOME Passwordsafeのような信頼性の高いパスワード管理用アプリを用意し、コピー&ペーストして保存してく
ださい。

ビルド
----------------------------------------------------------------------------------------------------
### 準備
* GTK+-3.0 (e.g. libgtk-3-dev)
* gcc
* make
* vala compiler (valac)

### ビルド手順
手早くビルドしたい人向け (デバッガー等) にMakefileが用意されています。

    $ make

より推奨される方法は「Mesonビルドシステム」を使用することです。

    $ meson build --prefix=/usr
	$ cd build
	$ meson compile # or ninja

インストール
----------------------------------------------------------------------------------------------------
`make`によって生成された実行可能ファイル`passger`をすぐに起動できます。
環境変数PATHが通っているロケーションに移動して使用してください。

あるいは`PREFIX`引数を指定して`make install`によってもインストール可能です。

    $ make intsall PREFIX=~/.local

Mesonを使用する場合、以下のコマンドを使用してください。

    $ sudo meson install

クレジット
----------------------------------------------------------------------------------------------------
Copyright 2021 (C) Tanaka Takayuki <https://github.com/aharotias2>