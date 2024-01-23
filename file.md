

今日はJavaScriptのfindメソッドについて学習したので、少し書いてみたいと思います。

## findメソッドとは
findメソッドとはMDNによると
> find() は Array インスタンスのメソッドで、提供されたテスト関数を満たす配列内の最初の要素を返します。 テスト関数を満たす値がない場合は、 undefined を返します。
> 引用：[Array.prototype.find()](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
の様に説明されていました。
つまり、findメソッドを使うことである配列の中で条件を設定し、その条件にあった最初の値を一つ取得することができ、条件を満たす値がない場合は、 undefined を返すものとなっています。

## findメソッドの使い方の例

```js
const ages = [1, 2, 3, 4, 5];
const found = numbers.find(element => element > 3);
console.log(found); // 4
```
配列内の最初の要素を返します。指定した要素が見つからない場合はundefinedを返します。
```js
// 配列agesを定義
const ages = [10, 15, 18, 25, 40];

// 18以上の要素だけを取り出し、新しい配列に格納する。
const adult = ages.find(age => age >= 18); 

//adultを出力
console.log(adult); // 18
```
今回、まず配列agesを定義します。

そして、成人の年齢18以上の要素だけを取り出し、新しい配列に格納するためにfindメソッドを使い引数にコールバック関数で18以上の最初の要素を取り出しています。

そしてadultを出力すると出力結果が18となります。

## まとめ
今日はJavaScriptのfindメソッドについてについて少し書いてみました。findメソッドも色々な使い方がありそうなので学習していきたいと思います🏃
