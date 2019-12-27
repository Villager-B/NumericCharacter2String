# NumericCharacter2String 

PythonでNetworkXを使用しているときに`networkx.write_gml()`を使用したら
日本語が数値文字参照のせいで記号列になってしまい，CytoScapeで表示する際に??となったので
数値文字参照を文字列に変換するPythonスクリプトを用意しました．

## Useage

数値文字参照になっている任意のファイル名をコマンドライン引数として与えることで
`filename-unescape.fileextension`の文字列に変更されたファイルが生成される．

```
python numetric_char_str.py [filename]
```

## Sample

### test.txt
```
&#25991;&#31456;&#9834;
&#x3042;&#x3044;&#x3046;&#x3048;&#x304a;
&gt;
```

### test-unescape.txt
```
文章♪
あいうえお
>
```