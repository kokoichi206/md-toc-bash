% MD-TOC(1)
% Takahiro Tominaga
% 2023年12月

# 名前

md-toc - Markdown ファイルの目次（TOC）を作成します。

# 概要

**md-toc** [オプション] [Markdown ファイルのパス]

# 説明

**md-toc** は、Markdown ファイルの目次（TOC）を生成する CLI コマンドです。
指定された Markdown ファイルを読み込み、見出しを抽出して TOC を作成し、
インデントのサイズを調整し、最小および最大の見出しレベルを指定するオプションがあります。

**-h**, **--help**
:   ヘルプメッセージを表示します。

**-s**, **--indent-size サイズ**
:   インデントのサイズを変更します（スペースを使用したインデントです）。

**-min レベル**, **--minimum レベル**
:   目次に含める最小の見出しレベルを設定します。

**-max レベル**, **--maximum レベル**
:   目次に含める最大の見出しレベルを設定します。

## 例

**Markdown ファイルの目次（TOC）を生成します。**

    $ bash md-toc.sh <ファイル名>
      * [h1-タイトル](#h1-タイトル)
        * [h2-タイトル-1](#h2-タイトル-1)
          * [スペースとは何か？](#スペースとは何か？)
    $ bash md-toc.sh --min 2 <ファイル名>
      * [h2-タイトル-1](#h2-タイトル-1)
        * [スペースとは何か？](#スペースとは何か？)

## 終了ステータス:

**0**
:   正常終了の場合

**1**
:   軽微な問題があった場合（例：パースエラーやファイルが渡されなかった場合）

# バグ

GitHub のイシューをご確認ください: https://github.com/kokoichi206/md-toc-bash/issues

# ライセンス

md-toc は MIT ライセンスの条件の下でライセンスされています。
