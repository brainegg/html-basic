
<p align="center">
<img src="https://brainegg.net/img/site_id_brainegg_b2.svg" width="360" height="66" alt="BrainEgg.Net">  
</p>
<p align="center"> BrainEgg HTML Basic Package</p>

## Directory

+ htdocs/ 
    + index.html
    + img/
        + logo_site_id.svg
    + css/
        + base.css
        + project.css
        + print.css
    + js/
        + common.js
    + lib/
        + jquery/
            + jquery-3.3.1.min.js


## Naming

### Folder 

|type| |description|
|----|----|-----------|
|img|image|画像|
|doc|document|ドキュメント(pdf,doc,xls)|
|ico|icon|アイコン|
|js|javascript|スクリプト|
|lib|library|ライブラリー、プラグイン|
|css|style sheet|スタイルシート|

<!--
<table width="100%" style="width:100%">
<colgroup>
<col style="width:8%" span="2">
</colgroup>
<thead><tr><th>name</th><th colspan="2">description</th></tr></thead>
<tbody>
<tr><td>img</td><td>image</td><td>画像</td></tr>
<tr><td>ico</td><td>icon</td><td>アイコン</td></tr>
<tr><td>doc</td><td>document</td><td>ドキュメント(pdf,doc,xls)</td></tr>
<tr><td>js</td><td>javascript</td><td>スクリプト</td></tr>
<tr><td>lib</td><td>library</td><td>ライブラリー、プラグイン</td></tr>
<tr><td>css</td><td>style sheet</td><td>スタイルシート</td></tr>
</tbody>
</table>-->


### Image 

[type] _ [description] _ [number] _ [state].extension( jpg | png | svg )

|type| |description|
|----|----|-----------|
|logo|logo| ロゴ|
|ico|icon|アイコン|
|img|image|写真、グラフ、イラスト|
|bg|background|背景画像|
|h|heading|見出し|
|txt|text|文字|
|btn|button|ボタン|
|nav|navigation|ナビゲーション|

### Style Sheet

|type| |description|
|----|----|-----------|
|bs|base style|base.cssのユーティリティ、モジュール、コンポーネントスタイル|
|pj|project style|project,cssのサイト固有のスタイル|
|sc|special content style|スペシャルサイトのスタイル|

#### Class 
 
    [type]-class--modifier(state|size)
    [type]-class@device[Tablet|Sp] 
    [type]-class__inner
    [type]-class__header 
    [type]-class__body
    [type]-class__footer
    [type]-class__title
    etc.
    
  
---  

## Base Style Class ( base.css )

+ 基本CSSのプロパティ名に極力準拠
+ サイズは大文字で XS, S, M, L, XL
+ デバイス指定は、@Tablet, @Sp, @SpLand, @SpPort
+ normalize.8.00をバンドル
+ マージン、パッティング等はは多用しすぎるとデザインルールが崩れるので含まない。<br>間隔をあけるものはproject.cssに記述して3～5パターンに抑えて固定された数値表記のクラスを作らないようにする。


<b>*</b> はデバイス指定あり 下記 Device Break point 参照 

### Utility

<table>
<thead width="100%">
<tr> <th>type</th> <th>class</th> <th>description</th> </tr>
</thead>
<tbody width="100%">
<tr><td>font size</td> <td>bs-font *</td> <td>bs-font_( XS, S, M, L, XL )</td> </tr>
<tr><td>text</td> <td>bs-text *</td> <td>bs-text_( right, center, left, bold. underline )、 right, center, leftのみデバイス対応</td></tr>
<tr> <td>color</td> <td>bs-color</td> <td>bs-color_( red, blue, green, yellow )</td> </tr>
<tr> <td>width</td> <td>bs-width *</td> <td>bs-width_(1-1 ~ 10-10) 1of1 ~ 10of10</td> </tr>
<tr> <td>hr</td> <td>bs-hr</td> <td>bs-hr_( dot, dosh, bevel, emboss, double )</td> </tr>
<tr> <td>float</td> <td>bs-float</td> <td>bs-float_( left, right )</td> </tr>
<tr> <td>overflow</td> <td>bs-overflow</td> <td>bs-overflow_( auto, hidden, scroll, scrollX, scrollY )</td> </tr>
<tr> <td>nowrap</td> <td>bs-nowrap</td> <td>bs-nowrap : white-space: nowrap</td> </tr>
<tr> <td>clear</td> <td>bs-clear</td> <td>bs-clear : clear : both</td> </tr>
<tr> <td>display</td> <td>bs-show *</td> <td>bs-show@( Desk, Tablet, Sp, SpLand, SpPort ) 指定のデバイスサイズのみ表示</td> </tr>
<tr> <td></td> <td>bs-hide *</td> <td>bs-hide@( Tablet, Tablet-lte, Sp, SpLand, SpPort ) 指定のデバイスサイズのみ非表示</td> </tr>
</tbody></table>

<!--
|type|class|description|
|-----|-----------|----|
|font size|bs-font *| bs-font_( XS, S, M, L, XL )  |
|text|bs-text *| bs-text_( right, center, left, bold. underline )、 right, center, leftのみデバイス対応 |
|color|bs-color|bs-color_( red, blue, green, yellow ) |
|width|bs-width *|bs-width_(1-1 ~ 10-10) 1of1 ~ 10of10 |
|hr|bs-hr|bs-hr_( dot, dosh, bevel, emboss, double )|
|float|bs-float|bs-float_( left, right )|
|overflow|bs-overflow|bs-overflow_( auto, hidden, scroll, scrollX, scrollY )|
|nowrap|bs-nowrap|bs-nowrap : white-space: nowrap|
|clear|bs-clear|bs-clear : clear : both |
|display|bs-show *|bs-show@( Desk, Tablet, Sp, SpLand, SpPort ) 指定のデバイスサイズのみ表示|
| |bs-hide *|bs-hide@( Tablet, Tablet-lte, Sp, SpLand, SpPort ) 指定のデバイスサイズのみ非表示| 
-->
### Module
|type|class|description|
|-----|-----------|----|
|list ( ul, ol )|bs-list|リスト要素をリセット|
| |bs-list--gap|bs-list--gap_( S, M, L ) 、custom時の横の間隔を調整|
| |bs-list--rowGap|bs-list--rowGap_( S, M, L ) 、縦の間隔を調整 |
| |bs-list--inline|リストを並列表示|
| |bs-list--custom|リストマークを任意に変更、<br> 使用する場合構成を li > elem{任意} + {text} にする|
| |bs-list--(opt)|bs-list--( horizon_line, vertical_line ) 、ボーダーを追加 |
|table|bs-table|テーブル要素をリセット|
| |bs-table--gap|bs-table--gap_( S, M, L )|
| |bs-table--(opt)|bs-table--( horizon_line, lattice, zebra, light, dark ) 、ボーダーを追加、 横ラインの背景を交互に着色 、カラーリング|
|flex|bs-flex| ul,ol対応 list要素をリセット<br> *ie9* 以下 では 子要素inline-block に変更 、center、 end、 columnのみ対応  |
| |bs-flex--gap|bs-flex--gap_( S, M, L )|
| |bs-flex--col *|bs-flex--col_( 1 ~ 12 )|
| |bs-flex--(opt)|bs-flex--( center, end, between, reverse, column, middle )|
|ico|bs-ico|スプライト用にリセット、画像はimg/ico/ico_project.svg を使用
| |bs-ico--(opt)|bs-ico--( M, L, type ) サイズ指定( デフォルト16x16,M:32ｘ32,L:64ｘ64)、アイコンタイプ指定詳細は別途記載|

### Component
|type|class|description|
|-----|-----------|----|
|figure|bs-figure|  画像等(メディア)とキャプション <br> bs-figure > <br>bs-figure__img +  bs-figure__caption |
|media|bs-media| 画像等(メディア)とテキスト <br> bs-media > <br>bs-media__side +  bs-media__body  |
| |bs-media--gap| bs-media--gap_( S, M, L ) side と body の間隔を調整|
| |bs-media--(opt) *| bs-media--( column, reverse ) 指定のデバイスで垂直配置、上下反転|
| |bs-media__side| bs-media__side--( left, right ) 左、右に配置 |
| |bs-media__body| bs-media__body--( melt ) sideに回り込み |
|panel|bs-panel| 装飾パネル <br> bs-panel > <br>bs-panel__header + bs-panel__body|
| |bs-panel--(opt)| bs-panel--( round, light, gray, dark ) 丸角、カラーリング|
| |bs-panel__header| bs-panel__header--( separator ) header と body の間にボーダーを追加 |

### Device Break Point
	ex.) bs-font@Tablet_S 、 bs-flex@Sp--col_1

|class|range|description|
|-----|-----:|-----------|
|(class)@Tablet-lte| 0 ~ 800| max-width: 800px |
|(class)@Tablet|  668 ~ 800 | min-width: 668px and max-width: 800px |
|(class)@Sp| 0 ~ 667| max-width: 667px |
|(class)@SpLand|481 ~ 667| min-width:481 and max-width: 667px|
|(class)@SpPort|0 ~ 480| max-width: 480px /
