# 最新版のワードプレスをダウンロード
FROM wordpress:latest

# 	APTライブラリのインデックスを更新。`wget`と`unzip`を入れる。
RUN apt-get update
RUN apt-get -y --force-yes -o Dpkg::Options::="--force-confdef" install wget unzip
WORKDIR /tmp/wp-plugins

# WPCoreをzipでダウンロード
RUN wget https://downloads.wordpress.org/plugin/wpcore.zip

# zipファイルの解凍
RUN unzip './*.zip' -d /usr/src/wordpress/wp-content/plugins
RUN chown -R www-data:www-data /usr/src/wordpress/wp-content

# プラグインのダウンロード用のディレクトリを削除
RUN rm -rf '/tmp/wp-plugins'
WORKDIR /var/www/html