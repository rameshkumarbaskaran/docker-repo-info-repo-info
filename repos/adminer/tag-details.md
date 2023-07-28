<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4`](#adminer4)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:4.8.1`](#adminer481)
-	[`adminer:4.8.1-fastcgi`](#adminer481-fastcgi)
-	[`adminer:4.8.1-standalone`](#adminer481-standalone)
-	[`adminer:fastcgi`](#adminerfastcgi)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:standalone`](#adminerstandalone)

## `adminer:4`

```console
$ docker pull adminer@sha256:18609aac77637e99fbbdfbe2de4f3837bf4b835c30b4c84fdb593d90d24349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:4` - linux; amd64

```console
$ docker pull adminer@sha256:0174c52770125d4206b808412926458b544758845f8f552151f97cb33881ca32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad39a6f503c44bda7082754111a22a9ba05f764a759d3d3ada7b444a55bc12`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:15 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:26 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 03:26:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7a59571f85d61c32167207b31048b15456dbc4c07560c912b86f1ceef081c`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530e7e02f75518fdf62aa976f5ec67a1c0c66451e5de48963221ec07b0143bfd`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee8734c62c40d287661833cf8774b85007370efb9f23c1dc52a0983bb2efa1`  
		Last Modified: Tue, 04 Jul 2023 03:26:59 GMT  
		Size: 1.4 MB (1385432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a0cc37cf2cace649b536ffa14618f5b2f9d1e641feeee7a449e94c0c188f5`  
		Last Modified: Tue, 04 Jul 2023 03:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v5

```console
$ docker pull adminer@sha256:962e9bfdfa21d1e9af480c715cb14c0200637a4304b6969013d9aa9dffdd9b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91194385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145a48b09f292be73dfc37cb3141ac089a668515d7448662a553615c95e55e0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:19 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:32:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9237d1e17acadb8c10dd17f8d666ccd1c9343514a18589a12a5d6bfa7eff40`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18540feda134b6545df8efa09e435f8f79fb7828703c8f0cd6fa986ce96f5295`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ddef2f8502b3232c3215f41c96321944ab58eb1efd0dd0da8359d91f43371`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.4 MB (1385375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a79a4cff669839273b8b81cf6a0fc9582dece1dcbd47b2d4ad47b829cfee1b0`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a05d314c7de66c8cb10b085543a98e4278d271893be05d73b7f28515f74854f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fe9ea70e4697d5a79eaaa3de540bcb6ab33331b23b134e3e83a5e80102c84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:22 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:48:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450f098fa03bb8ec8464823656b3438895417c4ff68e7cb817bf81d92428835e`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243bba61a9bf6f71050b509f6d32f150733d079d88f05e3baf5257037291d52`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ca2f56cb674dfee1f52c140d8d2f26e0068b1f9a192518bd80245bd1dd0eb`  
		Last Modified: Tue, 04 Jul 2023 05:48:56 GMT  
		Size: 1.4 MB (1385426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5dc82712c6232409a9e98550357737eceb09e05870ea9579e6d37ff34e3094`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:958990f6d1f66e6a9f854251e04835456490db94d5049bd0781b82a4535b79b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ec1ac6b42873905c2e49fe8b847346b584a9934045a9af7c5ad3a2f4ce533`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:32:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:32:58 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:09 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:33:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805759b30cc65928f6590a87df6374385bc4ab00bac8e6c082067cad6a0c8052`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c52d243051d0380315d262f0c75865d8dbaff27d5d57b1fc3090fbb76dbf44`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b32c0aa3641a21349bda0ace8e58c088db3cbbba1a6f262ea97e74e2ecd25`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e6078a351dedfa26b1cd20ceca3b8cca8fc8e6aa765670fa373020469f9ef`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:461fd7352ea0d006503da7a92caf49bef7d68374e3a6f186026f2aac5bd316ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b840e17b2b92310ff52e92ccc4f30a308ebab1004136bbf42eba705fb9bc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:26:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:26:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:26:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:26:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:26:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96dc5d5492a6571a3974948e4374a3c5d7049b6d958aac525df2d2bbfdf627`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341dcf80f058bf05383a7b6a2df74a1d36294baebd5f5292e4fe8434091576a1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd8d1218897da786e8e717e520aa31c9c6f6db2aa9ec80af132f76deb7f67c`  
		Last Modified: Tue, 04 Jul 2023 05:27:15 GMT  
		Size: 1.4 MB (1385291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9673c67b185741461ba76717835fe0a1d76ab762d02dae5f5a28fb3a1450566b`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; mips64le

```console
$ docker pull adminer@sha256:bba236958f3ef20f85f094ef599957a623ea712aa38c6b16090a9d32b6b72d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4507a99e483cae111243d540a169beaba5b2399ae32abbc24552dcc14c06646f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:29:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:29:17 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:29:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:29:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:29:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:29:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:30:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:30:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:30:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:30:31 GMT
USER adminer
# Tue, 04 Jul 2023 14:30:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 14:30:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c7da25ad9de44c8075b26de39239e884bba5e188ad5b3c7d9d9f126ba5039`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddc446ac238027e91c76b2ed3e55af67046cf1742ec9ff8f1189b45b3226a14`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686c97d6e8dd8d071fca9724489d4b249e53a9b029354c8668871b3725e5305`  
		Last Modified: Tue, 04 Jul 2023 14:32:42 GMT  
		Size: 1.4 MB (1386278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce629354f0a6b55bc416d4b4fcbb5e8ce6a197cb5708a017936c011662d82c`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:513659a3661e42d0e40985ae242c59d5dada7938fc81cf3b033261838c8f59f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a18eba61d2a1d4913ca037b6b2fd9bd7c455f98ca723b338a5c4d3f20513`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:53:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:53:10 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:53:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:53:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:53:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:53:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:54:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:54:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:54:22 GMT
USER adminer
# Tue, 04 Jul 2023 04:54:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:54:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa56055f8b8b3c5e2190e891801d2cd8e63265e487d2065cc972d9b12531c71`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18434fa3f232269e2dea15e4eef30f28360ba63d46add5fb9bdad8c361a8bc8e`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec4ed1374295eb9d7ea18c48406bea22284a8b8a24426929873ed30572209c`  
		Last Modified: Tue, 04 Jul 2023 04:55:52 GMT  
		Size: 1.4 MB (1385875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2de9446f31d2128352d88e158d78ec61f485d2fb3f4e25fe2d696a344feff9`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:faca9d7d2872d5b55b86b5075e69a84c556c930258a875e13aa3fa72ecf2b17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93697370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5204631a997d1234d7546fcb38705962f54c2530fc951f2daf73a073ad0969`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:18 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:54:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1820f29b009a397fd193ee10f17404280d3b9228f8b36daf5bb815bce0307`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a3cdb65e8cd3b2cb9e3aceddb9e95864743111dc589908c4805fca9f9bf9b8`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aee720253a711b2d402e08cb5cafdfa0cc5290a8f09f543174ff677614c67f`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.4 MB (1385448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f7c164596b5009b686a6803bc457fe549e5272341bfa787cc8f342ad43442`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:58587babe247ff692523f82309b6db1a74d57813e3503f2f6d45eb1ca788cc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:6caa807820ca7c9cdbadf1ab1d45db1bd786efc37ef5aa47cbe10708dd12d998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95935139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5a487eafbb1e1c54550a075a220d824e930146fccd78c5a4afdb74a2bc50a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 03:26:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:33 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:33 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:44 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d76a56a3771369c6e704d5e35bd1766d6e549b0d66ed49c4ad0f11e9606374f`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7ccb20f3a0eece3e90efca525e5571942cf228298324515c02198d05777cb9`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8c7d8cd6f443d542fd01782eed5dc03b0a74d0f0714683dc176561ba235edf`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db1d8f59a146868100bd71857251dc11b79dbc9b8b8cb776a4d89e05748ac88`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.4 MB (1385454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8979c84db28ce690caecdf197ecff4c3fa9fd09b8da2aed722a745e415edae28`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:000c82eff38911214c7db7c3a511c0a57cba0bda80bcf27ee035587d3eed20be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610a0bd191c5498d32fa7dcb44808b310a87072810de50eba2ae2654de87ca3c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:22 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 04:32:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:23 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:23 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:24 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:37 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:37 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75e47d8dcfa6ad8c28efd5221051c57745479e4c9be773a174ed053c964fdc`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6d17752c4fc62ce532477600101cfe5b1108020f93a8c97e4d220d8ef823ba`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b637b24bf6e78648f068b8a4683cf6f28db889ba791c3134c6524a347b7ca`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07ec511505a60a6fad31428b9d54cf218f5256afd31101c81098d87db2a5e3`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.4 MB (1385376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b106734e44f3b038b26d8a5c64f653c388d92572b121d6ce448372a7ff16c2f`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:0be94bd6202f72f371789c8c37780bf657de3d1c590e6ca57b0bfc52b20b6904
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87793947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1678a0b92255b8085e7baec25267827d874cf221fc98c542e2979a62d5def219`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 05:48:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:34 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:46 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611383b899e8a30dc5ee74865f6ad93b4b59b676b48f4c4a9fe5eb0d92d9a8a3`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e604c1e6cce082e392b473dcdc2824c86f055c7e910560c81eb54d7dbf758c`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e04bf6ee13b97e03f675aa27139cac7931f5cd1c735d6a6e078abf6ab8004`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9348a926275a93bc78151de56c3200f5f3d15827e53cd9c50db6ef4557513b6`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.4 MB (1385410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07644552098791dbe95267ac6756b65b68cdced2563aa3f7d54135b1c72de7dc`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:62a62e95e6e92f9e8510495f3cb436a6b4196b63bb07134596be3e010d33acd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94340314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164e7749682325c1aa3417dd5bdd3315167af4c5b97129e7994a12bfc9a727bc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:33:11 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 28 Jul 2023 01:33:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:33:12 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:33:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:22 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:22 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8010fea9be3a6e42dfda4398bc8dd961f3cc38cd2b066ccc38d8b83b7b0dd3e4`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7694be696a7e8c7e0ca897c46b134bd20166b15352ab0c9c130f49b4334faebc`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec715a9f3239113933f55f76bc62d32455f3b1647d2867f143645ade0de0e60`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e99cff7b42b42793347c1b48793f8d6340ba93fca1aa4a375b53344b9112c9`  
		Last Modified: Fri, 28 Jul 2023 01:33:58 GMT  
		Size: 1.4 MB (1385351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea23c2e8231c1a0717f52f8aac5318af3412ac9f3481f18bf16428f83686358`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:f28603ea4c880db60110049c6cf22720545bc6be296659ec3bb3d320c7343d55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96991589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cf9f1de498d643ae57669878101b1e59fcebf70db1074d81ceea8801ccd8f7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:49 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 05:26:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:49 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:27:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:27:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:27:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:27:02 GMT
USER adminer
# Tue, 04 Jul 2023 05:27:02 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55ca2f23f925c98c51f8a734f76590fb5f3be47a5f8dee895176e2c49ce49cf`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e6f54f2eebdc0908a5bb0ea1bf013ce274873f298ca9b3516e231f378666da`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88228cdb9c571deaf46d3473a01ca87db8a9b15747155e4fa4acb1dfd7978eb`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23222c8c9b4ecdd9417f8199b026bbfb4764f3a4b1eb9bb2e36a6fdae431afdb`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.4 MB (1385307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51719e58ff78bcdbb9022589936f75bbe7a64df0048c6777578f0f2461600a3d`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:50d0c5eb0fbb7449ac67c44dbdfc5ac9641364bd0aea37d12bf97c3d6816d8d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92616895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1386d228067b12c15d63697ae97c45005440e0d5fd512eaabf582a612a1be56`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:30:55 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 14:31:02 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:31:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:31:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:31:11 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:31:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:31:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:32:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:32:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:32:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:32:15 GMT
USER adminer
# Tue, 04 Jul 2023 14:32:18 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8538a1b8df56534e7c48884f0d1725ddebeaf72b505864e1f72ef622b38548`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b025e749cde7de1afda81b9cf371bce0015174ae81e8927c0b0d6b1ab4a8a2`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b4935cf4ff366bd19d37dd1e4355f151e7669e579994aa44b9c11eede72183`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88efd70fc04cd68535ade5181500a3f0866dc315fc4cc75ba33a82e1a50ca358`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.4 MB (1386288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8dc7d0c9faa199b112a26d67ded4852ef3a41460385ab3e0a81c1e54156877`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:9364792ada1b2eb7211f622b7a788103b4abd9fcf3b97c8768924f6e09b6690e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101260839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a36421f33b53c1c0f63f968861fd66876c3ea0c6830325f9681e900bd5d2f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:54:41 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 04:54:44 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:54:46 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:54:46 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:54:47 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:54:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:54:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:55:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:55:25 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:55:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:55:26 GMT
USER adminer
# Tue, 04 Jul 2023 04:55:27 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2011aca228bf492e49980db4d7f382fb149bfcdd0d23cb67659c0df6737226`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859d3a288f61883dc684d9157c6cd5075a0b1a74f011c4e69e987c11f886bbd7`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5d0aacdd54eb059e402c26939fdccb4fe827cc7b1fb89571221e11e2bc6e62`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c456356bca8fc124638a22b16275bb5b2ba5380b47c6af4c3cf3683ce4f8d0b5`  
		Last Modified: Tue, 04 Jul 2023 04:56:29 GMT  
		Size: 1.4 MB (1385813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dc45753ebe2ef73c8d7aece8aa163f83dfbbc85299390556dd5a5d9854b65b`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:812f84c9c8509197cf3cfd52fa7136b369eee6ec8fbf1f5d2137da850ebeb6bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93700045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8977da130ff083c95c53d0d74b0de0698be066c3800b8194112d7626900e84a0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:27 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 28 Jul 2023 01:54:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:28 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:28 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:36 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:36 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:36 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d8d234b4ce8e57ad21e2de8659dc0f24143bb0af60900bd7317781c460740b`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554328df2364098195b130e82f52a57e47ff4b781ce4c9d69810941845b904b7`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2b12034fd6588bd8a56877d9cf07d58044f91dd0f343c31876aa015a99c1cf`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154c43a8555997901e4a970eafa0c5bea898ebdf9610d3274b8bda76877115d7`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.4 MB (1385420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e715878adf9a51664bcf8f0cd897b9d823c44d90dff045eed47d17f7efa72e48`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:18609aac77637e99fbbdfbe2de4f3837bf4b835c30b4c84fdb593d90d24349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:0174c52770125d4206b808412926458b544758845f8f552151f97cb33881ca32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad39a6f503c44bda7082754111a22a9ba05f764a759d3d3ada7b444a55bc12`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:15 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:26 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 03:26:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7a59571f85d61c32167207b31048b15456dbc4c07560c912b86f1ceef081c`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530e7e02f75518fdf62aa976f5ec67a1c0c66451e5de48963221ec07b0143bfd`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee8734c62c40d287661833cf8774b85007370efb9f23c1dc52a0983bb2efa1`  
		Last Modified: Tue, 04 Jul 2023 03:26:59 GMT  
		Size: 1.4 MB (1385432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a0cc37cf2cace649b536ffa14618f5b2f9d1e641feeee7a449e94c0c188f5`  
		Last Modified: Tue, 04 Jul 2023 03:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:962e9bfdfa21d1e9af480c715cb14c0200637a4304b6969013d9aa9dffdd9b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91194385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145a48b09f292be73dfc37cb3141ac089a668515d7448662a553615c95e55e0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:19 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:32:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9237d1e17acadb8c10dd17f8d666ccd1c9343514a18589a12a5d6bfa7eff40`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18540feda134b6545df8efa09e435f8f79fb7828703c8f0cd6fa986ce96f5295`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ddef2f8502b3232c3215f41c96321944ab58eb1efd0dd0da8359d91f43371`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.4 MB (1385375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a79a4cff669839273b8b81cf6a0fc9582dece1dcbd47b2d4ad47b829cfee1b0`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a05d314c7de66c8cb10b085543a98e4278d271893be05d73b7f28515f74854f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fe9ea70e4697d5a79eaaa3de540bcb6ab33331b23b134e3e83a5e80102c84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:22 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:48:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450f098fa03bb8ec8464823656b3438895417c4ff68e7cb817bf81d92428835e`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243bba61a9bf6f71050b509f6d32f150733d079d88f05e3baf5257037291d52`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ca2f56cb674dfee1f52c140d8d2f26e0068b1f9a192518bd80245bd1dd0eb`  
		Last Modified: Tue, 04 Jul 2023 05:48:56 GMT  
		Size: 1.4 MB (1385426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5dc82712c6232409a9e98550357737eceb09e05870ea9579e6d37ff34e3094`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:958990f6d1f66e6a9f854251e04835456490db94d5049bd0781b82a4535b79b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ec1ac6b42873905c2e49fe8b847346b584a9934045a9af7c5ad3a2f4ce533`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:32:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:32:58 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:09 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:33:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805759b30cc65928f6590a87df6374385bc4ab00bac8e6c082067cad6a0c8052`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c52d243051d0380315d262f0c75865d8dbaff27d5d57b1fc3090fbb76dbf44`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b32c0aa3641a21349bda0ace8e58c088db3cbbba1a6f262ea97e74e2ecd25`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e6078a351dedfa26b1cd20ceca3b8cca8fc8e6aa765670fa373020469f9ef`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:461fd7352ea0d006503da7a92caf49bef7d68374e3a6f186026f2aac5bd316ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b840e17b2b92310ff52e92ccc4f30a308ebab1004136bbf42eba705fb9bc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:26:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:26:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:26:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:26:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:26:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96dc5d5492a6571a3974948e4374a3c5d7049b6d958aac525df2d2bbfdf627`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341dcf80f058bf05383a7b6a2df74a1d36294baebd5f5292e4fe8434091576a1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd8d1218897da786e8e717e520aa31c9c6f6db2aa9ec80af132f76deb7f67c`  
		Last Modified: Tue, 04 Jul 2023 05:27:15 GMT  
		Size: 1.4 MB (1385291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9673c67b185741461ba76717835fe0a1d76ab762d02dae5f5a28fb3a1450566b`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:bba236958f3ef20f85f094ef599957a623ea712aa38c6b16090a9d32b6b72d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4507a99e483cae111243d540a169beaba5b2399ae32abbc24552dcc14c06646f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:29:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:29:17 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:29:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:29:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:29:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:29:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:30:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:30:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:30:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:30:31 GMT
USER adminer
# Tue, 04 Jul 2023 14:30:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 14:30:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c7da25ad9de44c8075b26de39239e884bba5e188ad5b3c7d9d9f126ba5039`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddc446ac238027e91c76b2ed3e55af67046cf1742ec9ff8f1189b45b3226a14`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686c97d6e8dd8d071fca9724489d4b249e53a9b029354c8668871b3725e5305`  
		Last Modified: Tue, 04 Jul 2023 14:32:42 GMT  
		Size: 1.4 MB (1386278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce629354f0a6b55bc416d4b4fcbb5e8ce6a197cb5708a017936c011662d82c`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:513659a3661e42d0e40985ae242c59d5dada7938fc81cf3b033261838c8f59f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a18eba61d2a1d4913ca037b6b2fd9bd7c455f98ca723b338a5c4d3f20513`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:53:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:53:10 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:53:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:53:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:53:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:53:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:54:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:54:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:54:22 GMT
USER adminer
# Tue, 04 Jul 2023 04:54:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:54:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa56055f8b8b3c5e2190e891801d2cd8e63265e487d2065cc972d9b12531c71`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18434fa3f232269e2dea15e4eef30f28360ba63d46add5fb9bdad8c361a8bc8e`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec4ed1374295eb9d7ea18c48406bea22284a8b8a24426929873ed30572209c`  
		Last Modified: Tue, 04 Jul 2023 04:55:52 GMT  
		Size: 1.4 MB (1385875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2de9446f31d2128352d88e158d78ec61f485d2fb3f4e25fe2d696a344feff9`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:faca9d7d2872d5b55b86b5075e69a84c556c930258a875e13aa3fa72ecf2b17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93697370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5204631a997d1234d7546fcb38705962f54c2530fc951f2daf73a073ad0969`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:18 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:54:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1820f29b009a397fd193ee10f17404280d3b9228f8b36daf5bb815bce0307`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a3cdb65e8cd3b2cb9e3aceddb9e95864743111dc589908c4805fca9f9bf9b8`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aee720253a711b2d402e08cb5cafdfa0cc5290a8f09f543174ff677614c67f`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.4 MB (1385448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f7c164596b5009b686a6803bc457fe549e5272341bfa787cc8f342ad43442`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1`

```console
$ docker pull adminer@sha256:18609aac77637e99fbbdfbe2de4f3837bf4b835c30b4c84fdb593d90d24349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:4.8.1` - linux; amd64

```console
$ docker pull adminer@sha256:0174c52770125d4206b808412926458b544758845f8f552151f97cb33881ca32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad39a6f503c44bda7082754111a22a9ba05f764a759d3d3ada7b444a55bc12`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:15 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:26 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 03:26:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7a59571f85d61c32167207b31048b15456dbc4c07560c912b86f1ceef081c`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530e7e02f75518fdf62aa976f5ec67a1c0c66451e5de48963221ec07b0143bfd`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee8734c62c40d287661833cf8774b85007370efb9f23c1dc52a0983bb2efa1`  
		Last Modified: Tue, 04 Jul 2023 03:26:59 GMT  
		Size: 1.4 MB (1385432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a0cc37cf2cace649b536ffa14618f5b2f9d1e641feeee7a449e94c0c188f5`  
		Last Modified: Tue, 04 Jul 2023 03:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v5

```console
$ docker pull adminer@sha256:962e9bfdfa21d1e9af480c715cb14c0200637a4304b6969013d9aa9dffdd9b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91194385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145a48b09f292be73dfc37cb3141ac089a668515d7448662a553615c95e55e0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:19 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:32:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9237d1e17acadb8c10dd17f8d666ccd1c9343514a18589a12a5d6bfa7eff40`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18540feda134b6545df8efa09e435f8f79fb7828703c8f0cd6fa986ce96f5295`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ddef2f8502b3232c3215f41c96321944ab58eb1efd0dd0da8359d91f43371`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.4 MB (1385375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a79a4cff669839273b8b81cf6a0fc9582dece1dcbd47b2d4ad47b829cfee1b0`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a05d314c7de66c8cb10b085543a98e4278d271893be05d73b7f28515f74854f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fe9ea70e4697d5a79eaaa3de540bcb6ab33331b23b134e3e83a5e80102c84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:22 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:48:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450f098fa03bb8ec8464823656b3438895417c4ff68e7cb817bf81d92428835e`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243bba61a9bf6f71050b509f6d32f150733d079d88f05e3baf5257037291d52`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ca2f56cb674dfee1f52c140d8d2f26e0068b1f9a192518bd80245bd1dd0eb`  
		Last Modified: Tue, 04 Jul 2023 05:48:56 GMT  
		Size: 1.4 MB (1385426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5dc82712c6232409a9e98550357737eceb09e05870ea9579e6d37ff34e3094`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:958990f6d1f66e6a9f854251e04835456490db94d5049bd0781b82a4535b79b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ec1ac6b42873905c2e49fe8b847346b584a9934045a9af7c5ad3a2f4ce533`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:32:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:32:58 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:09 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:33:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805759b30cc65928f6590a87df6374385bc4ab00bac8e6c082067cad6a0c8052`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c52d243051d0380315d262f0c75865d8dbaff27d5d57b1fc3090fbb76dbf44`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b32c0aa3641a21349bda0ace8e58c088db3cbbba1a6f262ea97e74e2ecd25`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e6078a351dedfa26b1cd20ceca3b8cca8fc8e6aa765670fa373020469f9ef`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; 386

```console
$ docker pull adminer@sha256:461fd7352ea0d006503da7a92caf49bef7d68374e3a6f186026f2aac5bd316ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b840e17b2b92310ff52e92ccc4f30a308ebab1004136bbf42eba705fb9bc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:26:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:26:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:26:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:26:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:26:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96dc5d5492a6571a3974948e4374a3c5d7049b6d958aac525df2d2bbfdf627`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341dcf80f058bf05383a7b6a2df74a1d36294baebd5f5292e4fe8434091576a1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd8d1218897da786e8e717e520aa31c9c6f6db2aa9ec80af132f76deb7f67c`  
		Last Modified: Tue, 04 Jul 2023 05:27:15 GMT  
		Size: 1.4 MB (1385291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9673c67b185741461ba76717835fe0a1d76ab762d02dae5f5a28fb3a1450566b`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; mips64le

```console
$ docker pull adminer@sha256:bba236958f3ef20f85f094ef599957a623ea712aa38c6b16090a9d32b6b72d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4507a99e483cae111243d540a169beaba5b2399ae32abbc24552dcc14c06646f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:29:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:29:17 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:29:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:29:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:29:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:29:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:30:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:30:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:30:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:30:31 GMT
USER adminer
# Tue, 04 Jul 2023 14:30:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 14:30:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c7da25ad9de44c8075b26de39239e884bba5e188ad5b3c7d9d9f126ba5039`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddc446ac238027e91c76b2ed3e55af67046cf1742ec9ff8f1189b45b3226a14`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686c97d6e8dd8d071fca9724489d4b249e53a9b029354c8668871b3725e5305`  
		Last Modified: Tue, 04 Jul 2023 14:32:42 GMT  
		Size: 1.4 MB (1386278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce629354f0a6b55bc416d4b4fcbb5e8ce6a197cb5708a017936c011662d82c`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; ppc64le

```console
$ docker pull adminer@sha256:513659a3661e42d0e40985ae242c59d5dada7938fc81cf3b033261838c8f59f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a18eba61d2a1d4913ca037b6b2fd9bd7c455f98ca723b338a5c4d3f20513`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:53:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:53:10 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:53:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:53:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:53:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:53:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:54:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:54:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:54:22 GMT
USER adminer
# Tue, 04 Jul 2023 04:54:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:54:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa56055f8b8b3c5e2190e891801d2cd8e63265e487d2065cc972d9b12531c71`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18434fa3f232269e2dea15e4eef30f28360ba63d46add5fb9bdad8c361a8bc8e`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec4ed1374295eb9d7ea18c48406bea22284a8b8a24426929873ed30572209c`  
		Last Modified: Tue, 04 Jul 2023 04:55:52 GMT  
		Size: 1.4 MB (1385875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2de9446f31d2128352d88e158d78ec61f485d2fb3f4e25fe2d696a344feff9`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; s390x

```console
$ docker pull adminer@sha256:faca9d7d2872d5b55b86b5075e69a84c556c930258a875e13aa3fa72ecf2b17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93697370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5204631a997d1234d7546fcb38705962f54c2530fc951f2daf73a073ad0969`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:18 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:54:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1820f29b009a397fd193ee10f17404280d3b9228f8b36daf5bb815bce0307`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a3cdb65e8cd3b2cb9e3aceddb9e95864743111dc589908c4805fca9f9bf9b8`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aee720253a711b2d402e08cb5cafdfa0cc5290a8f09f543174ff677614c67f`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.4 MB (1385448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f7c164596b5009b686a6803bc457fe549e5272341bfa787cc8f342ad43442`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-fastcgi`

```console
$ docker pull adminer@sha256:58587babe247ff692523f82309b6db1a74d57813e3503f2f6d45eb1ca788cc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:4.8.1-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:6caa807820ca7c9cdbadf1ab1d45db1bd786efc37ef5aa47cbe10708dd12d998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95935139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5a487eafbb1e1c54550a075a220d824e930146fccd78c5a4afdb74a2bc50a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 03:26:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:33 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:33 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:44 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d76a56a3771369c6e704d5e35bd1766d6e549b0d66ed49c4ad0f11e9606374f`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7ccb20f3a0eece3e90efca525e5571942cf228298324515c02198d05777cb9`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8c7d8cd6f443d542fd01782eed5dc03b0a74d0f0714683dc176561ba235edf`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db1d8f59a146868100bd71857251dc11b79dbc9b8b8cb776a4d89e05748ac88`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.4 MB (1385454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8979c84db28ce690caecdf197ecff4c3fa9fd09b8da2aed722a745e415edae28`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:000c82eff38911214c7db7c3a511c0a57cba0bda80bcf27ee035587d3eed20be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610a0bd191c5498d32fa7dcb44808b310a87072810de50eba2ae2654de87ca3c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:22 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 04:32:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:23 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:23 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:24 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:37 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:37 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75e47d8dcfa6ad8c28efd5221051c57745479e4c9be773a174ed053c964fdc`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6d17752c4fc62ce532477600101cfe5b1108020f93a8c97e4d220d8ef823ba`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b637b24bf6e78648f068b8a4683cf6f28db889ba791c3134c6524a347b7ca`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07ec511505a60a6fad31428b9d54cf218f5256afd31101c81098d87db2a5e3`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.4 MB (1385376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b106734e44f3b038b26d8a5c64f653c388d92572b121d6ce448372a7ff16c2f`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:0be94bd6202f72f371789c8c37780bf657de3d1c590e6ca57b0bfc52b20b6904
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87793947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1678a0b92255b8085e7baec25267827d874cf221fc98c542e2979a62d5def219`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 05:48:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:34 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:46 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611383b899e8a30dc5ee74865f6ad93b4b59b676b48f4c4a9fe5eb0d92d9a8a3`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e604c1e6cce082e392b473dcdc2824c86f055c7e910560c81eb54d7dbf758c`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e04bf6ee13b97e03f675aa27139cac7931f5cd1c735d6a6e078abf6ab8004`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9348a926275a93bc78151de56c3200f5f3d15827e53cd9c50db6ef4557513b6`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.4 MB (1385410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07644552098791dbe95267ac6756b65b68cdced2563aa3f7d54135b1c72de7dc`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:62a62e95e6e92f9e8510495f3cb436a6b4196b63bb07134596be3e010d33acd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94340314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164e7749682325c1aa3417dd5bdd3315167af4c5b97129e7994a12bfc9a727bc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:33:11 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 28 Jul 2023 01:33:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:33:12 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:33:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:22 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:22 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8010fea9be3a6e42dfda4398bc8dd961f3cc38cd2b066ccc38d8b83b7b0dd3e4`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7694be696a7e8c7e0ca897c46b134bd20166b15352ab0c9c130f49b4334faebc`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec715a9f3239113933f55f76bc62d32455f3b1647d2867f143645ade0de0e60`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e99cff7b42b42793347c1b48793f8d6340ba93fca1aa4a375b53344b9112c9`  
		Last Modified: Fri, 28 Jul 2023 01:33:58 GMT  
		Size: 1.4 MB (1385351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea23c2e8231c1a0717f52f8aac5318af3412ac9f3481f18bf16428f83686358`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:f28603ea4c880db60110049c6cf22720545bc6be296659ec3bb3d320c7343d55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96991589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cf9f1de498d643ae57669878101b1e59fcebf70db1074d81ceea8801ccd8f7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:49 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 05:26:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:49 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:27:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:27:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:27:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:27:02 GMT
USER adminer
# Tue, 04 Jul 2023 05:27:02 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55ca2f23f925c98c51f8a734f76590fb5f3be47a5f8dee895176e2c49ce49cf`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e6f54f2eebdc0908a5bb0ea1bf013ce274873f298ca9b3516e231f378666da`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88228cdb9c571deaf46d3473a01ca87db8a9b15747155e4fa4acb1dfd7978eb`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23222c8c9b4ecdd9417f8199b026bbfb4764f3a4b1eb9bb2e36a6fdae431afdb`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.4 MB (1385307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51719e58ff78bcdbb9022589936f75bbe7a64df0048c6777578f0f2461600a3d`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:50d0c5eb0fbb7449ac67c44dbdfc5ac9641364bd0aea37d12bf97c3d6816d8d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92616895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1386d228067b12c15d63697ae97c45005440e0d5fd512eaabf582a612a1be56`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:30:55 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 14:31:02 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:31:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:31:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:31:11 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:31:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:31:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:32:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:32:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:32:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:32:15 GMT
USER adminer
# Tue, 04 Jul 2023 14:32:18 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8538a1b8df56534e7c48884f0d1725ddebeaf72b505864e1f72ef622b38548`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b025e749cde7de1afda81b9cf371bce0015174ae81e8927c0b0d6b1ab4a8a2`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b4935cf4ff366bd19d37dd1e4355f151e7669e579994aa44b9c11eede72183`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88efd70fc04cd68535ade5181500a3f0866dc315fc4cc75ba33a82e1a50ca358`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.4 MB (1386288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8dc7d0c9faa199b112a26d67ded4852ef3a41460385ab3e0a81c1e54156877`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:9364792ada1b2eb7211f622b7a788103b4abd9fcf3b97c8768924f6e09b6690e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101260839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a36421f33b53c1c0f63f968861fd66876c3ea0c6830325f9681e900bd5d2f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:54:41 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 04:54:44 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:54:46 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:54:46 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:54:47 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:54:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:54:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:55:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:55:25 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:55:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:55:26 GMT
USER adminer
# Tue, 04 Jul 2023 04:55:27 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2011aca228bf492e49980db4d7f382fb149bfcdd0d23cb67659c0df6737226`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859d3a288f61883dc684d9157c6cd5075a0b1a74f011c4e69e987c11f886bbd7`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5d0aacdd54eb059e402c26939fdccb4fe827cc7b1fb89571221e11e2bc6e62`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c456356bca8fc124638a22b16275bb5b2ba5380b47c6af4c3cf3683ce4f8d0b5`  
		Last Modified: Tue, 04 Jul 2023 04:56:29 GMT  
		Size: 1.4 MB (1385813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dc45753ebe2ef73c8d7aece8aa163f83dfbbc85299390556dd5a5d9854b65b`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:812f84c9c8509197cf3cfd52fa7136b369eee6ec8fbf1f5d2137da850ebeb6bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93700045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8977da130ff083c95c53d0d74b0de0698be066c3800b8194112d7626900e84a0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:27 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 28 Jul 2023 01:54:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:28 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:28 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:36 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:36 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:36 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d8d234b4ce8e57ad21e2de8659dc0f24143bb0af60900bd7317781c460740b`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554328df2364098195b130e82f52a57e47ff4b781ce4c9d69810941845b904b7`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2b12034fd6588bd8a56877d9cf07d58044f91dd0f343c31876aa015a99c1cf`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154c43a8555997901e4a970eafa0c5bea898ebdf9610d3274b8bda76877115d7`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.4 MB (1385420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e715878adf9a51664bcf8f0cd897b9d823c44d90dff045eed47d17f7efa72e48`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-standalone`

```console
$ docker pull adminer@sha256:18609aac77637e99fbbdfbe2de4f3837bf4b835c30b4c84fdb593d90d24349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:4.8.1-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:0174c52770125d4206b808412926458b544758845f8f552151f97cb33881ca32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad39a6f503c44bda7082754111a22a9ba05f764a759d3d3ada7b444a55bc12`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:15 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:26 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 03:26:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7a59571f85d61c32167207b31048b15456dbc4c07560c912b86f1ceef081c`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530e7e02f75518fdf62aa976f5ec67a1c0c66451e5de48963221ec07b0143bfd`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee8734c62c40d287661833cf8774b85007370efb9f23c1dc52a0983bb2efa1`  
		Last Modified: Tue, 04 Jul 2023 03:26:59 GMT  
		Size: 1.4 MB (1385432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a0cc37cf2cace649b536ffa14618f5b2f9d1e641feeee7a449e94c0c188f5`  
		Last Modified: Tue, 04 Jul 2023 03:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:962e9bfdfa21d1e9af480c715cb14c0200637a4304b6969013d9aa9dffdd9b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91194385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145a48b09f292be73dfc37cb3141ac089a668515d7448662a553615c95e55e0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:19 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:32:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9237d1e17acadb8c10dd17f8d666ccd1c9343514a18589a12a5d6bfa7eff40`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18540feda134b6545df8efa09e435f8f79fb7828703c8f0cd6fa986ce96f5295`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ddef2f8502b3232c3215f41c96321944ab58eb1efd0dd0da8359d91f43371`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.4 MB (1385375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a79a4cff669839273b8b81cf6a0fc9582dece1dcbd47b2d4ad47b829cfee1b0`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a05d314c7de66c8cb10b085543a98e4278d271893be05d73b7f28515f74854f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fe9ea70e4697d5a79eaaa3de540bcb6ab33331b23b134e3e83a5e80102c84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:22 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:48:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450f098fa03bb8ec8464823656b3438895417c4ff68e7cb817bf81d92428835e`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243bba61a9bf6f71050b509f6d32f150733d079d88f05e3baf5257037291d52`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ca2f56cb674dfee1f52c140d8d2f26e0068b1f9a192518bd80245bd1dd0eb`  
		Last Modified: Tue, 04 Jul 2023 05:48:56 GMT  
		Size: 1.4 MB (1385426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5dc82712c6232409a9e98550357737eceb09e05870ea9579e6d37ff34e3094`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:958990f6d1f66e6a9f854251e04835456490db94d5049bd0781b82a4535b79b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ec1ac6b42873905c2e49fe8b847346b584a9934045a9af7c5ad3a2f4ce533`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:32:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:32:58 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:09 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:33:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805759b30cc65928f6590a87df6374385bc4ab00bac8e6c082067cad6a0c8052`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c52d243051d0380315d262f0c75865d8dbaff27d5d57b1fc3090fbb76dbf44`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b32c0aa3641a21349bda0ace8e58c088db3cbbba1a6f262ea97e74e2ecd25`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e6078a351dedfa26b1cd20ceca3b8cca8fc8e6aa765670fa373020469f9ef`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; 386

```console
$ docker pull adminer@sha256:461fd7352ea0d006503da7a92caf49bef7d68374e3a6f186026f2aac5bd316ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b840e17b2b92310ff52e92ccc4f30a308ebab1004136bbf42eba705fb9bc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:26:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:26:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:26:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:26:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:26:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96dc5d5492a6571a3974948e4374a3c5d7049b6d958aac525df2d2bbfdf627`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341dcf80f058bf05383a7b6a2df74a1d36294baebd5f5292e4fe8434091576a1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd8d1218897da786e8e717e520aa31c9c6f6db2aa9ec80af132f76deb7f67c`  
		Last Modified: Tue, 04 Jul 2023 05:27:15 GMT  
		Size: 1.4 MB (1385291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9673c67b185741461ba76717835fe0a1d76ab762d02dae5f5a28fb3a1450566b`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:bba236958f3ef20f85f094ef599957a623ea712aa38c6b16090a9d32b6b72d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4507a99e483cae111243d540a169beaba5b2399ae32abbc24552dcc14c06646f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:29:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:29:17 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:29:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:29:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:29:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:29:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:30:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:30:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:30:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:30:31 GMT
USER adminer
# Tue, 04 Jul 2023 14:30:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 14:30:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c7da25ad9de44c8075b26de39239e884bba5e188ad5b3c7d9d9f126ba5039`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddc446ac238027e91c76b2ed3e55af67046cf1742ec9ff8f1189b45b3226a14`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686c97d6e8dd8d071fca9724489d4b249e53a9b029354c8668871b3725e5305`  
		Last Modified: Tue, 04 Jul 2023 14:32:42 GMT  
		Size: 1.4 MB (1386278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce629354f0a6b55bc416d4b4fcbb5e8ce6a197cb5708a017936c011662d82c`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:513659a3661e42d0e40985ae242c59d5dada7938fc81cf3b033261838c8f59f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a18eba61d2a1d4913ca037b6b2fd9bd7c455f98ca723b338a5c4d3f20513`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:53:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:53:10 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:53:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:53:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:53:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:53:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:54:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:54:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:54:22 GMT
USER adminer
# Tue, 04 Jul 2023 04:54:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:54:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa56055f8b8b3c5e2190e891801d2cd8e63265e487d2065cc972d9b12531c71`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18434fa3f232269e2dea15e4eef30f28360ba63d46add5fb9bdad8c361a8bc8e`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec4ed1374295eb9d7ea18c48406bea22284a8b8a24426929873ed30572209c`  
		Last Modified: Tue, 04 Jul 2023 04:55:52 GMT  
		Size: 1.4 MB (1385875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2de9446f31d2128352d88e158d78ec61f485d2fb3f4e25fe2d696a344feff9`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:faca9d7d2872d5b55b86b5075e69a84c556c930258a875e13aa3fa72ecf2b17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93697370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5204631a997d1234d7546fcb38705962f54c2530fc951f2daf73a073ad0969`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:18 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:54:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1820f29b009a397fd193ee10f17404280d3b9228f8b36daf5bb815bce0307`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a3cdb65e8cd3b2cb9e3aceddb9e95864743111dc589908c4805fca9f9bf9b8`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aee720253a711b2d402e08cb5cafdfa0cc5290a8f09f543174ff677614c67f`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.4 MB (1385448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f7c164596b5009b686a6803bc457fe549e5272341bfa787cc8f342ad43442`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:58587babe247ff692523f82309b6db1a74d57813e3503f2f6d45eb1ca788cc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:6caa807820ca7c9cdbadf1ab1d45db1bd786efc37ef5aa47cbe10708dd12d998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95935139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5a487eafbb1e1c54550a075a220d824e930146fccd78c5a4afdb74a2bc50a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 03:26:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:33 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:33 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:44 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d76a56a3771369c6e704d5e35bd1766d6e549b0d66ed49c4ad0f11e9606374f`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7ccb20f3a0eece3e90efca525e5571942cf228298324515c02198d05777cb9`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8c7d8cd6f443d542fd01782eed5dc03b0a74d0f0714683dc176561ba235edf`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db1d8f59a146868100bd71857251dc11b79dbc9b8b8cb776a4d89e05748ac88`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 1.4 MB (1385454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8979c84db28ce690caecdf197ecff4c3fa9fd09b8da2aed722a745e415edae28`  
		Last Modified: Tue, 04 Jul 2023 03:27:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:000c82eff38911214c7db7c3a511c0a57cba0bda80bcf27ee035587d3eed20be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610a0bd191c5498d32fa7dcb44808b310a87072810de50eba2ae2654de87ca3c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:22 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 04:32:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:23 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:23 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:24 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:37 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:37 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75e47d8dcfa6ad8c28efd5221051c57745479e4c9be773a174ed053c964fdc`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6d17752c4fc62ce532477600101cfe5b1108020f93a8c97e4d220d8ef823ba`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b637b24bf6e78648f068b8a4683cf6f28db889ba791c3134c6524a347b7ca`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07ec511505a60a6fad31428b9d54cf218f5256afd31101c81098d87db2a5e3`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 1.4 MB (1385376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b106734e44f3b038b26d8a5c64f653c388d92572b121d6ce448372a7ff16c2f`  
		Last Modified: Tue, 04 Jul 2023 04:33:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:0be94bd6202f72f371789c8c37780bf657de3d1c590e6ca57b0bfc52b20b6904
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87793947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1678a0b92255b8085e7baec25267827d874cf221fc98c542e2979a62d5def219`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 05:48:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:34 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:46 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611383b899e8a30dc5ee74865f6ad93b4b59b676b48f4c4a9fe5eb0d92d9a8a3`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e604c1e6cce082e392b473dcdc2824c86f055c7e910560c81eb54d7dbf758c`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282e04bf6ee13b97e03f675aa27139cac7931f5cd1c735d6a6e078abf6ab8004`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9348a926275a93bc78151de56c3200f5f3d15827e53cd9c50db6ef4557513b6`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 1.4 MB (1385410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07644552098791dbe95267ac6756b65b68cdced2563aa3f7d54135b1c72de7dc`  
		Last Modified: Tue, 04 Jul 2023 05:49:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:62a62e95e6e92f9e8510495f3cb436a6b4196b63bb07134596be3e010d33acd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94340314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164e7749682325c1aa3417dd5bdd3315167af4c5b97129e7994a12bfc9a727bc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:33:11 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 28 Jul 2023 01:33:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:33:12 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:33:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:33:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:22 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:22 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8010fea9be3a6e42dfda4398bc8dd961f3cc38cd2b066ccc38d8b83b7b0dd3e4`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7694be696a7e8c7e0ca897c46b134bd20166b15352ab0c9c130f49b4334faebc`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec715a9f3239113933f55f76bc62d32455f3b1647d2867f143645ade0de0e60`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e99cff7b42b42793347c1b48793f8d6340ba93fca1aa4a375b53344b9112c9`  
		Last Modified: Fri, 28 Jul 2023 01:33:58 GMT  
		Size: 1.4 MB (1385351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea23c2e8231c1a0717f52f8aac5318af3412ac9f3481f18bf16428f83686358`  
		Last Modified: Fri, 28 Jul 2023 01:33:57 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:f28603ea4c880db60110049c6cf22720545bc6be296659ec3bb3d320c7343d55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96991589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cf9f1de498d643ae57669878101b1e59fcebf70db1074d81ceea8801ccd8f7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:49 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 05:26:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:49 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:27:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:27:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:27:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:27:02 GMT
USER adminer
# Tue, 04 Jul 2023 05:27:02 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55ca2f23f925c98c51f8a734f76590fb5f3be47a5f8dee895176e2c49ce49cf`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e6f54f2eebdc0908a5bb0ea1bf013ce274873f298ca9b3516e231f378666da`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88228cdb9c571deaf46d3473a01ca87db8a9b15747155e4fa4acb1dfd7978eb`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23222c8c9b4ecdd9417f8199b026bbfb4764f3a4b1eb9bb2e36a6fdae431afdb`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 1.4 MB (1385307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51719e58ff78bcdbb9022589936f75bbe7a64df0048c6777578f0f2461600a3d`  
		Last Modified: Tue, 04 Jul 2023 05:27:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:50d0c5eb0fbb7449ac67c44dbdfc5ac9641364bd0aea37d12bf97c3d6816d8d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92616895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1386d228067b12c15d63697ae97c45005440e0d5fd512eaabf582a612a1be56`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:30:55 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 14:31:02 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:31:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:31:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:31:11 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:31:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:31:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:32:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:32:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:32:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:32:15 GMT
USER adminer
# Tue, 04 Jul 2023 14:32:18 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8538a1b8df56534e7c48884f0d1725ddebeaf72b505864e1f72ef622b38548`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b025e749cde7de1afda81b9cf371bce0015174ae81e8927c0b0d6b1ab4a8a2`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b4935cf4ff366bd19d37dd1e4355f151e7669e579994aa44b9c11eede72183`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88efd70fc04cd68535ade5181500a3f0866dc315fc4cc75ba33a82e1a50ca358`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 1.4 MB (1386288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8dc7d0c9faa199b112a26d67ded4852ef3a41460385ab3e0a81c1e54156877`  
		Last Modified: Tue, 04 Jul 2023 14:33:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:9364792ada1b2eb7211f622b7a788103b4abd9fcf3b97c8768924f6e09b6690e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101260839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a36421f33b53c1c0f63f968861fd66876c3ea0c6830325f9681e900bd5d2f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:54:41 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 04 Jul 2023 04:54:44 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:54:46 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:54:46 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:54:47 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:54:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:54:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:55:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:55:25 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:55:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:55:26 GMT
USER adminer
# Tue, 04 Jul 2023 04:55:27 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2011aca228bf492e49980db4d7f382fb149bfcdd0d23cb67659c0df6737226`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859d3a288f61883dc684d9157c6cd5075a0b1a74f011c4e69e987c11f886bbd7`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5d0aacdd54eb059e402c26939fdccb4fe827cc7b1fb89571221e11e2bc6e62`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c456356bca8fc124638a22b16275bb5b2ba5380b47c6af4c3cf3683ce4f8d0b5`  
		Last Modified: Tue, 04 Jul 2023 04:56:29 GMT  
		Size: 1.4 MB (1385813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dc45753ebe2ef73c8d7aece8aa163f83dfbbc85299390556dd5a5d9854b65b`  
		Last Modified: Tue, 04 Jul 2023 04:56:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:812f84c9c8509197cf3cfd52fa7136b369eee6ec8fbf1f5d2137da850ebeb6bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93700045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8977da130ff083c95c53d0d74b0de0698be066c3800b8194112d7626900e84a0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:27 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 28 Jul 2023 01:54:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:28 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:28 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:28 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:36 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:36 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:36 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d8d234b4ce8e57ad21e2de8659dc0f24143bb0af60900bd7317781c460740b`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554328df2364098195b130e82f52a57e47ff4b781ce4c9d69810941845b904b7`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2b12034fd6588bd8a56877d9cf07d58044f91dd0f343c31876aa015a99c1cf`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154c43a8555997901e4a970eafa0c5bea898ebdf9610d3274b8bda76877115d7`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 1.4 MB (1385420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e715878adf9a51664bcf8f0cd897b9d823c44d90dff045eed47d17f7efa72e48`  
		Last Modified: Fri, 28 Jul 2023 01:55:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:18609aac77637e99fbbdfbe2de4f3837bf4b835c30b4c84fdb593d90d24349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:0174c52770125d4206b808412926458b544758845f8f552151f97cb33881ca32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad39a6f503c44bda7082754111a22a9ba05f764a759d3d3ada7b444a55bc12`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:15 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:26 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 03:26:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7a59571f85d61c32167207b31048b15456dbc4c07560c912b86f1ceef081c`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530e7e02f75518fdf62aa976f5ec67a1c0c66451e5de48963221ec07b0143bfd`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee8734c62c40d287661833cf8774b85007370efb9f23c1dc52a0983bb2efa1`  
		Last Modified: Tue, 04 Jul 2023 03:26:59 GMT  
		Size: 1.4 MB (1385432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a0cc37cf2cace649b536ffa14618f5b2f9d1e641feeee7a449e94c0c188f5`  
		Last Modified: Tue, 04 Jul 2023 03:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:962e9bfdfa21d1e9af480c715cb14c0200637a4304b6969013d9aa9dffdd9b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91194385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145a48b09f292be73dfc37cb3141ac089a668515d7448662a553615c95e55e0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:19 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:32:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9237d1e17acadb8c10dd17f8d666ccd1c9343514a18589a12a5d6bfa7eff40`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18540feda134b6545df8efa09e435f8f79fb7828703c8f0cd6fa986ce96f5295`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ddef2f8502b3232c3215f41c96321944ab58eb1efd0dd0da8359d91f43371`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.4 MB (1385375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a79a4cff669839273b8b81cf6a0fc9582dece1dcbd47b2d4ad47b829cfee1b0`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a05d314c7de66c8cb10b085543a98e4278d271893be05d73b7f28515f74854f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fe9ea70e4697d5a79eaaa3de540bcb6ab33331b23b134e3e83a5e80102c84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:22 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:48:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450f098fa03bb8ec8464823656b3438895417c4ff68e7cb817bf81d92428835e`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243bba61a9bf6f71050b509f6d32f150733d079d88f05e3baf5257037291d52`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ca2f56cb674dfee1f52c140d8d2f26e0068b1f9a192518bd80245bd1dd0eb`  
		Last Modified: Tue, 04 Jul 2023 05:48:56 GMT  
		Size: 1.4 MB (1385426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5dc82712c6232409a9e98550357737eceb09e05870ea9579e6d37ff34e3094`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:958990f6d1f66e6a9f854251e04835456490db94d5049bd0781b82a4535b79b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ec1ac6b42873905c2e49fe8b847346b584a9934045a9af7c5ad3a2f4ce533`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:32:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:32:58 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:09 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:33:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805759b30cc65928f6590a87df6374385bc4ab00bac8e6c082067cad6a0c8052`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c52d243051d0380315d262f0c75865d8dbaff27d5d57b1fc3090fbb76dbf44`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b32c0aa3641a21349bda0ace8e58c088db3cbbba1a6f262ea97e74e2ecd25`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e6078a351dedfa26b1cd20ceca3b8cca8fc8e6aa765670fa373020469f9ef`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:461fd7352ea0d006503da7a92caf49bef7d68374e3a6f186026f2aac5bd316ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b840e17b2b92310ff52e92ccc4f30a308ebab1004136bbf42eba705fb9bc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:26:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:26:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:26:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:26:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:26:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96dc5d5492a6571a3974948e4374a3c5d7049b6d958aac525df2d2bbfdf627`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341dcf80f058bf05383a7b6a2df74a1d36294baebd5f5292e4fe8434091576a1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd8d1218897da786e8e717e520aa31c9c6f6db2aa9ec80af132f76deb7f67c`  
		Last Modified: Tue, 04 Jul 2023 05:27:15 GMT  
		Size: 1.4 MB (1385291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9673c67b185741461ba76717835fe0a1d76ab762d02dae5f5a28fb3a1450566b`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:bba236958f3ef20f85f094ef599957a623ea712aa38c6b16090a9d32b6b72d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4507a99e483cae111243d540a169beaba5b2399ae32abbc24552dcc14c06646f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:29:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:29:17 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:29:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:29:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:29:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:29:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:30:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:30:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:30:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:30:31 GMT
USER adminer
# Tue, 04 Jul 2023 14:30:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 14:30:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c7da25ad9de44c8075b26de39239e884bba5e188ad5b3c7d9d9f126ba5039`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddc446ac238027e91c76b2ed3e55af67046cf1742ec9ff8f1189b45b3226a14`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686c97d6e8dd8d071fca9724489d4b249e53a9b029354c8668871b3725e5305`  
		Last Modified: Tue, 04 Jul 2023 14:32:42 GMT  
		Size: 1.4 MB (1386278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce629354f0a6b55bc416d4b4fcbb5e8ce6a197cb5708a017936c011662d82c`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:513659a3661e42d0e40985ae242c59d5dada7938fc81cf3b033261838c8f59f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a18eba61d2a1d4913ca037b6b2fd9bd7c455f98ca723b338a5c4d3f20513`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:53:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:53:10 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:53:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:53:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:53:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:53:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:54:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:54:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:54:22 GMT
USER adminer
# Tue, 04 Jul 2023 04:54:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:54:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa56055f8b8b3c5e2190e891801d2cd8e63265e487d2065cc972d9b12531c71`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18434fa3f232269e2dea15e4eef30f28360ba63d46add5fb9bdad8c361a8bc8e`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec4ed1374295eb9d7ea18c48406bea22284a8b8a24426929873ed30572209c`  
		Last Modified: Tue, 04 Jul 2023 04:55:52 GMT  
		Size: 1.4 MB (1385875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2de9446f31d2128352d88e158d78ec61f485d2fb3f4e25fe2d696a344feff9`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:faca9d7d2872d5b55b86b5075e69a84c556c930258a875e13aa3fa72ecf2b17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93697370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5204631a997d1234d7546fcb38705962f54c2530fc951f2daf73a073ad0969`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:18 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:54:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1820f29b009a397fd193ee10f17404280d3b9228f8b36daf5bb815bce0307`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a3cdb65e8cd3b2cb9e3aceddb9e95864743111dc589908c4805fca9f9bf9b8`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aee720253a711b2d402e08cb5cafdfa0cc5290a8f09f543174ff677614c67f`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.4 MB (1385448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f7c164596b5009b686a6803bc457fe549e5272341bfa787cc8f342ad43442`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:18609aac77637e99fbbdfbe2de4f3837bf4b835c30b4c84fdb593d90d24349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:0174c52770125d4206b808412926458b544758845f8f552151f97cb33881ca32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad39a6f503c44bda7082754111a22a9ba05f764a759d3d3ada7b444a55bc12`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:25:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:26:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:26:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 03:26:15 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 03:26:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 03:26:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 03:26:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 03:26:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:26:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 03:26:26 GMT
USER adminer
# Tue, 04 Jul 2023 03:26:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 03:26:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942860e9b081ab6c14dea841e13d6b8e230b5c3a7482ddc73980c866338f81bd`  
		Last Modified: Tue, 04 Jul 2023 03:27:06 GMT  
		Size: 39.5 MB (39487448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571177b537e8c4f94f8bd4920e829d50ef7d56e541695ba67a448487efc1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7a59571f85d61c32167207b31048b15456dbc4c07560c912b86f1ceef081c`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530e7e02f75518fdf62aa976f5ec67a1c0c66451e5de48963221ec07b0143bfd`  
		Last Modified: Tue, 04 Jul 2023 03:26:58 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee8734c62c40d287661833cf8774b85007370efb9f23c1dc52a0983bb2efa1`  
		Last Modified: Tue, 04 Jul 2023 03:26:59 GMT  
		Size: 1.4 MB (1385432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a0cc37cf2cace649b536ffa14618f5b2f9d1e641feeee7a449e94c0c188f5`  
		Last Modified: Tue, 04 Jul 2023 03:27:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:962e9bfdfa21d1e9af480c715cb14c0200637a4304b6969013d9aa9dffdd9b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91194385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6145a48b09f292be73dfc37cb3141ac089a668515d7448662a553615c95e55e0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:39 GMT
ADD file:fe1b9f9f6c7d67ad23a2ee839774be4bcee33c60c7b34c48df5a08eb33cafd1b in / 
# Tue, 04 Jul 2023 00:48:40 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:31:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:32:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:32:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:32:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:32:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:32:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:32:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:32:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:32:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:32:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:32:19 GMT
USER adminer
# Tue, 04 Jul 2023 04:32:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:32:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:702dd8b607f626c689176debe921fe96009c1ce6dbd66f4f238c7def50080e3d`  
		Last Modified: Tue, 04 Jul 2023 00:52:15 GMT  
		Size: 52.6 MB (52556778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d374e7d45666fbc1903d32400cd401880366876db459c5ab206a54ab0d0411`  
		Last Modified: Tue, 04 Jul 2023 04:32:58 GMT  
		Size: 37.2 MB (37248008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b59f67ee61ca2a807576d30a1cc008c51081eae0849e200e60ce47af498c`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9237d1e17acadb8c10dd17f8d666ccd1c9343514a18589a12a5d6bfa7eff40`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18540feda134b6545df8efa09e435f8f79fb7828703c8f0cd6fa986ce96f5295`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ddef2f8502b3232c3215f41c96321944ab58eb1efd0dd0da8359d91f43371`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 1.4 MB (1385375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a79a4cff669839273b8b81cf6a0fc9582dece1dcbd47b2d4ad47b829cfee1b0`  
		Last Modified: Tue, 04 Jul 2023 04:32:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6a05d314c7de66c8cb10b085543a98e4278d271893be05d73b7f28515f74854f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441fe9ea70e4697d5a79eaaa3de540bcb6ab33331b23b134e3e83a5e80102c84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:06 GMT
ADD file:17e02296458241d9441f8da6a5dafb747d528a729106b17cec2f4c1c8cfe0ad8 in / 
# Tue, 04 Jul 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:47:35 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:48:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:48:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:48:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:48:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:48:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:48:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:48:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:48:22 GMT
USER adminer
# Tue, 04 Jul 2023 05:48:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:48:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:31edf2db9ca1650aa08e2d42e9b5bb7349413d7212110149a1a5d202ac20914b`  
		Last Modified: Tue, 04 Jul 2023 01:03:12 GMT  
		Size: 50.2 MB (50218247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcd0af927af2ef5ff85003d2efb7bec343ebb0e0ae33e33a182aba3044318c`  
		Last Modified: Tue, 04 Jul 2023 05:49:03 GMT  
		Size: 36.2 MB (36183362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b63416f4c6f052acc74f92deae27e302df97dc86efe776938f5064b98a90f`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450f098fa03bb8ec8464823656b3438895417c4ff68e7cb817bf81d92428835e`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243bba61a9bf6f71050b509f6d32f150733d079d88f05e3baf5257037291d52`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ca2f56cb674dfee1f52c140d8d2f26e0068b1f9a192518bd80245bd1dd0eb`  
		Last Modified: Tue, 04 Jul 2023 05:48:56 GMT  
		Size: 1.4 MB (1385426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5dc82712c6232409a9e98550357737eceb09e05870ea9579e6d37ff34e3094`  
		Last Modified: Tue, 04 Jul 2023 05:48:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:958990f6d1f66e6a9f854251e04835456490db94d5049bd0781b82a4535b79b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ec1ac6b42873905c2e49fe8b847346b584a9934045a9af7c5ad3a2f4ce533`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:38 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:32:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:32:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:32:58 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:33:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:33:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:33:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:33:09 GMT
USER adminer
# Fri, 28 Jul 2023 01:33:09 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:33:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c936be3d46519b363d127d99d4a16afc2bcda8095c369d6962f2074106072b`  
		Last Modified: Fri, 28 Jul 2023 01:33:40 GMT  
		Size: 39.2 MB (39243229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f330de399f2ce87df9e5548f572616f566f9e9c844ebe34b92acf948008cdd`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805759b30cc65928f6590a87df6374385bc4ab00bac8e6c082067cad6a0c8052`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c52d243051d0380315d262f0c75865d8dbaff27d5d57b1fc3090fbb76dbf44`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966b32c0aa3641a21349bda0ace8e58c088db3cbbba1a6f262ea97e74e2ecd25`  
		Last Modified: Fri, 28 Jul 2023 01:33:34 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e6078a351dedfa26b1cd20ceca3b8cca8fc8e6aa765670fa373020469f9ef`  
		Last Modified: Fri, 28 Jul 2023 01:33:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:461fd7352ea0d006503da7a92caf49bef7d68374e3a6f186026f2aac5bd316ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577b840e17b2b92310ff52e92ccc4f30a308ebab1004136bbf42eba705fb9bc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:48 GMT
ADD file:c5739407c2c257fbb85ab4b9dcd2dc07e6fe172d7309aaaaab544c8df6c42b92 in / 
# Tue, 04 Jul 2023 01:38:49 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:26:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 05:26:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:26:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 05:26:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 05:26:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 05:26:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 05:26:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 05:26:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 05:26:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 05:26:46 GMT
USER adminer
# Tue, 04 Jul 2023 05:26:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 05:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b700c8b35944e0d5f6ab9049dbe2262492e26327a8efad518b1011428393653f`  
		Last Modified: Tue, 04 Jul 2023 01:43:49 GMT  
		Size: 56.0 MB (56040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a902a66c5c608f61d35dd264eb84af9a969f2d77d57ec06ad874647c6357d0e`  
		Last Modified: Tue, 04 Jul 2023 05:27:24 GMT  
		Size: 39.6 MB (39558591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cd99c580c15e79afcf178eb77f3c0ac0432c212f50ccd720a2680b26373d1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96dc5d5492a6571a3974948e4374a3c5d7049b6d958aac525df2d2bbfdf627`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341dcf80f058bf05383a7b6a2df74a1d36294baebd5f5292e4fe8434091576a1`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dd8d1218897da786e8e717e520aa31c9c6f6db2aa9ec80af132f76deb7f67c`  
		Last Modified: Tue, 04 Jul 2023 05:27:15 GMT  
		Size: 1.4 MB (1385291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9673c67b185741461ba76717835fe0a1d76ab762d02dae5f5a28fb3a1450566b`  
		Last Modified: Tue, 04 Jul 2023 05:27:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:bba236958f3ef20f85f094ef599957a623ea712aa38c6b16090a9d32b6b72d44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4507a99e483cae111243d540a169beaba5b2399ae32abbc24552dcc14c06646f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:02 GMT
ADD file:f7ddd7406e3aa24165fc80933583fc2298f9792865511fe65def2f571fed2207 in / 
# Tue, 04 Jul 2023 01:10:07 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:27:09 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 14:29:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:29:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 14:29:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 14:29:17 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 14:29:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 14:29:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 14:29:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 14:29:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 14:30:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 14:30:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 14:30:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 14:30:31 GMT
USER adminer
# Tue, 04 Jul 2023 14:30:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 14:30:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:af98e96208d7ce4cff5417a3e8a38f98d2ed3abbca318e1e6c323aa8b8c56690`  
		Last Modified: Tue, 04 Jul 2023 01:20:40 GMT  
		Size: 53.3 MB (53270472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6791bd7eb8dda07e9d1530ff7401ec314ff7c191e0c85f206cc8cd86be855c`  
		Last Modified: Tue, 04 Jul 2023 14:33:08 GMT  
		Size: 38.0 MB (37953331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3920a88961362bf993802523f7cca2e85caaa4a60f7f1e3d63aaf5eb0c09a4a7`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c7da25ad9de44c8075b26de39239e884bba5e188ad5b3c7d9d9f126ba5039`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddc446ac238027e91c76b2ed3e55af67046cf1742ec9ff8f1189b45b3226a14`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686c97d6e8dd8d071fca9724489d4b249e53a9b029354c8668871b3725e5305`  
		Last Modified: Tue, 04 Jul 2023 14:32:42 GMT  
		Size: 1.4 MB (1386278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce629354f0a6b55bc416d4b4fcbb5e8ce6a197cb5708a017936c011662d82c`  
		Last Modified: Tue, 04 Jul 2023 14:32:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:513659a3661e42d0e40985ae242c59d5dada7938fc81cf3b033261838c8f59f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a18eba61d2a1d4913ca037b6b2fd9bd7c455f98ca723b338a5c4d3f20513`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:11 GMT
ADD file:ff86c25854c28609c2852c1615270f0acd4c4efaa38ff8ed9c23afe5132f2135 in / 
# Tue, 04 Jul 2023 01:18:15 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:50:59 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 04:52:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:53:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 04 Jul 2023 04:53:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 04 Jul 2023 04:53:10 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 04:53:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 04 Jul 2023 04:53:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 04 Jul 2023 04:53:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 04 Jul 2023 04:53:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 04 Jul 2023 04:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Jul 2023 04:54:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 04 Jul 2023 04:54:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 04 Jul 2023 04:54:22 GMT
USER adminer
# Tue, 04 Jul 2023 04:54:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 04 Jul 2023 04:54:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a792749f62225048efdf85841bea6f3999f586371852f3dbce13a6c3d89b1fa7`  
		Last Modified: Tue, 04 Jul 2023 01:25:06 GMT  
		Size: 58.9 MB (58927745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44790fdc65745caeec0d36cb605fed307ff2f9e2ef066a8d2b1522e8221f18f3`  
		Last Modified: Tue, 04 Jul 2023 04:56:04 GMT  
		Size: 40.9 MB (40940332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24457876d46dbb125dbcfa9f211d86229bb07a8f9864412462d6c795573177a8`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa56055f8b8b3c5e2190e891801d2cd8e63265e487d2065cc972d9b12531c71`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18434fa3f232269e2dea15e4eef30f28360ba63d46add5fb9bdad8c361a8bc8e`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec4ed1374295eb9d7ea18c48406bea22284a8b8a24426929873ed30572209c`  
		Last Modified: Tue, 04 Jul 2023 04:55:52 GMT  
		Size: 1.4 MB (1385875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2de9446f31d2128352d88e158d78ec61f485d2fb3f4e25fe2d696a344feff9`  
		Last Modified: Tue, 04 Jul 2023 04:55:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:faca9d7d2872d5b55b86b5075e69a84c556c930258a875e13aa3fa72ecf2b17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93697370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5204631a997d1234d7546fcb38705962f54c2530fc951f2daf73a073ad0969`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:23 GMT
ADD file:6e134e7958a9106ced0feb988945d71421340aa36ed7d8ad28fe5e91ab70df62 in / 
# Thu, 27 Jul 2023 23:47:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:53:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:54:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:54:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 28 Jul 2023 01:54:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
WORKDIR /var/www/html
# Fri, 28 Jul 2023 01:54:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 28 Jul 2023 01:54:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 28 Jul 2023 01:54:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Jul 2023 01:54:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:54:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 28 Jul 2023 01:54:18 GMT
USER adminer
# Fri, 28 Jul 2023 01:54:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 28 Jul 2023 01:54:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4909b03e906e0e2f8a83103a5b44c902afcad9d1bdcabcbc71058f3165c169e4`  
		Last Modified: Thu, 27 Jul 2023 23:52:31 GMT  
		Size: 53.3 MB (53289052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc8014a61d0196a352e2e57cc9351c1fa171b6a57905fe5921e55c00c7f634a`  
		Last Modified: Fri, 28 Jul 2023 01:55:01 GMT  
		Size: 39.0 MB (39018628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39aa6cfe13181ba6359c2b4fb46225c562e58e7cb27fb1591637c521f9d70d0`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df1820f29b009a397fd193ee10f17404280d3b9228f8b36daf5bb815bce0307`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a3cdb65e8cd3b2cb9e3aceddb9e95864743111dc589908c4805fca9f9bf9b8`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aee720253a711b2d402e08cb5cafdfa0cc5290a8f09f543174ff677614c67f`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 1.4 MB (1385448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f7c164596b5009b686a6803bc457fe549e5272341bfa787cc8f342ad43442`  
		Last Modified: Fri, 28 Jul 2023 01:54:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
