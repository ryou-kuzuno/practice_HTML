
  /* ボックスの基準を相対配置にする */
    position: relative;

  /* 表示しなくする */
    display: none;

  /* 縦方向の揃え位置を中央ぞろえにする。 */
    vertical-align: middle;

  /* 親ボックスにrelativeが入っているので親ボックスの左上が基準位置。 */
  position: absolute;
  
  /* 色、画像、原点と寸法、反復方法、その他の機能など、背景に関するすべてのスタイルオプションを一括で設定 */
  background: #555;
  /* 要素を横いっぱいに広げて縦に並べる */
  display: block;
  /* 擬似要素を挿入する際に使用する */
  content: '';
  /* カーソルの形状をリンクカーソルに指定する。 */
  cursor: pointer;

  /* positionがstatic以外なので使用可能。 */
  bottom: -8px;



  /*はじめは隠しておくため*/
  display: none;
  // 画面のきまった位置に固定する
  position: fixed;
  // 0を基準としてボックスの重なりの順序を指定する
  z-index: 99;
  
  // 要素を0.0（完全に透明）～1.0（完全に不透明）の数値で指定
  opacity: 0;
  // 要素に対して移動、回転、伸縮、傾斜の変形を加えることができます。
  transition: .3s ease-in-out;



  // はみ出た部分の表示の仕方をユーザーエージェントに依存する。
  overflow: auto;
 