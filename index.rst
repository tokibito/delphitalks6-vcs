==========================
バージョン管理システムの話
==========================

.. contents:: 目次
   :local:

バージョン管理システムとは
==========================

バージョン管理システム(Version Control System、以降VCS)とは、ファイルやディレクトリの変更履歴を管理するシステムです。

簡単に言うとファイルのバックアップツールです。

共有機能を持ったものも多い。

バックアップどうしてますか
==========================

* バックアップなど存在しない
* コピー_【最新】新しいフォルダ_20130906 (2)
* フォルダやファイル名に日時の文字列を付けて管理

VCS使いましょう。

ソースコードの共有どうしてますか
================================

* 共有しない
* ファイルサーバーで共有

  * 同時に編集できない

* メディアに入れてコピー

  * 手間かかるよ

* メールで

  * でかいファイルどうすんの...

VCS使うと楽できますよ。

VCSの種類
=========

* Subversion(SVN)
* Git
* Mercurial
* Bazaar
* CVS
* Perforce
* Version Cue
* Visual SourceSafe(VSS, Team Foundation Server)

他にもいくつか(いっぱい?)あります。

種類分け
========

* 中央リポジトリ or 分散リポジトリ

  * 分散バージョン管理システム(DVCS)
  * 分散型でも共有のために中央リポジトリに相当するものを用意することが多い

* ファイル単位 or チェンジセット単位

  * チェンジセット単位が多い

日本語の扱い
============

* コメントに日本語を使えるか
* ファイル名(ファイルパス)に日本語を使えるか

.. csv-table::
   :header-rows: 1

   ソフトウェア,内部エンコード,リポジトリ
   Subversion,UTF-16,中央
   Git,OS依存,分散
   Mercurial,OS依存,分散
   Bazaar,UTF-16,分散

* 複数のOSで日本語のファイル名(ファイルパス)を扱いたいならSubversionかBazaar
* 日本語ファイルパスってそもそもトラブルの元なので避けるほうがいいかもね

ホスティングサービス
====================

.. csv-table::
   :header-rows: 1

   サービス名,運営会社,対応しているリポジトリの種類
   GitHub,GitHub,Git
   BitBucket,Atlassian,Mercurial、Git
   GoogleCode,Google,Subversion、Mercurial、Git
   SourceForge,Geeknet,CVS、Subversion、Mercurial、Git、Bazaar
   LaunchPad,Canonical,Bazaar
   CodePlex,Microsoft,Subversion、VSS、Mercurial、Git

共有方法
========

.. csv-table::
   :header-rows: 1

   ソフトウェア,方法
   Subversion,ファイルサーバーやHTTP/WebDAVでリポジトリのディレクトリを共有
   Git,OS依存,SSHやHTTPでベアーリポジトリを共有
   Mercurial,SSHやHTTPでリポジトリを共有

他にも...

* パッチを作成して共有

ツール
======

* TortoiseSVN
* TortoiseHg
* SourceTree

RadStudio統合について
=====================

* Subversionが標準で使える

  * サードパーティでMercurialのもあるけどXE4では動かず...
  * 最新のSubversionで作ったリポジトリだとエラーで読めない

TortoiseSVNを使うのが無難。

操作
====

* チェックアウト(Checkout)/クローン(Clone)
* 追加(Add)してコミット(Commit)する

  * ファイルをVCSの管理下に追加する(Add)
  * 変更をデータベースに保存する(Commit)

* Push/Pull
