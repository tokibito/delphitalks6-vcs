==========================
バージョン管理システムの話
==========================

.. contents:: 目次
   :local:

バージョン管理システムとは
==========================

バージョン管理システム(以降VCS)とは、ファイルやディレクトリの変更履歴を管理するシステムです。

簡単に言うとファイルのバックアップツールです。

VCSの種類
=========

* Subversion(SVN)
* Git
* Mercurial
* Bazaar
* CVS
* Perforce
* Version Cue
* Visual SourceSafe(VSS)

他にもいくつか(いっぱい?)あります。

種類分け
========

* 中央リポジトリ or 分散リポジトリ
* ファイル単位 or チェンジセット単位

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

ツール
======

* TortoiseSVN
* TortoiseHg
* SourceTree
