https://github.com/KnpLabs/snappy


EN:
I created generateFromHtml(), generateFromXml() and generateFromTxt() method.

wkhtmltopdf is not a single kind of rendering program.
Local input files are rendered differently depending on the file extension.
You can choose three rendering engines of txt html xml with generateFromHtml(), generateFromXml() and generateFromTxt().

JA:
generateFromHtml(), generateFromXml() and generateFromTxt() メソッドを追加しました。

wkhtmltopdf は1つのレンダリング プログラムではありません。
ローカルファイルの場合、入力するファイル拡張子によって レンダリング プログラム が違ってきます。
generateFromHtml(), generateFromXml(), generateFromTxt() の3種類を追加しました。
txt html xml のレンダリング プログラムを使い分けることができるようになりました。

### Generate local pdf file 
```php
$snappy = new Pdf('/usr/local/bin/wkhtmltopdf');
$snappy->generateFromHtml('<h1>Bill</h1><p>You owe me money, dude.</p>', '/tmp/bill-123.pdf');
```

```php
$snappy = new Pdf('/usr/local/bin/wkhtmltopdf');
$snappy->generateFromTxt('Hello World', '/tmp/bill-123.pdf');
```

```php
$snappy = new Pdf('/usr/local/bin/wkhtmltopdf');
$snappy->generateFromXml('<svg> ..... </svg>', '/tmp/bill-123.pdf');
```

