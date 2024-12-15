コントローラーはルーティングのみを担当する

# DIのタイプ
DIにはモジュール内でDIする内部的なもの
外部のモジュールからDIするパターンがある
　

# どのようにDIするのか
内部的にDIする
1. InjectuonしたいServiceに@Injectionデコレータをつける
2. Serviceで使用したModuleのProvidersに登録
3. ControllerのコンストラクタにServiceを追加する

外部的にDIする
1. Moduleのimportsに外部Moduleを登録する。
2. 内部的にDIしているときと同じようにすることができる

外部ライブラリもDIすることができる。
JWTなどのライブラリでは@Injectionを使っているのでModuleに登録するとJWTのServiceを使用することができる。