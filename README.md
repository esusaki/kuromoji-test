- コンソールを見ると、形態素解析の結果が表示される（はず）

- ローカルで実行すると、CORSエラーが出てうまく動きませんが、Vercel上なら動きます（なんでそうなのかはあんまりよくわかってない）

- kuromoji.jsの内容を、別のJSファイルから呼び出すことに失敗しました。そのため、本来kuromoji.jsの中には書くべきではない内容（以下）を、kuromoji.jsの末尾に書いています。

  ```
   kuromoji.builder({ dicPath: "./dict" }).build(function (err, tokenizer) {
        // tokenizer is ready
        var path = tokenizer.tokenize("すもももももももものうち");
        console.log(path);
    });
  ```
