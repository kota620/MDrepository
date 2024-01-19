JavaScriptのコールバック関数の簡単な例

今日JavaScriptのコールバック関数について勉強したので、学習した内容を少し書いてみたいと思います。

## コールバック関数とは
コールバック関数とはMDNによると
> コールバック関数とは、引数として他の関数に渡され、外側の関数の中で呼び出されて、何らかのルーチンやアクションを完了させる関数のことです。
> 引用：[Callback function (コールバック関数)](https://developer.mozilla.org/ja/docs/Glossary/Callback_function)

という説明になっていました。
なかなかこれだけだと理解するのが難しかったので、簡単な例を参照して理解してみたいと思います。

## コールバック関数の例
```js
//関数messageを定義
const message = () => {
    console.log('メッセージを受け取りました。');
};

//関数sentenceを定義
const sentence = (callback) => {
    console.log('こんにちは。');
    callback();
};

//messageをコールバック関数としてsentenceに渡す
sentence(massage);

//以下、出力結果
//こんにちは。
//メッセージを受け取りました。
```
今回、messageとsentenceが関数として定義されています。
また、messageは引数としてsentenceに渡されています。

コールバック関数の流れとしては、まず引数としてmessageが渡され、sentenceが呼び出されます。
次に引数であるmessageはcallbackに代入され、sentence内の処理に書かれているcallbackに代入され処理が実行されます。

この引数になっている関数（今回ではmessage）のことをコールバック関数と呼びます。

## まとめ
今回、JavaScriptのコールバック関数の簡単な例について書いてみました。コールバック関数も奥が深そうなので色々な使い方について学んでみたいと思います🏃