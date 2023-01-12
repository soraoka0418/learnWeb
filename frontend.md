# frontend 勉強会

## ES2022 の便利機能

https://speakerdeck.com/tonkotsuboy_com/koredakehaya-saeteokitai-es2022nobian-li-ji-neng?slide=7

<!-- その他 -->

クラスフィールド宣言

```js
// constructorの中でしか宣言できなかった
// # でプライベートなメソッドやフィールドにできる

// staticでインスタンス化なしでクラスのフィールドにアクセスできる
// staticイニシャライザー（初期化処理）がつかえるようになった
class Human {
  age = 23;
}
const human = new Human();

class Animal {
  static name;
  static {
    this.name = "猫";
  }

  // tsのprivate修飾子はコンパイル後にpublicなるが#はprivateのままになる。
  #void = "ニャー";
}

console.log(Animal.name);
```

トップレベルでの async

モジュールでのみ使用可能

```js
// await関数の外でもasyncが使えるようになった

await new Promise((resolve) => {
  setTimeout(() => {
    alert("1秒");
    resolve();
  }, 1000);
});
```

## ビジュアル表現のための CSS

https://speakerdeck.com/yuneco/biziyuarubiao-xian-notamenocss-and-svg-and-javascriptnozui-xin-shi-qing

Web Animations API の composite の記事
https://qiita.com/yuneco/items/8be607b9bfe8e609a658

translate
https://developer.mozilla.org/ja/docs/Web/CSS/translate

rotate
https://developer.mozilla.org/ja/docs/Web/CSS/rotate

transform
https://developer.mozilla.org/ja/docs/Web/CSS/transform

## Fresh

https://www.slideshare.net/yuyayamaguchi6/20221017qiitanightver2pdf
fresh 公式
https://fresh.deno.dev/

## Qwik

https://www.docswell.com/s/kawamataryo/K4GW15-qwik-resumable?utm_source=twitter&utm_medium=social&utm_campaign=singlepage#p1

Qwiq 公式
https://qwik.builder.io/
