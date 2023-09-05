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

```
otool -L curl
@loader_path/libcurl.4.dylib (compatibility version 8.0.0, current version 8.0.0)
@loader_path/libidn.11.dylib (compatibility version 18.0.0, current version 18.12.0)
@loader_path/libintl.8.dylib (compatibility version 10.0.0, current version 10.3.0)
/usr/lib/libSystem.B.dylib (compatibility version 1.0.0, current version 1213.0.0)
@loader_path/libiconv.2.dylib (compatibility version 8.0.0, current version 8.1.0)
@loader_path/libssh2.1.dylib (compatibility version 2.0.0, current version 2.1.0)
@loader_path/libssl.1.0.0.dylib (compatibility version 1.0.0, current version 1.0.0)
@loader_path/libcrypto.1.0.0.dylib (compatibility version 1.0.0, current version 1.0.0)
/System/Library/Frameworks/LDAP.framework/Versions/A/LDAP (compatibility version 1.0.0, current version 2.4.0)
@loader_path/libz.1.dylib (compatibility version 1.0.0, current version 1.2.8)
```
