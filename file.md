JavaScriptのfilterメソッドの簡単な使い方

今日はJavaScriptのfilterメソッドについて勉強したので、その簡単な使い方について少し書いてみたいと思います。

## filterメソッドとは
filterメソッドとはMDNによると
> filter() は Array インスタンスのメソッドで、指定された配列の中から指定された関数で実装されているテストに合格した要素だけを抽出したシャローコピーを作成します。
> 引用：[Array.prototype.filter()](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

という説明になっていました。
なかなかこれだけだと理解するのが難しかったので、今回も簡単な例を参照して理解してみたいと思います。

## filterメソッドの例
```js
// 配列agesを定義
const ages = [10, 15, 18, 25, 40];

// 18以上の要素だけを取り出し、新しい配列に格納する。
const adult = ages.filter(age => age >= 18); 

//adultを出力
console.log(adult); // [18, 25, 40]
```
今回、まず配列agesを定義します。

そして、成人の年齢18以上の要素だけを取り出し、新しい配列に格納するためにfilterメソッドを使い引数にコールバック関数（今回はage => age >= 18で、コールバック関数については[JavaScriptのコールバック関数の簡単な例](https://zenn.dev/kota1234/articles/ce25d7cc6794d7)で簡単に書いています。）で18以上の要素だけを取り出しています。

そしてadultを出力すると出力結果が[18, 25, 40]となります。

## まとめ
今回、JavaScriptのfilterメソッドの簡単な例について書いてみました。filterメソッドも色々な使い方がある様なので徐々に学んでいきたいと思います🏃