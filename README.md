
<p align="center">
<img src="https://brainegg.net/img/site_id_brainegg_b2.svg" width="360" height="66" alt="BrainEgg.Net">  
</p>
<p align="center"> BrainEgg HTML Basic Package</p>

---  

## Directory

+ htdocs/ 
    + index.html
    + img/
        + logo_site_id.svg
        + ico/
    		+ ico_project.svg
    + css/
        + base.css
        + project.css
        + print.css
    + js/
        + common.js
    + lib/
        + jquery/
            + jquery-3.3.1.min.js

---  

## Naming

|type| |description|
|----|----|-----------|
|<b>/* Folder */</b>|
|img|image|画像|
|img/ico|icon|アイコン|
|img/bg|background|背景画像|
|img/nav|navigation|ナビゲーション、ボタン|
|doc|document|ドキュメント(pdf,doc,xls)|
|js|javascript|スクリプト|
|lib|library|ライブラリー、プラグイン|
|css|style sheet|スタイルシート|
|<b>/* Image */</b>|
|logo|logo| ロゴ|
|ico|icon|アイコン|
|img|image|写真、グラフ、イラスト|
|bnr|banner|バナー|
|thmb|thumbnail|サムネイル|
|bg|background|背景画像|
|h|heading|見出し|
|txt|text|文字|
|btn|button|ボタン|
|<b>/* Style Sheet */</b>|
|bs|base style|base.cssのユーティリティ、モジュール、コンポーネントスタイル|
|pj|project style|project,cssのサイト固有のスタイル|
|sc|special content style|スペシャルサイトのスタイル|

#### Image file Example
	[type] _ [description] _ [number] _ [state].extension( jpg | png | svg )
	
#### Style Class Example
 
    [type]-[class]--modifier(state|size)
    [type]-[class]@( Tablet, Sp, SpLand, SpPort ) 
    [type]-[class]__( inner, header, body, footer, cell, title, list, item, btn )
    etc.
  
---  

## Base Style Class ( base.css | prefix : bs-  )

+ 基本CSSのプロパティ名に極力準拠
+ サイズは大文字で XS, S, M, L, XL
+ デバイス指定は、@Tablet, @Sp, @SpLand, @SpPort
+ normalize.8.00をバンドル
+ マージン、パッティング等はは多用しすぎるとデザインルールが崩れるので含まない。<br>間隔をあけるものはproject.cssに記述して3～5パターンに抑えて固定された数値表記のクラスを作らないようにする。


<b>*</b> はデバイス指定あり 下記 Device Break point 参照 

|type|class|description|
|-----|-----------|----|
|<b>/* Utility */</b>| | |
|font size|bs-font *| bs-font_( XS, S, M, L, XL )  |
|text|bs-text *| bs-text_( right, center, left, bold. underline )、 <br>right, center, leftのみデバイス対応 |
|color|bs-color|bs-color_( red, blue, green, yellow ) |
|width|bs-width *|bs-width_(1-1 ~ 10-10) 1of1 ~ 10of10 |
|hr|bs-hr|bs-hr_( dot, dosh, bevel, emboss, double )|
|float|bs-float|bs-float_( left, right )|
|overflow|bs-overflow|bs-overflow_( auto, hidden, scroll, scrollX, scrollY )|
|nowrap|bs-nowrap|bs-nowrap : white-space: nowrap|
|clear|bs-clear|bs-clear : clear : both |
|display|bs-show *|bs-show@( Desk, Tablet, Sp, SpLand, SpPort ) <br>指定のデバイスサイズのみ表示|
| |bs-hide *|bs-hide@( Tablet, Tablet-lte, Sp, SpLand, SpPort ) <br>指定のデバイスサイズのみ非表示| 
|<b>/* Module */</b>| | |
|list ( ul, ol )|bs-list|リスト要素をリセット|
| |bs-list--gap|bs-list--gap_( S, M, L ) 、custom時の横の間隔を調整|
| |bs-list--rowgap|bs-list--rowgap_( S, M, L ) 、縦の間隔を調整 |
| |bs-list--inline|リストを並列表示|
| |bs-list--custom|リストマークを任意に変更、<br> 使用する場合構成を li > elem{任意} + {text} にする|
| |bs-list--(opt)|bs-list--( horizon_line, vertical_line ) 、ボーダーを追加 |
|table|bs-table|テーブル要素をリセット|
| |bs-table--gap|bs-table--gap_( S, M, L )|
| |bs-table--(theme)|bs-table--( light, dark  )、カラーリング|
| |bs-table--(opt)|bs-table--( horizon_line, lattice, zebra ) 、<br>ボーダーを追加、 横ラインの背景を交互に着色 |
|flex|bs-flex| ul,ol対応 list要素をリセット<br> *ie9* 以下 では 子要素inline-block に変更 、<br>center、 end、 columnのみ対応  |
| |bs-flex--gap|bs-flex--gap_( S, M, L )|
| |bs-flex--col *|bs-flex--col_( 1 ~ 12 )|
| |bs-flex--(opt)|bs-flex--( center, end, between, reverse, column, middle )|
|ico|bs-ico|スプライト用にリセット、画像はimg/ico/ico_project.svg を使用|
| |bs-ico--(opt)|bs-ico--( M, L, type ) <br>サイズ指定( デフォルト16x16,M:32ｘ32,L:64ｘ64)、<br>アイコンタイプ指定詳細は別途記載||
|<b>/* Component */</b>| | |
|figure|bs-figure|  画像等(メディア)とキャプション <br> bs-figure > <br>bs-figure__img +  bs-figure__caption |
|media|bs-media| 画像等(メディア)とテキスト <br> bs-media > <br>bs-media__side +  bs-media__body  |
| |bs-media--gap| bs-media--gap_( S, M, L ) side と body の間隔を調整|
| |bs-media--(opt) *| bs-media--( column, reverse ) <br>指定のデバイスで垂直配置、上下反転|
| |bs-media__side| bs-media__side--( left, right ) 左、右に配置 |
| |bs-media__body| bs-media__body--( melt ) sideに回り込み |
|panel|bs-panel| 装飾パネル <br> bs-panel > <br>bs-panel__header + bs-panel__body|
| |bs-panel--(theme)| bs-panel--( light, gray, dark ) カラーリング|
| |bs-panel--(opt)| bs-panel--( round ) 丸角|
| |bs-panel__header| bs-panel__header--( separator ) <br>header と body の間にボーダーを追加 |

### Device Break Point
	ex.) bs-font@Tablet_S 、 bs-flex@Sp--col_1

|class|range|description|
|-----|-----:|-----------|
|(class)@Tablet-lte| 0 ~ 800| max-width: 800px |
|(class)@Tablet|  668 ~ 800 | min-width: 668px and max-width: 800px |
|(class)@Sp| 0 ~ 667| max-width: 667px |
|(class)@SpLand|481 ~ 667| min-width:481 and max-width: 667px|
|(class)@SpPort|0 ~ 480| max-width: 480px /
    
  
---  

## Project Style Class ( project.css, prefix : pj- )

project.cssは制作するページによって要素が異なるので
『 pj- 』を付ける以外は厳格なルールはありません。  
決まった要素には予め用意してあるのでそれを使うほうが好ましい程度です。

|type|class|description|
|-----|-----------|----|
|page|pj-page|ページ全体|
| |pj-page__inner|ページ幅|
| |pj-page__spencer|pj-page__spencer_( S, M, L ) 縦の間隔|
|area|pj-header|ページヘッダー|
| |pj-content|ページコンテンツ|
| |pj-main|メインコンテンツ|
| |pj-second|セカンドコンテンツ|
| |pj-footer|ページフッター|
| |pj-siteID|サイト識別( site identification )、サイトロゴ|
| |pj-copyright|コピーライト|
| |pj-article|記事|
| |pj-section|章、節|
|navigation|pj-globalNav|グローバルナビゲーション|
| |pj-localNav|ローカルナビゲーション|
| |pj-footerNav|フッターナビゲーション|
| |pj-siteMapNav|サイトマップナビゲーション|
| |pj-assistNav|アシストナビゲーション|
| |pj-pagePathNav|ページパスナビゲーション(パンくずナビ)|
| |pj-toPageTop|ページ先頭へのボタンまたはリンク|


#### Component Style Class Example

##### Area

	div.pj-[area]
		div.pj-[area]__innder *
			div.pj-[area]__header
				h2.pj-[area]__title
			div.pj-[area]__body
			div.pj-[area]__footer

<b>*</b> はデザインによって省略します。 

##### Navigation

	nav.pj-[nav]
		div.pj-[nav]__innder *
			div.pj-[nav]__header *
				h2.pj-[nav]__title
			ul.pj-[nav]__list
				li.pj-[nav]__item
					a.pj-[nav]__btn
						span.pj-[nav]__name
    
<b>*</b> はデザインによって省略します。 
    