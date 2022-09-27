
<header>
  <div id="title">Jenkins Design Documents</div>
  <div id="document_info">
    <div id="document_id">ID-JDD-<div id="version">00-a</div></div>
    <div id="copyright">COPYRIGHT</div>
  </div>
</header>

<aside id="toolbox"><h3><label for="toc-toggle" id="toc-toggle-label">&gt;</label></h3></aside><input type="checkbox" id="toc-toggle"><div id="main-container">
<main>

# 1. Overview

Jenkins実行環境及びジョブに関するドキュメントです。

# 2. System configuration


# 3. Pipeline

## 3.1. E2S4K

Excel to SVG for KANBAN


## 3.2. E2T4P


# 4. Stage

## 4.1. Excel 2 CSV

Excelファイルの一部をcsv形式で切り抜き出力します。

### Limitation

- [x] Desktop user
- [x] Workspace

### 4.1.1. Sequence

```plantuml
autoactivate on
skinparam monochrome true

actor User
control "Job\nWorkspace" as Job
Entity Artifact

User -> Job : build with parameter
Job -> Job : Clean workspace
return
Job ->  Artifact : Copy: schedule.csv



```



Excel Gantt2PUML and upload to Confluence


```plantuml
autoactivate on
skinparam monochrome true

actor user

user -> this : \

this -> Excel2Csv
return csv


```


`var moge = 100;`です。

- [ ] タスク1
- [x] タスク2

## 4.2. Parameter rule

## 4.3. Stages

### 4.3.1. Excel2Csv

#### 4.3.1.1. Description



#### 4.3.1.2. 2.2.1 Parameter

##### 4.3.1.2.1. pString_importFileName

**aa**

<caption>HTMLの要素</caption>

| Name                    | Init         | Description                              |
| :---------------------- | :----------- | :--------------------------------------- |
| pString_importFileName  | None         | CSVに変換するExcelファイル名             |
| pString_importSheetName | None         | CSVに変換するExcelシート名               |
| pString_exportFileName  | None         | CSV出力するファイル名                    |
| pFile_convertionRule    | default.json | 詳細な変換ルールが記載されたjsonファイル |

## 4.4. Parameter rule

## 4.5. Stages

### 4.5.1. Excel2Csv

#### 4.5.1.1. Parameter

##### 4.5.1.1.1. pString_importFileName

## 4.6. Parameter rule

## 4.7. Stages

### 4.7.1. Excel2Csv

#### 4.7.1.1. Parameter

##### 4.7.1.1.1. pString_importFileName

## 4.8. Parameter rule

## 4.9. Stages

### 4.9.1. Excel2Csv

#### 4.9.1.1. Parameter

##### 4.9.1.1.1. pString_importFileName

## 4.10. Parameter rule

## 4.11. Stages

### 4.11.1. Excel2Csv

#### 4.11.1.1. Parameter

##### 4.11.1.1.1. pString_importFileName

## 4.12. Parameter rule

## 4.13. Stages

### 4.13.1. Excel2Csv

#### 4.13.1.1. Parameter

##### 4.13.1.1.1. pString_importFileName

## 4.14. Parameter rule

## 4.15. Stages

### 4.15.1. Excel2Csv

#### 4.15.1.1. Parameter

##### 4.15.1.1.1. pString_importFileNamedssssssssssssssssssssssssssssssssssss

</main>

<aside id="toc">

- [1. Overview](#1-overview)
- [2. System configuration](#2-system-configuration)
- [3. Pipeline](#3-pipeline)
  - [3.1. E2S4K](#31-e2s4k)
  - [3.2. E2T4P](#32-e2t4p)
- [4. Stage](#4-stage)
  - [4.1. Excel 2 CSV](#41-excel-2-csv)
    - [Limitation](#limitation)
    - [4.1.1. Sequence](#411-sequence)
  - [4.2. Parameter rule](#42-parameter-rule)
  - [4.3. Stages](#43-stages)
    - [4.3.1. Excel2Csv](#431-excel2csv)
      - [4.3.1.1. Description](#4311-description)
      - [4.3.1.2. 2.2.1 Parameter](#4312-221-parameter)
        - [4.3.1.2.1. pString_importFileName](#43121-pstring_importfilename)
  - [4.4. Parameter rule](#44-parameter-rule)
  - [4.5. Stages](#45-stages)
    - [4.5.1. Excel2Csv](#451-excel2csv)
      - [4.5.1.1. Parameter](#4511-parameter)
        - [4.5.1.1.1. pString_importFileName](#45111-pstring_importfilename)
  - [4.6. Parameter rule](#46-parameter-rule)
  - [4.7. Stages](#47-stages)
    - [4.7.1. Excel2Csv](#471-excel2csv)
      - [4.7.1.1. Parameter](#4711-parameter)
        - [4.7.1.1.1. pString_importFileName](#47111-pstring_importfilename)
  - [4.8. Parameter rule](#48-parameter-rule)
  - [4.9. Stages](#49-stages)
    - [4.9.1. Excel2Csv](#491-excel2csv)
      - [4.9.1.1. Parameter](#4911-parameter)
        - [4.9.1.1.1. pString_importFileName](#49111-pstring_importfilename)
  - [4.10. Parameter rule](#410-parameter-rule)
  - [4.11. Stages](#411-stages)
    - [4.11.1. Excel2Csv](#4111-excel2csv)
      - [4.11.1.1. Parameter](#41111-parameter)
        - [4.11.1.1.1. pString_importFileName](#411111-pstring_importfilename)
  - [4.12. Parameter rule](#412-parameter-rule)
  - [4.13. Stages](#413-stages)
    - [4.13.1. Excel2Csv](#4131-excel2csv)
      - [4.13.1.1. Parameter](#41311-parameter)
        - [4.13.1.1.1. pString_importFileName](#413111-pstring_importfilename)
  - [4.14. Parameter rule](#414-parameter-rule)
  - [4.15. Stages](#415-stages)
    - [4.15.1. Excel2Csv](#4151-excel2csv)
      - [4.15.1.1. Parameter](#41511-parameter)
        - [4.15.1.1.1. pString_importFileNamedssssssssssssssssssssssssssssssssssss](#415111-pstring_importfilenamedssssssssssssssssssssssssssssssssssss)

</aside>
</div>

<style>
 :root{ --header_height:50px; --aside_toolbox_width:55px; --toolbox_item_size:45px; --toc_width:250px; }body {all:initial !important;} .markdown-preview { all:initial !important; } header { position:fixed !important; height:var(--header_height); width:100%; z-index:3000; top:0px; left:0px; background-color:white; border-bottom: 1px solid gray; box-sizing: border-box; } #toolbox { width: var(--aside_toolbox_width); height:calc(100% - var(--header_height)); position:fixed !important; left:0px; top:var(--header_height); z-index:1000; border-right: 1px solid darkgray; box-sizing: border-box; background-color:#fcfcfc; } #toc-toggle-label{ display: block; width: var(--toolbox_item_size); height: var(--toolbox_item_size); margin-left:5px; text-align: center; text-decoration: none; font-size: var(--toolbox_item_size); background-color: darkgray; border: 1px solid slategray; color: #fff; box-sizing: border-box; border-radius: 10%; font-family: Arial;} #toc-toggle{ display: none; } #main-container{ position:fixed; left: var(--aside_toolbox_width); top : var(--header_height); width:calc(100% - var(--aside_toolbox_width)); overflow:scroll; height:calc(100% - var(--header_height));} #toc-toggle+#main-container { display: grid; grid-template-areas: 'main'; grid-template-columns: 1fr; } #toc-toggle:checked+#main-container { display: grid; grid-template-areas: 'aside main'; grid-template-columns: var(--toc_width) 1fr; } #main-container aside { grid-area: aside; position: fixed; left:0px; top:0px; height: calc(100% - var(--header_height)); overflow: scroll; z-index:100; margin:0px;} #toc-toggle+#main-container aside { display: none } #toc-toggle:checked+#main-container aside { display: block; width: var(--toc_width); left:var(--aside_toolbox_width); top:var(--header_height)} main { grid-area: main; padding-left:1em; width: calc(100% - var(--aside_toolbox_width));} aside ol, aside ul, li {list-style-type: none !important; padding-left:0.2em !important; } #title { padding-left:0.5em; font-size:20px; font-weight:bold; } #document_info{ display:block; position:fixed; top:0.5em; right:1em; font-weight:bold; color:darkgray; font-size:14px; text-align:right;} #document_id::before{content:"DOCUMENT ID: "} #version{ display:inline;  }
</style>