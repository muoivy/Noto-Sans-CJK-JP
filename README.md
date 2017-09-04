# Noto Sans CJK JP（Japanese）
サブセット化済みの「Noto Sans CJK JP」のCSS付きWebフォント  

## Google Webフォントのダウンロード
[http://www.google.com/get/noto/#/family/noto-sans-jpan](http://www.google.com/get/noto/#/family/noto-sans-jpan)  

## WOFFコンバータ
[http://opentype.jp/woffconv.htm](http://opentype.jp/woffconv.htm)  
様々なブラウザに対応するため4種類のフォーマットのファイルを作成  
* eot
* ttf
* woff2
* woff

### 各ブラウザの対応フォーマット
|フォーマット|Chrome|Firefox|Opera|Safari|IE/Edge|
|:---:|:---:|:---:|:---:|:---:|:---:|
|TTF/OTF|4|3.5|10|3.1|9[1]|
|WOFF|5|3.6|11.10|5.1|9|
|WOFF2|36|39|23|10|Notsupported|
|EOT|Notsupported|Notsupported|Notsupported|Notsupported|6|

## サブセット化
[http://opentype.jp/subsetfontmk.htm](http://opentype.jp/subsetfontmk.htm)  
サブセットフォントメーカーを使用して、アスキー文字 + 非漢字文字 + 第1水準漢字でサブセット化し、ファイルサイズを削減します。  
約16MBあるファイルサイズが700KBにまで減少します。

## CSSの書き方
```c
@font-face {
    font-family: 'Noto Sans Japanese';
    font-style: normal;
    font-weight: 100;
    src: url('../fonts/NotoSansCJKjp-Thin.woff2') format('woff2'),
	       url('../fonts/NotoSansCJKjp-Thin.woff') format('woff'),
	       url('../fonts/NotoSansCJKjp-Thin.ttf')  format('truetype'),
         url('../fonts/NotoSansCJKjp-Thin.eot') format('embedded-opentype');
```
