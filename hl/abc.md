---
# Setting for Markdown Preview Enhanced v0.6.3
toc:                        # 目次設定
  depth_from: 1             # - 目次化する開始ネスト
  depth_to: 4               # - 目次化する終了ネスト
  ordered: false            # - オーダーを表示しない
html:                       # HTMLファイル出力に関する設定
  embed_local_images: true  # - ローカル埋め込み画像ファイルを有効にする
  embed_svg: true           # - SVGの埋め込みを有効にする
  offline: true             # - offlineでの生成を有効にする
  toc: true                 # - デフォルトでサイドバーにTOCを表示する
export_on_save:             # ファイル保存時の振る舞い
  html: true                # - htmlで出力(※Markdown PDF等他のAddinの自動保存機能は無効化してください)
---

@import "csv2.csv"

@import "csv1.csv"

[ABC]
[EDF]

@import "filepath.md"


<header id="header"><div id="title">{meta.documentName}</div><div id="document_info"><div id="document_id">{meta.documentID}-{meta.version}</div><div id="version">{meta.version}</div></div></header>
<footer id="footer">- {meta.issued} - CONFIDENTIAL</footer>
<style> header { position:fixed !important; height: 60px; width:100%; z-index:3000; top: 0px; left:0px; background-color: rgba(255,255,255,0.8); border-bottom: 1px solid gray !important; box-sizing: border-box;} #title { padding-left:0.5em; font-size:20px; font-weight:bold; } #document_info { display:block; position:fixed; top:0.5em; right:1em; font-weight:bold; color:#666, font-size:14px; text-align:right;} #document_id::before {content:"DOCUMENT ID: "} #version { display:inline;} #version::before { content: "VERSION: "} footer { position:fixed !important; bottom:0px; left:0px; width:100%; height:20px; z-index:3500; background-color:white; border-top: 1px solid slategray; text-align:center; font-size:15px; color:#333; font-weight:bold; } .md-sidebar-toc{ top:60px !important; height: calc(100% - 60px - 20px) !important; overflow:scroll !important; white-space:nowrap; font-size:12px !important; } .markdown-preview { margin:0 !important; padding: 1em 1em 1em 1em !important; position:fixed !important; top:60px !important; height:calc(100% - 60px) !important; overflow:scroll !important;} html body[for="html-export"]:not([data-presentation-mode]):not([html-show-sidebar-toc]) .markdown-preview{left:0% !important; transform: initial !important;} .md-sidebar-toc::-webkit-scrollbar { height:8px !important; } #sidebar-toc-btn { bottom:0px !important; top:60px;} h1, h2, h3, h4, h5, h6 { border-bottom: solid 2px #333 !important; font-weight:bold; margin:2em 0em 0em 0em !important; } h1 + h2 { page-break-before:auto; margin-top : 0.5em !important; } h2 + h3 { page-break-before: auto; margin-top: 0.5em !important; } h3 + h4 { page-break-before: auto; margin-top: 0.5em !important; }  h3 + h4 { page-break-before: auto; margin-top: 0.5em !important; }  h4 + h5 { page-break-before: auto; margin-top: 0.5em !important; }  h5 + h6 { page-break-before: auto; margin-top: 0.5em !important; } h1,h2,h3{ font-size:24px !important;} h4,h5,h6 { font-size:22px !important; } .column-left{ float: left; width: calc(50% - 10px); text-align: left;} .column-right{ float: right; width: calc(50% - 10px);text-align: left;}  .three-column{ float: left; width: calc(33% - 15px); text-align: left; margin-left: 10px;} .clearfix::after{ content: ""; clear: both; display: block; } pre, code, var, samp, kbd, .mono { font-family: 'ＭＳ ゴシック', Consolas, 'Courier New', Courier, Monaco, monospace !important; line-height: 1.2 !important;}
.active {
    background-color: #ffffaa;
}
</style>

<script src="http://code.jquery.com/jquery-2.1.4.min.js"></script>
<script type="text/javascript">
prevAnchor = ""
$(document).ready(function(){
    $(document).on('click','a', function () {
      if ( prevAnchor != "") {
          $(prevAnchor).removeClass('active');
      }
      anchor = $(this).attr('href')
      $(anchor).addClass('active');
      $(anchor).fadeOut(500,function(){$(this).fadeIn(500)});
      setInterval(function(){
          $(anchor).fadeOut(500,function(){$(this).fadeIn(500)});
      },1000);
      prevAnchor = anchor
    });
});
</script>
