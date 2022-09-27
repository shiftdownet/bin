---
html:
  embed_local_images: true
  embed_svg: true
  offline: true
  toc: true

print_background: false
export_on_save:
  html: true
---
<!----------------------------------------------------------------------------
 #
 # Document information: Definitionセクションのmetaデータを参照のこと。
 # 
 # Template info:
 #      Template ID     : G-DOC-CMN-Beta
 #      Template Version: Beta
 #      Last updated    : 2022-09-27
 #      Created by      : H.Nakayama
 #      Requirements:
 #          Editor:
 #              VSCode 1.68.0
 #          HTML viewer:
 #              Chrome 105.0.5195.127
 #          Generation environment for HTML:
 #              VSCode Add-in Markdown PDF v1.4.4
 #                  Settings:
 #                  [x] Plantuml Open Marker : ```plantuml
 #                  [x] Plantuml Close Marker : ```
 #                  [x] Type : html
 #                  [x] Convert on save
 #          Preview environment:
 #              VSCode Add-in Markdown Preview Enhanced v0.6.3
 #                  Settings:
 #                  [x] Enable Script Execution
 #              Graphviz Version.
 #              Java 17 LTS
 #          Other Add-ins
 #              Markdown All in One : TOC creation/updating
 #              markdownlint        : Syntax check
 #
 #---------------------------------------------------------------------------->
<!----------------------------------------------------------------------------
 # Section    : Definition
 # Description: meta内で定義した値を文書内で{meta.定義名}の形で参照可能です。
 #---------------------------------------------------------------------------->
<script>
const meta = {
    documentName: "Document Name",          // 文書名
    documentID:"documentID",                // 文書ID
    version: "00-a",                        // バージョン
    system: "System",                       // システム
    vehicle: "Vehicle",                     // 車両
    customer: "Customer",                   // 顧客
    asil: "QM",                             // ASIL
    issued: "issued"                        // 版権
};
</script>

<!----------------------------------------------------------------------------
 # Section    : Sidebar
 # Description: Expandableなサイドバーを描画します。変更不要です。
 #---------------------------------------------------------------------------->
<aside id="toolbox"><label for="toc-toggle" id="toc-toggle-label">&gt;</label></aside><input type="checkbox" id="toc-toggle"><div id="main-container">

<!----------------------------------------------------------------------------
 # Section    : main
 # Description: 文書化したい内容を記述する領域です。
 #---------------------------------------------------------------------------->
<main id="main">

# 1. Document information
Document Name
: {meta.documentName}

Document ID
: {meta.documentID}

Version
: {meta.version}

System
: {meta.system}

Vehicle
: {meta.vehicle}

Customer
: {meta.customer}

ASIL
: {meta.asil}

Issued by
: {meta.issued}


```gnuplot {cmd=true output="html"}
set terminal svg
set title "Simple Plots" font ",20"
set key left box
set samples 50
set style data points

plot [-10:10] sin(x),atan(x),cos(atan(x))
```

# 2. Introduction

<!-- @import "./sample.csv" -->

@import "./sample.csv"


*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
The HTML specification
is maintained by the W3C.

H~2~O

!!! note This is the admonition title
    This is the admonition body



## 2.1. Purpose

## 2.2. Scope

## 2.3. Reference

## 2.4. Term definition

用語
: 説明

# 3. Hardware-Software Inteface

| left | center | right |
| :--- | :----: | ----: |
| <--  |  >--<  |   --> |

Table: キャプション

# 4. Safety-Requirements


# 5. 

aaaaaa


</main>


<!----------------------------------------------------------------------------
 # Section    : toc
 # Description: 目次です。'Markdown All in one:Update table of content'で更新してください。
 #---------------------------------------------------------------------------->
<aside id="toc">


<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [1. Document information](#1-document-information)
- [2. Introduction](#2-introduction)
  - [2.1. Purpose](#21-purpose)
  - [2.2. Scope](#22-scope)
  - [2.3. Reference](#23-reference)
  - [2.4. Term definition](#24-term-definition)
- [3. Hardware-Software Inteface](#3-hardware-software-inteface)
- [4. Safety-Requirements](#4-safety-requirements)
- [5.](#5)

<!-- /code_chunk_output -->

</aside>
</div>

<!----------------------------------------------------------------------------
 # Section    : Header
 # Description: 変更不要です。
 #---------------------------------------------------------------------------->
<header id="header"><div id="title">{meta.documentName}</div><div id="document_info"><div id="document_id">{meta.documentID}-{meta.version}</div><div id="version">{meta.version}</div></div></header>

<!----------------------------------------------------------------------------
 # Section    : Footer
 # Description: 変更不要です。
 #---------------------------------------------------------------------------->
<footer id="footer">- {meta.issued} -</footer>

<!----------------------------------------------------------------------------
 # Section    : Style + Javascript
 # Description: 変更不要です。
 #---------------------------------------------------------------------------->
<style> :root{ --header_height:50px; --footer_height:25px;--aside_toolbox_width:55px; --toolbox_item_size:45px; --toc_width:250px; }body {all:initial !important;} .markdown-preview { all:initial !important; } header { position:fixed !important; height:var(--header_height); width:100%; z-index:3000; top:0px; left:0px; background-color:white; border-bottom: 1px solid gray; box-sizing: border-box; } #toolbox { width: var(--aside_toolbox_width); height:calc(100% - var(--header_height) - var(--footer_height)); position:fixed !important; left:0px; top:var(--header_height); z-index:1000; border-right: 1px solid darkgray; box-sizing: border-box; background-color:#fcfcfc; } #toc-toggle-label{ display: block; width: var(--toolbox_item_size); height: var(--toolbox_item_size); margin-left:5px; margin-top:5px; text-align: center; text-decoration: none; font-size: var(--toolbox_item_size); background-color: darkgray; border: 1px solid slategray; color: #fff; box-sizing: border-box; border-radius: 10%; font-family: Arial;} #toc-toggle{ display: none; } #main-container{ position:fixed; left: var(--aside_toolbox_width); top : var(--header_height); width:calc(100% - var(--aside_toolbox_width)); overflow:scroll; height:calc(100% - var(--header_height) - var(--footer_height));} #toc-toggle+#main-container { display: grid; grid-template-areas: 'aside main'; grid-template-columns: 0fr 1fr; } #toc-toggle:checked+#main-container { display: grid; grid-template-areas: 'aside main'; grid-template-columns: var(--toc_width) 1fr; } #main-container aside { grid-area: aside; position: fixed; left:0px; top:0px; height: calc(100% - var(--header_height) - var(--footer_height)); overflow: scroll; z-index:100; margin:0px;} #toc-toggle+#main-container aside { display: none } #toc-toggle:checked+#main-container aside { display: block; width: var(--toc_width); left:var(--aside_toolbox_width); top:var(--header_height)} main { grid-area: main; padding-left:1em; width: calc(100% - var(--aside_toolbox_width));} aside ol, aside ul, li {list-style-type: none !important; padding-left:0.2em !important; } #title { padding-left:0.5em; font-size:20px; font-weight:bold; } #document_info{ display:block; position:fixed; top:0.5em; right:1em; font-weight:bold; color:darkgray; font-size:14px; text-align:right;} #document_id::before{content:"DOCUMENT ID: "} #version{ display:inline; } #version::before{content:"VERSION: "} footer { position:fixed; bottom:0px; ;eft:0px; width:100%; height:var(--footer_height); z-index:3500; background-color:white; border-top: 1px solid slategray; text-align:center; font-size:15px; color:#333;}</style>
<script>Object.keys(meta).forEach(function (key) {});</script>

<!----------------------------------------------------------------------------
 # EOF
 #---------------------------------------------------------------------------->
