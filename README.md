# nginx
nginxのシェルスクリプト置き場、CentOS7専用となります。**centos7 minimal インストール** した状態で何もはいっていない状態で必要なファイルを実行してください

※自己責任で実行してください

## テスト環境
### conohaのVPS
* メモリ：512MB
* CPU：1コア
* SSD：20GB

### さくらのVPS
* メモリ：512MB
* CPU：1コア
* SSD：20GB

### さくらのクラウド
* メモリ：1GB
* CPU：1コア
* SSD：20GB

### IDCFクラウド
* メモリ：1GB
* CPU：1コア
* SSD：20GB

### Microsoft Azure
* メモリ：2GB
* CPU：1コア
* SSD：15GB

### 実行方法
SFTPなどでアップロードをして、rootユーザーもしくはsudo権限で実行
wgetを使用する場合は[環境構築スクリプトを公開してます](https://www.logw.jp/cloudserver/8886.html)を閲覧してください。
wgetがない場合は **yum -y install wget** でインストールしてください

**sh ファイル名.sh** ←同じ階層にある場合

**sh /home/ユーザー名/ファイル名.sh** ユーザー階層にある場合（rootユーザー実行時）

## 共通内容
* epelインストール
* gitのインストール
* システム更新
* mod_sslのインストール
* firewallのポート許可(80番、443番)
* gzip圧縮の設定
* centosユーザーの作成

**centosユーザーのパスワードはランダム生成になります。構築完了後にパスワードが表示されるのでメモするか、rootで変更してください** centosユーザーで作成、アップロードするファイルは **644** 、ディレクトリは **775** となります

## [nginx.sh](https://github.com/site-lab/apache/blob/master/nginx.sh)
### 実行内容
* nginxのインストール

## [nginx_php.sh](https://github.com/site-lab/apache/blob/master/nginx_php.sh)
### 実行内容
* nginxのインストール
* PHP7.2 or 7.3を選択してインストール


## [nginx_apache.sh](https://github.com/site-lab/apache/blob/master/nginx_apache.sh)
### 実行内容
* nginxのインストール
* apache2.4.6のインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）
* リバースプロキシ設定済み




## [nginx_php73.sh](https://github.com/site-lab/apache/blob/master/nginx_php73.sh)
### 実行内容
* nginxのインストール
* php7.3のインストール
* php7.3の必要モジュールインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

PHP7は **FastCGI版** となります。
データベースは自分でインストールしていただく形になります。データベースも含めてインストールしたい場合は[LAMP](https://github.com/site-lab/lamp)リポジトリからインストールしてください。

## [nginx_php73_socket.sh](https://github.com/site-lab/apache/blob/master/nginx_php73_socket.sh)
### 実行内容
* nginxのインストール
* php7.3のインストール
* php7.3の必要モジュールインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

PHP7は **FastCGI版** となります。
データベースは自分でインストールしていただく形になります。データベースも含めてインストールしたい場合は[LAMP](https://github.com/site-lab/lamp)リポジトリからインストールしてください。

## [nginx_php74.sh](https://github.com/site-lab/apache/blob/master/nginx_php74.sh)
### 実行内容
* nginxのインストール
* php7.4のインストール
* php7.4の必要モジュールインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

PHP7は **FastCGI版** となります。
データベースは自分でインストールしていただく形になります。データベースも含めてインストールしたい場合は[LAMP](https://github.com/site-lab/lamp)リポジトリからインストールしてください。

## [nginx_php74_socket.sh](https://github.com/site-lab/apache/blob/master/nginx_php74_socket.sh)
### 実行内容
* nginxのインストール
* php7.4のインストール
* php7.4の必要モジュールインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

PHP7は **FastCGI版** となります。
データベースは自分でインストールしていただく形になります。データベースも含めてインストールしたい場合は[LAMP](https://github.com/site-lab/lamp)リポジトリからインストールしてください。


## [nginx_nodejs.sh](https://github.com/site-lab/apache/blob/master/nginx_nodejs.sh)
### 実行内容
* nginxのインストール
* node.jsのインストール
* Expressのインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

nginx+node.jsです。nginxでリバースプロキシをしてます。

## [nginx_ndenv.sh](https://github.com/site-lab/apache/blob/master/nginx_ndenv.sh)
### 実行内容
* nginxのインストール
* node.jsのインストール
* Expressのインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

nginx+node.jsです。nginxでリバースプロキシをしてます。ndenvで動かします


## [nginx_go.sh](https://github.com/site-lab/apache/blob/master/nginx_go.sh)
### 実行内容
* nginxのインストール
* go言語のインストール
* Expressのインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

nginx+go言語です。nginxでリバースプロキシをしてます。

## [nginx_goenv.sh](https://github.com/site-lab/apache/blob/master/nginx_goenv.sh)
### 実行内容
* nginxのインストール
* go言語のインストール
* Expressのインストール
* HTTPSへのリダイレクト設定可（一部ファイル編集してください）

nginx+go言語です。nginxでリバースプロキシをしてます。こっちはgoenvでバージョン管理出来るタイプとなります。


## [openlitespeed.sh](https://github.com/site-lab/webserver/blob/master/openlitespeed.sh)
### 実行内容
* openlitespeedのインストール
* 初期設定：https://www.logw.jp/cloudserver/8545.html
* openlitespeed関係の記事：https://www.logw.jp/tag/litespeed
