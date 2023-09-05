# dev-curl-7_75_0
[sendmail.4dbase](https://github.com/miyako/4d-component-sendmail)をサポートするためにCLI版のcURLを再コンパイルする

**注記**: curlの簡易的なラッパーである当該コンポーネントは，v14で非Unicodeの日本語メールを送受信するための回避策として公開されたものです。現行バージョンでこのようなものを使用するメリットはありません。

さらにいえば，curlはmacOSおよびWindowsにプリインストールされており，パッケージマネージャーでも保守することができるので，コンポーネントとして配付することもあまりスマートなやり方とはいえません。

# curl

```
file curl
Mach-O universal binary with 2 architectures: [x86_64:Mach-O 64-bit executable x86_64] [i386:Mach-O executable i386]
```

* i386は`10.9sdk`よりも古い
