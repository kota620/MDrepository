今日JavaScriptの分割代入を学習していたところエラーが出てしまったので、どうしてエラーが出てしまったのかについて記事を書いてみたいと思います。

## そもそも分割代入とは

分割代入 (Destructuring assignment) 構文は配列の値を取り出して、あるいはオブジェクトのプロパティを取り出して別の変数に代入するJavaScriptの式です。

#### 配列の値を取り出す場合
```js 
const number = [1, 2, 3];

const [a, b, c] = number;

console.log(a); //1
console.log(b); //2
console.log(a); //3
```
#### オブジェクトのプロパティを取り出す場合
```js
const person = {name: 'John', age: 30};

const {name, age} = person;

console.log(name); //John
console.log(age); //30
```
の様な形で使うことができます。

## どんなエラーを起こしたか

私がエラーを起こしてしまった記述は以下の様なものでした
```js
const person = {name: 'John', age: 30};

const [name, age] = person;

console.log(name); 
console.log(age); //error
```
すぐに気づいた方もいらっしゃると思いますが、今回代入するものがオブジェクトなので2行目の[name, age]の[]を{}に変更する必要がありました。

## まとめ
今回JavaScriptの分割代入でのエラー体験について書いてみました。自分で解決できることが増えるように学習を進めてみようと思います🏃
