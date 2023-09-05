# dev-sendmail
[sendmail.4dbase](https://github.com/miyako/4d-component-sendmail)をサポートするためにCLI版のcURLを再コンパイルする

**注記**: curlの簡易的なラッパーである当該コンポーネントは，v14で非Unicodeの日本語メールを送受信するための回避策として公開されたものです。現行バージョンでこのようなものを使用するメリットはありません。

さらにいえば，curlはmacOSおよびWindowsにプリインストールされており，パッケージマネージャーでも保守することができるので，コンポーネントとして配付することもあまりスマートなやり方とはいえません。

# 問題点

オリジナルのコンポーネントにインストールされているMac版のcurlは，i386/x86_64のUniversal Binaryですが，macos-109.sdkよりも古いツールセットでコンパイルされているので，公証にパスすることができません。

* The binary uses an SDK older than the 10.9 SDK.
* The signature does not include a secure timestamp.
* The executable does not have the hardened runtime enabled.
* The binary is not signed.

https://developer.apple.com/documentation/security/notarizing_macos_software_before_distribution/resolving_common_notarization_issues#3087723

# 回避策

システムのcurlで代用します。
