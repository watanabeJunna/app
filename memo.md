## 作業メモ

チャプター1で下記の様なコードに遭遇した 

~~~~js
var spa = (function () {
    var initModule = function ($container) {
        $container.html(
            '<h1 style="display:inline-block;margin: 25px">Hello World!</h1>'
        );
    }
    return { initModule: initModule };
}());
~~~~

変数に関数を代入する場合、通常の関数宣言とは違う点が存在する
上記の行っていることは略すと下記の様になる。

~~~~js
var a = (function(){var b = function(){return '通貨'};return {b:b}}());
~~~~

ポイントは親変数の関数内で宣言された変数に外からアクセスできない。

変数は返り値を持たない場合、内部でいかなる構造を持っていても返さなければ出力できない。
また関数を変数に代入する場合には、即時実行を行わないと内部にアクセスできない。関数を((){}()),(){}()で実行する。

最後に返り値を変数、関数にした場合には返り値を持った変数自身が値を出力する、{}記法でオブジェクトで返す場合には、親はインスタンスを持つ。

