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
$ docker pull adminer@sha256:637bfc58e3812a5a5b02a4751346ee6014546c4cd668e0536f10819d9a5f070a
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
$ docker pull adminer@sha256:6d5d4a863c0f2e05e4a7a4dd5971a49afbe247bea72a6f7a2bf43586907cf541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95928958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db158f89ac5a0f88c7f20de5c8a1964aea8b3bbe6c772b62773b6733b1115a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:46:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb61091e569f770e9e3eeb7cba2097292a05032573e0eeee0b4f9718d93e7a4`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980a061c8abdef923339d3e40dc8918eefc42f128490760e6f166a29d229ee9`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5edff6748342b30b6494d181a231a8545de04b07f2897afa8df63d0b7c7b42`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 1.4 MB (1385369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4912d736721c397fde9b5cf74e064c968992ea39e919a1ed56e4b3660f52cfe`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v5

```console
$ docker pull adminer@sha256:899a343626fc8810d226a61458c3f6a1a36e7153fc4fbffe2ea3b135977deddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320bf705fd42d0c6893ab05d9973f52e44426b520ef97e9a2e18dfc82dd97d4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:34 GMT
USER adminer
# Wed, 03 May 2023 10:02:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 10:02:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28efee19a53301da773979aa1ba4e7647846067c0116d6d2aa19a68a749ede6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914e558bc32eeb3cc306e62fc22b35b4ff39ff8061e8ec4e2ca563462a2dcfe`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb403fa885ad9ffe9d7aa45c3e3ef20c78f9d6fa066399fd3404c87e30bf7b3e`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9edc465f41bf147e1b537181b104da72da0c30391b3a8d353024659319dbe6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:11b430e911b282f7b89fbb93e596bdc12369fc5502d67f0253b2429aee5a95e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87787988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6444ff0fe647446d31bc994a5630051f8c77ad362d7aaa7981e59302fbbcce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:32:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:33:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f561379c54146ddd2458f085e6a3d5b2204723c1240c2d2412edd4f5d3a2de`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a423c569fd2659253482ece7f04c260b9444afd58d620996d80135dd0a292`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194cbe1af54b30ec82b63fde8d09b7d85d8e69dbca36214566275e5bb1cc19ab`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.4 MB (1385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0c7c232efc74415f1761279f4279cf28a9370861defc0a690d3b6f6df5e52`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:195c05e88c549ff323f21435965c2e6677fe8cb8c5d8ee7b76a6de45404ccef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d9739cd4b1dcd81fff9a99d2363ec5d41f2ad74bdd346bd8fac26bbff9d06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:16:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:01 GMT
USER adminer
# Wed, 03 May 2023 17:17:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 17:17:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822087af0bdecd28923ab32fa9fc2e00566083e121bcaf67c0a2e6598c52d149`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5107c70315eac1012c7e38609673cccd890714b8fcf925196c063dcac78e70`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a12d03495dfb72be5d6277086be719ff559fa5ef937eef42793040eab4138a`  
		Last Modified: Wed, 03 May 2023 17:17:29 GMT  
		Size: 1.4 MB (1385335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca70bf37e696c8b2a1c3fad1f023f0c22794bcd2204a7ea0a5fa5de57829ff`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:3afb22ffb88d7612ed522f5f71033289471231e486f2739dc2af1de73d369e51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96980313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329cf5198a48a26609da2510580bac1d30b5de950ab4e17ced60caa13b2e526`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:21 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 05:09:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e92def6d1a89ad8be4edd1fe6307df529888e0918f9a3140d3cf1b564ddadd`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66948adf173d2026ceca9bbe5f0fc41445c77f6a235aacfe41969757971d9311`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754922f697aa1043924559c6fd3ba2e8a00783527cdec3d1af94206ccb13583`  
		Last Modified: Wed, 12 Apr 2023 05:09:52 GMT  
		Size: 1.4 MB (1385257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26a1d2ae2cc6358b97468b25ab918d87440698fac4d21e31dd28c92fa1ad7`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; mips64le

```console
$ docker pull adminer@sha256:a2481b949767cc9590da2052f75848628236dfa191907db80e507c0be8bb8e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ae62b8893e269cc48d8ade6f0338175abd327f2d9084130449ad757261007`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:41:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:41:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:41:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:41:44 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:41:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:41:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:42:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:42:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:42:52 GMT
USER adminer
# Wed, 12 Apr 2023 10:42:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 10:42:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7821bb95c14057d16890732aa8b3209cb604db2861e9363fb1f87ff7acae7a`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c203307aba5cfeda96f4e1c642688bf6ecdc19ffb20410957b67e44b440bd12`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c4cc17a0efce3fe1f0ab6cf44e5e46ee93b5a69d688cd6e6a13789c263cee`  
		Last Modified: Wed, 12 Apr 2023 10:45:04 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb383fb5d40f95724fe352abe8005c904ebb884b1afb7c1d84115a3fdaa51c1`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:a55a2c1ff24d027a36e46d24a34dcbb8e854ae5392eec85f9620ba60c7b58694
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101256116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735ee16dfbcee3a436e08438e55c6dd5114b673eec23b536b6b3a2f043a76ad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:20:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:20:40 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:21:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:21:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:21:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:21:34 GMT
USER adminer
# Wed, 12 Apr 2023 01:21:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 01:21:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79148517f43f66f402dd39c8ce8a6104a51fe03f3ed892be0eb40a2bf3ac513e`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc627fe6d1eed682ead8566e47d1e2328da8a1df7864e5a52ac7d20d815572`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7bbdc982c8e7f315e96ecd620a4c3a9d486beb72d36f89daddaaca429d14`  
		Last Modified: Wed, 12 Apr 2023 01:22:41 GMT  
		Size: 1.4 MB (1385746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1791e7b6ab1e976b9698dd6aed465ae1b9badc2ae1c6b6cb91197748b149d`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:5472a0984af7a0bcb4f370188898007842266789e4d9cd931aea7e05ffa0c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93694065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ca8c09f92e5cedf5daa80fc0e9a2a1b8b7e032b3719641feadef4e6294cf5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:22:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:22:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:22:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:22:58 GMT
USER adminer
# Wed, 12 Apr 2023 00:22:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 00:22:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23597fac1b0ce84055df85a56ef40909911286a24879b39f37200567f8e6e63`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88da54b627b523974ad186c33e429711d0e4968550bc7b513fae7d58b9f3de1`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c6c7cf39dd303de3dcb8c7c363f95bfcf24b7dfbd409557940ced6e28cd6e`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.4 MB (1385468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640f1f42167e00265be1505a797a83c7cf74946f47391b62064c6fd44e4fee4d`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:4215c4b37efabe690ea3c25fcbc385be134ee23fd2b74cd370bd36bc1a75127e
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
$ docker pull adminer@sha256:ecada04db15850cd30db2dbfa7fe5696cb718dbe27aa14166bc72c56ffc806d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95931654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e987db790e869ec7cee8fcc7c8f19d5d6a9893bc48967f30a54047c1166619`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:20 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 07:46:20 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:20 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:32 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:32 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5424e7ca02eeb6f2497271899a3f066ec180e00b64b95ea5e520074f4d1d96b`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e7c85b47d6154202655677b3e8e13c3cfdce6bf4bcac997b5a4b354f4ba323`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706bc8353e71fd2b4417cf0cfd9f90c7f8949898f1a83415800dcb8d29469978`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525591099069f500c0922ffff7fc5bc1162239467d2e3dfb1751565efb65f830`  
		Last Modified: Wed, 12 Apr 2023 07:47:06 GMT  
		Size: 1.4 MB (1385366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d565f58184c1cbadba9501e65d14920fe81133b7932680a1cd0c4d89e345214`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:558f302483df8ccda3c1fc58852f379155e64582ebd736b95894cb442c3e4c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91185946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c20b71a040d70be868f6b9df5a581feb1e789559115e3f135d92203882396af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:40 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 03 May 2023 10:02:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:41 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:54 GMT
USER adminer
# Wed, 03 May 2023 10:02:54 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301dd1f0c3eef7671629fb56c9a71a4205e156429bb4ea0c596c9d8e9984bd4`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01aee6a0464f241e20e1f733ad85346a7db9001a2219b4cfc23e57e13e1f2800`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe094b62e5e62a716dffc5e7768877a429a2f76291575f2e185123e74ebd6`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71b674a045dd23ea420791dc41cbd5d529be3870ce4f48136379812365a79e9`  
		Last Modified: Wed, 03 May 2023 10:03:29 GMT  
		Size: 1.4 MB (1385367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ab30ad769167e8caa776593bc92a729ebe8b3af4ad6b0a348d198781f9888`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:abca9c4e4ea6c74c24b5d44cf4790074caf0d030dc663596d49ce2fb3d4094bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87790703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1016b7a37351e06bc6123cf4f5dfb017400e19e1ad7abae67605e1666a82106d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:33:21 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 07:33:22 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:33:22 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:33:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:33 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:33 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce03f58793226edb8a26560156ce65072be14a02b0e6ba99c1b9e5fa0c0e97a`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac51c3d45ea1975984153e385b9ac4329062a51e680297de32b4bce3d14960e`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6872386e8c9f0fc484897fa6d15f427977c361776b8d572ad320fb6db5596d3`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00a5c4b366905c2c675dac63e188266d365b4625fb4345dbe7643d2f8b97678`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.4 MB (1385328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebca3f1cb817ef172f4525a4a39d894b67adc4925f88e02596ac698d1d63ba5d`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b27c31449632b9a65821b105ca7a98f4c07be23f490c615aa03a85535f55dc81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94327532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fe023c677da662d509e1abc3623a760d8f4cefcb81fb742f24df648a056f06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:17:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 03 May 2023 17:17:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:17:09 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:17:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:19 GMT
USER adminer
# Wed, 03 May 2023 17:17:19 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4668f312f76168b5ec5ba462cd882cdb5dd938580a0f9d0ea34136fdd309c72`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562094df7f95bedb11bf4ff8740f5df7952de583d03846e7c00d5de93af31879`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0826dfda302501033f4c7310b25337cfbc0d74c8fc7f0ebf783fb1cfa5736969`  
		Last Modified: Wed, 03 May 2023 17:17:51 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74a7a67f6c6592e208a69eab35b38e43d39e7d9b0fc229867c1c5a266007e50`  
		Last Modified: Wed, 03 May 2023 17:17:51 GMT  
		Size: 1.4 MB (1385319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf167363a0d5443d97b987ebeb028bb7549d031b7cf879b3873ff6fc85fa2d4`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:8923b59b2efac042cd9604405dbd538b7360dd01db66a80e38adfd4d4ec6e529
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96983029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88421d4c2f865cc4d870a678458661b2e812b119ff7abcfe566da428d56faa8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:28 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 05:09:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:29 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:42 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e201b91160b2c195f22b2a6dc5a195e7a02b9b4fc48235bcfe9e986fbea40c8`  
		Last Modified: Wed, 12 Apr 2023 05:10:18 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aaba726beb845320e15fb400887a3388466d8575690966ccb654c1aa847ad3`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1a23b0b94fca366fd869b376a81e8f6f2981611281c9a08adeca54aa842d5`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab80e71d640e3c22df2649623005063f27db1819649977f9b84cfdb3cbe92cf`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.4 MB (1385269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e397aa8ebdd609c1805b84a0dd0d00326d5ac78fa5cb35bfe3e00c7fab2028c`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:ec2503e1a3de2d5ca2bf316b67ed7e958a06136d8e39ec1fca269709ee875333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92616209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5676491ad5fd24ae8e97bb6069573498c98ee97cc7c061174219235d5e362be`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:43:16 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 10:43:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:43:26 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:43:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:43:32 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:43:35 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:43:39 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:44:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:44:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:44:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:44:38 GMT
USER adminer
# Wed, 12 Apr 2023 10:44:41 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bb3ffc932d05acd52c67296599ac0d3be51b729234eaa185ece820657514f2`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306049a9611831f6c79dc3ce39a6e611e574aa60fdac4717bb12d5f90e0e37ac`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85148145028f7b2b6299b17309acbbebfbcb5a1c359e091273d0b44c577de7a3`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed77d721f23feceaf7c9536e30e6db3cdc2c707ab31d2c80e4c786c159b9b01`  
		Last Modified: Wed, 12 Apr 2023 10:45:52 GMT  
		Size: 1.4 MB (1386310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4383371b6bafd035697e3c8e00264f5d6ca55333e1b168c40bde33c694f76e5`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:a035556296071d36e8a78a9fb4e6e566b030d8a04b2b961ce4a8874ed96af628
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3ec485bcf5a9208a03ffaaeffd1c6aa4408c565e11ce559ec629652c041a6a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:21:46 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 01:21:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:21:52 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:21:52 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:21:53 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:21:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:21:56 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:22:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:22:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:22:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:22:28 GMT
USER adminer
# Wed, 12 Apr 2023 01:22:28 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3013369f8e95d2665949e23f195080aa4f2f49cf345bb284164747c93462b1`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 2.7 KB (2716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18d6e52ddde5322eb2c03d3776619d697508750da16a1a0f486064299a5e67c`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bceca607df37463b3d4edc6d7f1fdbd6c21fa7d17c23ea3f37029b4fef209`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b5fb8c400ebb27e4513d1d29cc8ae5b6498e173b9ab0b418e0220d47eb350a`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.4 MB (1385683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f726494151054c4e7bb459b16a7c23209309d0be5221352f98027fed1913af`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:8fa537ed86e381074d357ce04c564bae5f507acf4188d3aa3e675a13e59716cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93696767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dcdae7e32897b325d716cb2131024c2344546e66d30f86aca7cb245499cf34`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:23:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 00:23:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:23:09 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:23:10 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:23:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:23:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:23:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:23:23 GMT
USER adminer
# Wed, 12 Apr 2023 00:23:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea6db7217edba5f8e49cbee261ad2ea9c96c10c83038a17071518884d1c81e6`  
		Last Modified: Wed, 12 Apr 2023 00:23:56 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881082d16d120a5a8f050b1cdc4abefb32e4247674e69a600e1b2f019bf126e0`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8b292e6ee64bda9332845e064826af581a04d7d69f09c6d33ea7f091742a1e`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792e42a83bf2a4947f67042cf923515e418d9ec97cf08b7b58924d139a59f9b`  
		Last Modified: Wed, 12 Apr 2023 00:23:56 GMT  
		Size: 1.4 MB (1385474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc070176a58f6105215209e8c6e8bcdc1d0f55c8540d08fb580df7d1f8b8ced`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:637bfc58e3812a5a5b02a4751346ee6014546c4cd668e0536f10819d9a5f070a
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
$ docker pull adminer@sha256:6d5d4a863c0f2e05e4a7a4dd5971a49afbe247bea72a6f7a2bf43586907cf541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95928958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db158f89ac5a0f88c7f20de5c8a1964aea8b3bbe6c772b62773b6733b1115a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:46:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb61091e569f770e9e3eeb7cba2097292a05032573e0eeee0b4f9718d93e7a4`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980a061c8abdef923339d3e40dc8918eefc42f128490760e6f166a29d229ee9`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5edff6748342b30b6494d181a231a8545de04b07f2897afa8df63d0b7c7b42`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 1.4 MB (1385369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4912d736721c397fde9b5cf74e064c968992ea39e919a1ed56e4b3660f52cfe`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:899a343626fc8810d226a61458c3f6a1a36e7153fc4fbffe2ea3b135977deddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320bf705fd42d0c6893ab05d9973f52e44426b520ef97e9a2e18dfc82dd97d4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:34 GMT
USER adminer
# Wed, 03 May 2023 10:02:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 10:02:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28efee19a53301da773979aa1ba4e7647846067c0116d6d2aa19a68a749ede6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914e558bc32eeb3cc306e62fc22b35b4ff39ff8061e8ec4e2ca563462a2dcfe`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb403fa885ad9ffe9d7aa45c3e3ef20c78f9d6fa066399fd3404c87e30bf7b3e`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9edc465f41bf147e1b537181b104da72da0c30391b3a8d353024659319dbe6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:11b430e911b282f7b89fbb93e596bdc12369fc5502d67f0253b2429aee5a95e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87787988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6444ff0fe647446d31bc994a5630051f8c77ad362d7aaa7981e59302fbbcce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:32:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:33:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f561379c54146ddd2458f085e6a3d5b2204723c1240c2d2412edd4f5d3a2de`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a423c569fd2659253482ece7f04c260b9444afd58d620996d80135dd0a292`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194cbe1af54b30ec82b63fde8d09b7d85d8e69dbca36214566275e5bb1cc19ab`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.4 MB (1385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0c7c232efc74415f1761279f4279cf28a9370861defc0a690d3b6f6df5e52`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:195c05e88c549ff323f21435965c2e6677fe8cb8c5d8ee7b76a6de45404ccef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d9739cd4b1dcd81fff9a99d2363ec5d41f2ad74bdd346bd8fac26bbff9d06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:16:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:01 GMT
USER adminer
# Wed, 03 May 2023 17:17:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 17:17:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822087af0bdecd28923ab32fa9fc2e00566083e121bcaf67c0a2e6598c52d149`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5107c70315eac1012c7e38609673cccd890714b8fcf925196c063dcac78e70`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a12d03495dfb72be5d6277086be719ff559fa5ef937eef42793040eab4138a`  
		Last Modified: Wed, 03 May 2023 17:17:29 GMT  
		Size: 1.4 MB (1385335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca70bf37e696c8b2a1c3fad1f023f0c22794bcd2204a7ea0a5fa5de57829ff`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:3afb22ffb88d7612ed522f5f71033289471231e486f2739dc2af1de73d369e51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96980313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329cf5198a48a26609da2510580bac1d30b5de950ab4e17ced60caa13b2e526`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:21 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 05:09:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e92def6d1a89ad8be4edd1fe6307df529888e0918f9a3140d3cf1b564ddadd`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66948adf173d2026ceca9bbe5f0fc41445c77f6a235aacfe41969757971d9311`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754922f697aa1043924559c6fd3ba2e8a00783527cdec3d1af94206ccb13583`  
		Last Modified: Wed, 12 Apr 2023 05:09:52 GMT  
		Size: 1.4 MB (1385257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26a1d2ae2cc6358b97468b25ab918d87440698fac4d21e31dd28c92fa1ad7`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:a2481b949767cc9590da2052f75848628236dfa191907db80e507c0be8bb8e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ae62b8893e269cc48d8ade6f0338175abd327f2d9084130449ad757261007`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:41:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:41:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:41:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:41:44 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:41:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:41:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:42:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:42:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:42:52 GMT
USER adminer
# Wed, 12 Apr 2023 10:42:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 10:42:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7821bb95c14057d16890732aa8b3209cb604db2861e9363fb1f87ff7acae7a`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c203307aba5cfeda96f4e1c642688bf6ecdc19ffb20410957b67e44b440bd12`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c4cc17a0efce3fe1f0ab6cf44e5e46ee93b5a69d688cd6e6a13789c263cee`  
		Last Modified: Wed, 12 Apr 2023 10:45:04 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb383fb5d40f95724fe352abe8005c904ebb884b1afb7c1d84115a3fdaa51c1`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:a55a2c1ff24d027a36e46d24a34dcbb8e854ae5392eec85f9620ba60c7b58694
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101256116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735ee16dfbcee3a436e08438e55c6dd5114b673eec23b536b6b3a2f043a76ad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:20:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:20:40 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:21:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:21:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:21:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:21:34 GMT
USER adminer
# Wed, 12 Apr 2023 01:21:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 01:21:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79148517f43f66f402dd39c8ce8a6104a51fe03f3ed892be0eb40a2bf3ac513e`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc627fe6d1eed682ead8566e47d1e2328da8a1df7864e5a52ac7d20d815572`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7bbdc982c8e7f315e96ecd620a4c3a9d486beb72d36f89daddaaca429d14`  
		Last Modified: Wed, 12 Apr 2023 01:22:41 GMT  
		Size: 1.4 MB (1385746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1791e7b6ab1e976b9698dd6aed465ae1b9badc2ae1c6b6cb91197748b149d`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:5472a0984af7a0bcb4f370188898007842266789e4d9cd931aea7e05ffa0c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93694065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ca8c09f92e5cedf5daa80fc0e9a2a1b8b7e032b3719641feadef4e6294cf5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:22:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:22:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:22:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:22:58 GMT
USER adminer
# Wed, 12 Apr 2023 00:22:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 00:22:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23597fac1b0ce84055df85a56ef40909911286a24879b39f37200567f8e6e63`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88da54b627b523974ad186c33e429711d0e4968550bc7b513fae7d58b9f3de1`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c6c7cf39dd303de3dcb8c7c363f95bfcf24b7dfbd409557940ced6e28cd6e`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.4 MB (1385468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640f1f42167e00265be1505a797a83c7cf74946f47391b62064c6fd44e4fee4d`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1`

```console
$ docker pull adminer@sha256:637bfc58e3812a5a5b02a4751346ee6014546c4cd668e0536f10819d9a5f070a
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
$ docker pull adminer@sha256:6d5d4a863c0f2e05e4a7a4dd5971a49afbe247bea72a6f7a2bf43586907cf541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95928958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db158f89ac5a0f88c7f20de5c8a1964aea8b3bbe6c772b62773b6733b1115a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:46:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb61091e569f770e9e3eeb7cba2097292a05032573e0eeee0b4f9718d93e7a4`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980a061c8abdef923339d3e40dc8918eefc42f128490760e6f166a29d229ee9`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5edff6748342b30b6494d181a231a8545de04b07f2897afa8df63d0b7c7b42`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 1.4 MB (1385369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4912d736721c397fde9b5cf74e064c968992ea39e919a1ed56e4b3660f52cfe`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v5

```console
$ docker pull adminer@sha256:899a343626fc8810d226a61458c3f6a1a36e7153fc4fbffe2ea3b135977deddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320bf705fd42d0c6893ab05d9973f52e44426b520ef97e9a2e18dfc82dd97d4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:34 GMT
USER adminer
# Wed, 03 May 2023 10:02:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 10:02:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28efee19a53301da773979aa1ba4e7647846067c0116d6d2aa19a68a749ede6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914e558bc32eeb3cc306e62fc22b35b4ff39ff8061e8ec4e2ca563462a2dcfe`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb403fa885ad9ffe9d7aa45c3e3ef20c78f9d6fa066399fd3404c87e30bf7b3e`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9edc465f41bf147e1b537181b104da72da0c30391b3a8d353024659319dbe6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v7

```console
$ docker pull adminer@sha256:11b430e911b282f7b89fbb93e596bdc12369fc5502d67f0253b2429aee5a95e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87787988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6444ff0fe647446d31bc994a5630051f8c77ad362d7aaa7981e59302fbbcce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:32:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:33:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f561379c54146ddd2458f085e6a3d5b2204723c1240c2d2412edd4f5d3a2de`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a423c569fd2659253482ece7f04c260b9444afd58d620996d80135dd0a292`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194cbe1af54b30ec82b63fde8d09b7d85d8e69dbca36214566275e5bb1cc19ab`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.4 MB (1385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0c7c232efc74415f1761279f4279cf28a9370861defc0a690d3b6f6df5e52`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:195c05e88c549ff323f21435965c2e6677fe8cb8c5d8ee7b76a6de45404ccef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d9739cd4b1dcd81fff9a99d2363ec5d41f2ad74bdd346bd8fac26bbff9d06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:16:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:01 GMT
USER adminer
# Wed, 03 May 2023 17:17:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 17:17:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822087af0bdecd28923ab32fa9fc2e00566083e121bcaf67c0a2e6598c52d149`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5107c70315eac1012c7e38609673cccd890714b8fcf925196c063dcac78e70`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a12d03495dfb72be5d6277086be719ff559fa5ef937eef42793040eab4138a`  
		Last Modified: Wed, 03 May 2023 17:17:29 GMT  
		Size: 1.4 MB (1385335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca70bf37e696c8b2a1c3fad1f023f0c22794bcd2204a7ea0a5fa5de57829ff`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; 386

```console
$ docker pull adminer@sha256:3afb22ffb88d7612ed522f5f71033289471231e486f2739dc2af1de73d369e51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96980313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329cf5198a48a26609da2510580bac1d30b5de950ab4e17ced60caa13b2e526`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:21 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 05:09:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e92def6d1a89ad8be4edd1fe6307df529888e0918f9a3140d3cf1b564ddadd`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66948adf173d2026ceca9bbe5f0fc41445c77f6a235aacfe41969757971d9311`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754922f697aa1043924559c6fd3ba2e8a00783527cdec3d1af94206ccb13583`  
		Last Modified: Wed, 12 Apr 2023 05:09:52 GMT  
		Size: 1.4 MB (1385257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26a1d2ae2cc6358b97468b25ab918d87440698fac4d21e31dd28c92fa1ad7`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; mips64le

```console
$ docker pull adminer@sha256:a2481b949767cc9590da2052f75848628236dfa191907db80e507c0be8bb8e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ae62b8893e269cc48d8ade6f0338175abd327f2d9084130449ad757261007`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:41:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:41:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:41:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:41:44 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:41:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:41:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:42:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:42:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:42:52 GMT
USER adminer
# Wed, 12 Apr 2023 10:42:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 10:42:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7821bb95c14057d16890732aa8b3209cb604db2861e9363fb1f87ff7acae7a`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c203307aba5cfeda96f4e1c642688bf6ecdc19ffb20410957b67e44b440bd12`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c4cc17a0efce3fe1f0ab6cf44e5e46ee93b5a69d688cd6e6a13789c263cee`  
		Last Modified: Wed, 12 Apr 2023 10:45:04 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb383fb5d40f95724fe352abe8005c904ebb884b1afb7c1d84115a3fdaa51c1`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; ppc64le

```console
$ docker pull adminer@sha256:a55a2c1ff24d027a36e46d24a34dcbb8e854ae5392eec85f9620ba60c7b58694
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101256116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735ee16dfbcee3a436e08438e55c6dd5114b673eec23b536b6b3a2f043a76ad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:20:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:20:40 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:21:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:21:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:21:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:21:34 GMT
USER adminer
# Wed, 12 Apr 2023 01:21:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 01:21:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79148517f43f66f402dd39c8ce8a6104a51fe03f3ed892be0eb40a2bf3ac513e`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc627fe6d1eed682ead8566e47d1e2328da8a1df7864e5a52ac7d20d815572`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7bbdc982c8e7f315e96ecd620a4c3a9d486beb72d36f89daddaaca429d14`  
		Last Modified: Wed, 12 Apr 2023 01:22:41 GMT  
		Size: 1.4 MB (1385746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1791e7b6ab1e976b9698dd6aed465ae1b9badc2ae1c6b6cb91197748b149d`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; s390x

```console
$ docker pull adminer@sha256:5472a0984af7a0bcb4f370188898007842266789e4d9cd931aea7e05ffa0c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93694065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ca8c09f92e5cedf5daa80fc0e9a2a1b8b7e032b3719641feadef4e6294cf5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:22:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:22:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:22:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:22:58 GMT
USER adminer
# Wed, 12 Apr 2023 00:22:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 00:22:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23597fac1b0ce84055df85a56ef40909911286a24879b39f37200567f8e6e63`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88da54b627b523974ad186c33e429711d0e4968550bc7b513fae7d58b9f3de1`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c6c7cf39dd303de3dcb8c7c363f95bfcf24b7dfbd409557940ced6e28cd6e`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.4 MB (1385468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640f1f42167e00265be1505a797a83c7cf74946f47391b62064c6fd44e4fee4d`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-fastcgi`

```console
$ docker pull adminer@sha256:4215c4b37efabe690ea3c25fcbc385be134ee23fd2b74cd370bd36bc1a75127e
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
$ docker pull adminer@sha256:ecada04db15850cd30db2dbfa7fe5696cb718dbe27aa14166bc72c56ffc806d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95931654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e987db790e869ec7cee8fcc7c8f19d5d6a9893bc48967f30a54047c1166619`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:20 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 07:46:20 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:20 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:32 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:32 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5424e7ca02eeb6f2497271899a3f066ec180e00b64b95ea5e520074f4d1d96b`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e7c85b47d6154202655677b3e8e13c3cfdce6bf4bcac997b5a4b354f4ba323`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706bc8353e71fd2b4417cf0cfd9f90c7f8949898f1a83415800dcb8d29469978`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525591099069f500c0922ffff7fc5bc1162239467d2e3dfb1751565efb65f830`  
		Last Modified: Wed, 12 Apr 2023 07:47:06 GMT  
		Size: 1.4 MB (1385366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d565f58184c1cbadba9501e65d14920fe81133b7932680a1cd0c4d89e345214`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:558f302483df8ccda3c1fc58852f379155e64582ebd736b95894cb442c3e4c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91185946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c20b71a040d70be868f6b9df5a581feb1e789559115e3f135d92203882396af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:40 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 03 May 2023 10:02:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:41 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:54 GMT
USER adminer
# Wed, 03 May 2023 10:02:54 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301dd1f0c3eef7671629fb56c9a71a4205e156429bb4ea0c596c9d8e9984bd4`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01aee6a0464f241e20e1f733ad85346a7db9001a2219b4cfc23e57e13e1f2800`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe094b62e5e62a716dffc5e7768877a429a2f76291575f2e185123e74ebd6`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71b674a045dd23ea420791dc41cbd5d529be3870ce4f48136379812365a79e9`  
		Last Modified: Wed, 03 May 2023 10:03:29 GMT  
		Size: 1.4 MB (1385367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ab30ad769167e8caa776593bc92a729ebe8b3af4ad6b0a348d198781f9888`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:abca9c4e4ea6c74c24b5d44cf4790074caf0d030dc663596d49ce2fb3d4094bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87790703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1016b7a37351e06bc6123cf4f5dfb017400e19e1ad7abae67605e1666a82106d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:33:21 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 07:33:22 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:33:22 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:33:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:33 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:33 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce03f58793226edb8a26560156ce65072be14a02b0e6ba99c1b9e5fa0c0e97a`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac51c3d45ea1975984153e385b9ac4329062a51e680297de32b4bce3d14960e`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6872386e8c9f0fc484897fa6d15f427977c361776b8d572ad320fb6db5596d3`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00a5c4b366905c2c675dac63e188266d365b4625fb4345dbe7643d2f8b97678`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.4 MB (1385328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebca3f1cb817ef172f4525a4a39d894b67adc4925f88e02596ac698d1d63ba5d`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b27c31449632b9a65821b105ca7a98f4c07be23f490c615aa03a85535f55dc81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94327532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fe023c677da662d509e1abc3623a760d8f4cefcb81fb742f24df648a056f06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:17:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 03 May 2023 17:17:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:17:09 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:17:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:19 GMT
USER adminer
# Wed, 03 May 2023 17:17:19 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4668f312f76168b5ec5ba462cd882cdb5dd938580a0f9d0ea34136fdd309c72`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562094df7f95bedb11bf4ff8740f5df7952de583d03846e7c00d5de93af31879`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0826dfda302501033f4c7310b25337cfbc0d74c8fc7f0ebf783fb1cfa5736969`  
		Last Modified: Wed, 03 May 2023 17:17:51 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74a7a67f6c6592e208a69eab35b38e43d39e7d9b0fc229867c1c5a266007e50`  
		Last Modified: Wed, 03 May 2023 17:17:51 GMT  
		Size: 1.4 MB (1385319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf167363a0d5443d97b987ebeb028bb7549d031b7cf879b3873ff6fc85fa2d4`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:8923b59b2efac042cd9604405dbd538b7360dd01db66a80e38adfd4d4ec6e529
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96983029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88421d4c2f865cc4d870a678458661b2e812b119ff7abcfe566da428d56faa8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:28 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 05:09:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:29 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:42 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e201b91160b2c195f22b2a6dc5a195e7a02b9b4fc48235bcfe9e986fbea40c8`  
		Last Modified: Wed, 12 Apr 2023 05:10:18 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aaba726beb845320e15fb400887a3388466d8575690966ccb654c1aa847ad3`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1a23b0b94fca366fd869b376a81e8f6f2981611281c9a08adeca54aa842d5`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab80e71d640e3c22df2649623005063f27db1819649977f9b84cfdb3cbe92cf`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.4 MB (1385269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e397aa8ebdd609c1805b84a0dd0d00326d5ac78fa5cb35bfe3e00c7fab2028c`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:ec2503e1a3de2d5ca2bf316b67ed7e958a06136d8e39ec1fca269709ee875333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92616209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5676491ad5fd24ae8e97bb6069573498c98ee97cc7c061174219235d5e362be`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:43:16 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 10:43:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:43:26 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:43:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:43:32 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:43:35 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:43:39 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:44:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:44:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:44:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:44:38 GMT
USER adminer
# Wed, 12 Apr 2023 10:44:41 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bb3ffc932d05acd52c67296599ac0d3be51b729234eaa185ece820657514f2`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306049a9611831f6c79dc3ce39a6e611e574aa60fdac4717bb12d5f90e0e37ac`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85148145028f7b2b6299b17309acbbebfbcb5a1c359e091273d0b44c577de7a3`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed77d721f23feceaf7c9536e30e6db3cdc2c707ab31d2c80e4c786c159b9b01`  
		Last Modified: Wed, 12 Apr 2023 10:45:52 GMT  
		Size: 1.4 MB (1386310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4383371b6bafd035697e3c8e00264f5d6ca55333e1b168c40bde33c694f76e5`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:a035556296071d36e8a78a9fb4e6e566b030d8a04b2b961ce4a8874ed96af628
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3ec485bcf5a9208a03ffaaeffd1c6aa4408c565e11ce559ec629652c041a6a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:21:46 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 01:21:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:21:52 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:21:52 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:21:53 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:21:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:21:56 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:22:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:22:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:22:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:22:28 GMT
USER adminer
# Wed, 12 Apr 2023 01:22:28 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3013369f8e95d2665949e23f195080aa4f2f49cf345bb284164747c93462b1`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 2.7 KB (2716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18d6e52ddde5322eb2c03d3776619d697508750da16a1a0f486064299a5e67c`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bceca607df37463b3d4edc6d7f1fdbd6c21fa7d17c23ea3f37029b4fef209`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b5fb8c400ebb27e4513d1d29cc8ae5b6498e173b9ab0b418e0220d47eb350a`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.4 MB (1385683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f726494151054c4e7bb459b16a7c23209309d0be5221352f98027fed1913af`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:8fa537ed86e381074d357ce04c564bae5f507acf4188d3aa3e675a13e59716cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93696767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dcdae7e32897b325d716cb2131024c2344546e66d30f86aca7cb245499cf34`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:23:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 00:23:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:23:09 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:23:10 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:23:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:23:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:23:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:23:23 GMT
USER adminer
# Wed, 12 Apr 2023 00:23:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea6db7217edba5f8e49cbee261ad2ea9c96c10c83038a17071518884d1c81e6`  
		Last Modified: Wed, 12 Apr 2023 00:23:56 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881082d16d120a5a8f050b1cdc4abefb32e4247674e69a600e1b2f019bf126e0`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8b292e6ee64bda9332845e064826af581a04d7d69f09c6d33ea7f091742a1e`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792e42a83bf2a4947f67042cf923515e418d9ec97cf08b7b58924d139a59f9b`  
		Last Modified: Wed, 12 Apr 2023 00:23:56 GMT  
		Size: 1.4 MB (1385474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc070176a58f6105215209e8c6e8bcdc1d0f55c8540d08fb580df7d1f8b8ced`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-standalone`

```console
$ docker pull adminer@sha256:637bfc58e3812a5a5b02a4751346ee6014546c4cd668e0536f10819d9a5f070a
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
$ docker pull adminer@sha256:6d5d4a863c0f2e05e4a7a4dd5971a49afbe247bea72a6f7a2bf43586907cf541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95928958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db158f89ac5a0f88c7f20de5c8a1964aea8b3bbe6c772b62773b6733b1115a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:46:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb61091e569f770e9e3eeb7cba2097292a05032573e0eeee0b4f9718d93e7a4`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980a061c8abdef923339d3e40dc8918eefc42f128490760e6f166a29d229ee9`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5edff6748342b30b6494d181a231a8545de04b07f2897afa8df63d0b7c7b42`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 1.4 MB (1385369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4912d736721c397fde9b5cf74e064c968992ea39e919a1ed56e4b3660f52cfe`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:899a343626fc8810d226a61458c3f6a1a36e7153fc4fbffe2ea3b135977deddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320bf705fd42d0c6893ab05d9973f52e44426b520ef97e9a2e18dfc82dd97d4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:34 GMT
USER adminer
# Wed, 03 May 2023 10:02:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 10:02:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28efee19a53301da773979aa1ba4e7647846067c0116d6d2aa19a68a749ede6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914e558bc32eeb3cc306e62fc22b35b4ff39ff8061e8ec4e2ca563462a2dcfe`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb403fa885ad9ffe9d7aa45c3e3ef20c78f9d6fa066399fd3404c87e30bf7b3e`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9edc465f41bf147e1b537181b104da72da0c30391b3a8d353024659319dbe6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:11b430e911b282f7b89fbb93e596bdc12369fc5502d67f0253b2429aee5a95e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87787988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6444ff0fe647446d31bc994a5630051f8c77ad362d7aaa7981e59302fbbcce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:32:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:33:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f561379c54146ddd2458f085e6a3d5b2204723c1240c2d2412edd4f5d3a2de`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a423c569fd2659253482ece7f04c260b9444afd58d620996d80135dd0a292`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194cbe1af54b30ec82b63fde8d09b7d85d8e69dbca36214566275e5bb1cc19ab`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.4 MB (1385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0c7c232efc74415f1761279f4279cf28a9370861defc0a690d3b6f6df5e52`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:195c05e88c549ff323f21435965c2e6677fe8cb8c5d8ee7b76a6de45404ccef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d9739cd4b1dcd81fff9a99d2363ec5d41f2ad74bdd346bd8fac26bbff9d06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:16:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:01 GMT
USER adminer
# Wed, 03 May 2023 17:17:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 17:17:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822087af0bdecd28923ab32fa9fc2e00566083e121bcaf67c0a2e6598c52d149`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5107c70315eac1012c7e38609673cccd890714b8fcf925196c063dcac78e70`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a12d03495dfb72be5d6277086be719ff559fa5ef937eef42793040eab4138a`  
		Last Modified: Wed, 03 May 2023 17:17:29 GMT  
		Size: 1.4 MB (1385335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca70bf37e696c8b2a1c3fad1f023f0c22794bcd2204a7ea0a5fa5de57829ff`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; 386

```console
$ docker pull adminer@sha256:3afb22ffb88d7612ed522f5f71033289471231e486f2739dc2af1de73d369e51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96980313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329cf5198a48a26609da2510580bac1d30b5de950ab4e17ced60caa13b2e526`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:21 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 05:09:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e92def6d1a89ad8be4edd1fe6307df529888e0918f9a3140d3cf1b564ddadd`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66948adf173d2026ceca9bbe5f0fc41445c77f6a235aacfe41969757971d9311`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754922f697aa1043924559c6fd3ba2e8a00783527cdec3d1af94206ccb13583`  
		Last Modified: Wed, 12 Apr 2023 05:09:52 GMT  
		Size: 1.4 MB (1385257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26a1d2ae2cc6358b97468b25ab918d87440698fac4d21e31dd28c92fa1ad7`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:a2481b949767cc9590da2052f75848628236dfa191907db80e507c0be8bb8e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ae62b8893e269cc48d8ade6f0338175abd327f2d9084130449ad757261007`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:41:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:41:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:41:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:41:44 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:41:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:41:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:42:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:42:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:42:52 GMT
USER adminer
# Wed, 12 Apr 2023 10:42:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 10:42:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7821bb95c14057d16890732aa8b3209cb604db2861e9363fb1f87ff7acae7a`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c203307aba5cfeda96f4e1c642688bf6ecdc19ffb20410957b67e44b440bd12`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c4cc17a0efce3fe1f0ab6cf44e5e46ee93b5a69d688cd6e6a13789c263cee`  
		Last Modified: Wed, 12 Apr 2023 10:45:04 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb383fb5d40f95724fe352abe8005c904ebb884b1afb7c1d84115a3fdaa51c1`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:a55a2c1ff24d027a36e46d24a34dcbb8e854ae5392eec85f9620ba60c7b58694
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101256116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735ee16dfbcee3a436e08438e55c6dd5114b673eec23b536b6b3a2f043a76ad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:20:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:20:40 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:21:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:21:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:21:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:21:34 GMT
USER adminer
# Wed, 12 Apr 2023 01:21:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 01:21:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79148517f43f66f402dd39c8ce8a6104a51fe03f3ed892be0eb40a2bf3ac513e`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc627fe6d1eed682ead8566e47d1e2328da8a1df7864e5a52ac7d20d815572`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7bbdc982c8e7f315e96ecd620a4c3a9d486beb72d36f89daddaaca429d14`  
		Last Modified: Wed, 12 Apr 2023 01:22:41 GMT  
		Size: 1.4 MB (1385746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1791e7b6ab1e976b9698dd6aed465ae1b9badc2ae1c6b6cb91197748b149d`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:5472a0984af7a0bcb4f370188898007842266789e4d9cd931aea7e05ffa0c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93694065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ca8c09f92e5cedf5daa80fc0e9a2a1b8b7e032b3719641feadef4e6294cf5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:22:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:22:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:22:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:22:58 GMT
USER adminer
# Wed, 12 Apr 2023 00:22:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 00:22:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23597fac1b0ce84055df85a56ef40909911286a24879b39f37200567f8e6e63`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88da54b627b523974ad186c33e429711d0e4968550bc7b513fae7d58b9f3de1`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c6c7cf39dd303de3dcb8c7c363f95bfcf24b7dfbd409557940ced6e28cd6e`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.4 MB (1385468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640f1f42167e00265be1505a797a83c7cf74946f47391b62064c6fd44e4fee4d`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:4215c4b37efabe690ea3c25fcbc385be134ee23fd2b74cd370bd36bc1a75127e
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
$ docker pull adminer@sha256:ecada04db15850cd30db2dbfa7fe5696cb718dbe27aa14166bc72c56ffc806d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95931654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e987db790e869ec7cee8fcc7c8f19d5d6a9893bc48967f30a54047c1166619`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:20 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 07:46:20 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:20 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:21 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:32 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:32 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5424e7ca02eeb6f2497271899a3f066ec180e00b64b95ea5e520074f4d1d96b`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e7c85b47d6154202655677b3e8e13c3cfdce6bf4bcac997b5a4b354f4ba323`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706bc8353e71fd2b4417cf0cfd9f90c7f8949898f1a83415800dcb8d29469978`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525591099069f500c0922ffff7fc5bc1162239467d2e3dfb1751565efb65f830`  
		Last Modified: Wed, 12 Apr 2023 07:47:06 GMT  
		Size: 1.4 MB (1385366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d565f58184c1cbadba9501e65d14920fe81133b7932680a1cd0c4d89e345214`  
		Last Modified: Wed, 12 Apr 2023 07:47:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:558f302483df8ccda3c1fc58852f379155e64582ebd736b95894cb442c3e4c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91185946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c20b71a040d70be868f6b9df5a581feb1e789559115e3f135d92203882396af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:40 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 03 May 2023 10:02:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:41 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:54 GMT
USER adminer
# Wed, 03 May 2023 10:02:54 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301dd1f0c3eef7671629fb56c9a71a4205e156429bb4ea0c596c9d8e9984bd4`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01aee6a0464f241e20e1f733ad85346a7db9001a2219b4cfc23e57e13e1f2800`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168fe094b62e5e62a716dffc5e7768877a429a2f76291575f2e185123e74ebd6`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71b674a045dd23ea420791dc41cbd5d529be3870ce4f48136379812365a79e9`  
		Last Modified: Wed, 03 May 2023 10:03:29 GMT  
		Size: 1.4 MB (1385367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ab30ad769167e8caa776593bc92a729ebe8b3af4ad6b0a348d198781f9888`  
		Last Modified: Wed, 03 May 2023 10:03:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:abca9c4e4ea6c74c24b5d44cf4790074caf0d030dc663596d49ce2fb3d4094bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87790703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1016b7a37351e06bc6123cf4f5dfb017400e19e1ad7abae67605e1666a82106d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:33:21 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 07:33:22 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:33:22 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:33:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:33:22 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:33 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:33 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce03f58793226edb8a26560156ce65072be14a02b0e6ba99c1b9e5fa0c0e97a`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac51c3d45ea1975984153e385b9ac4329062a51e680297de32b4bce3d14960e`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6872386e8c9f0fc484897fa6d15f427977c361776b8d572ad320fb6db5596d3`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00a5c4b366905c2c675dac63e188266d365b4625fb4345dbe7643d2f8b97678`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 1.4 MB (1385328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebca3f1cb817ef172f4525a4a39d894b67adc4925f88e02596ac698d1d63ba5d`  
		Last Modified: Wed, 12 Apr 2023 07:34:08 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b27c31449632b9a65821b105ca7a98f4c07be23f490c615aa03a85535f55dc81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94327532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fe023c677da662d509e1abc3623a760d8f4cefcb81fb742f24df648a056f06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:17:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 03 May 2023 17:17:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:17:09 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:17:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:17:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:19 GMT
USER adminer
# Wed, 03 May 2023 17:17:19 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4668f312f76168b5ec5ba462cd882cdb5dd938580a0f9d0ea34136fdd309c72`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562094df7f95bedb11bf4ff8740f5df7952de583d03846e7c00d5de93af31879`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0826dfda302501033f4c7310b25337cfbc0d74c8fc7f0ebf783fb1cfa5736969`  
		Last Modified: Wed, 03 May 2023 17:17:51 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74a7a67f6c6592e208a69eab35b38e43d39e7d9b0fc229867c1c5a266007e50`  
		Last Modified: Wed, 03 May 2023 17:17:51 GMT  
		Size: 1.4 MB (1385319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf167363a0d5443d97b987ebeb028bb7549d031b7cf879b3873ff6fc85fa2d4`  
		Last Modified: Wed, 03 May 2023 17:17:50 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:8923b59b2efac042cd9604405dbd538b7360dd01db66a80e38adfd4d4ec6e529
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96983029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88421d4c2f865cc4d870a678458661b2e812b119ff7abcfe566da428d56faa8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:28 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 05:09:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:29 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:42 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e201b91160b2c195f22b2a6dc5a195e7a02b9b4fc48235bcfe9e986fbea40c8`  
		Last Modified: Wed, 12 Apr 2023 05:10:18 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aaba726beb845320e15fb400887a3388466d8575690966ccb654c1aa847ad3`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b1a23b0b94fca366fd869b376a81e8f6f2981611281c9a08adeca54aa842d5`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab80e71d640e3c22df2649623005063f27db1819649977f9b84cfdb3cbe92cf`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 1.4 MB (1385269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e397aa8ebdd609c1805b84a0dd0d00326d5ac78fa5cb35bfe3e00c7fab2028c`  
		Last Modified: Wed, 12 Apr 2023 05:10:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:ec2503e1a3de2d5ca2bf316b67ed7e958a06136d8e39ec1fca269709ee875333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92616209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5676491ad5fd24ae8e97bb6069573498c98ee97cc7c061174219235d5e362be`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:43:16 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 10:43:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:43:26 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:43:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:43:32 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:43:35 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:43:39 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:44:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:44:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:44:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:44:38 GMT
USER adminer
# Wed, 12 Apr 2023 10:44:41 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bb3ffc932d05acd52c67296599ac0d3be51b729234eaa185ece820657514f2`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306049a9611831f6c79dc3ce39a6e611e574aa60fdac4717bb12d5f90e0e37ac`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85148145028f7b2b6299b17309acbbebfbcb5a1c359e091273d0b44c577de7a3`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed77d721f23feceaf7c9536e30e6db3cdc2c707ab31d2c80e4c786c159b9b01`  
		Last Modified: Wed, 12 Apr 2023 10:45:52 GMT  
		Size: 1.4 MB (1386310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4383371b6bafd035697e3c8e00264f5d6ca55333e1b168c40bde33c694f76e5`  
		Last Modified: Wed, 12 Apr 2023 10:45:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:a035556296071d36e8a78a9fb4e6e566b030d8a04b2b961ce4a8874ed96af628
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3ec485bcf5a9208a03ffaaeffd1c6aa4408c565e11ce559ec629652c041a6a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:21:46 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 01:21:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:21:52 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:21:52 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:21:53 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:21:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:21:56 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:22:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:22:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:22:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:22:28 GMT
USER adminer
# Wed, 12 Apr 2023 01:22:28 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3013369f8e95d2665949e23f195080aa4f2f49cf345bb284164747c93462b1`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 2.7 KB (2716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18d6e52ddde5322eb2c03d3776619d697508750da16a1a0f486064299a5e67c`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bceca607df37463b3d4edc6d7f1fdbd6c21fa7d17c23ea3f37029b4fef209`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b5fb8c400ebb27e4513d1d29cc8ae5b6498e173b9ab0b418e0220d47eb350a`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 1.4 MB (1385683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f726494151054c4e7bb459b16a7c23209309d0be5221352f98027fed1913af`  
		Last Modified: Wed, 12 Apr 2023 01:23:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:8fa537ed86e381074d357ce04c564bae5f507acf4188d3aa3e675a13e59716cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93696767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dcdae7e32897b325d716cb2131024c2344546e66d30f86aca7cb245499cf34`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:23:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 12 Apr 2023 00:23:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:23:09 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:23:10 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:23:10 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:23:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:23:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:23:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:23:23 GMT
USER adminer
# Wed, 12 Apr 2023 00:23:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea6db7217edba5f8e49cbee261ad2ea9c96c10c83038a17071518884d1c81e6`  
		Last Modified: Wed, 12 Apr 2023 00:23:56 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881082d16d120a5a8f050b1cdc4abefb32e4247674e69a600e1b2f019bf126e0`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8b292e6ee64bda9332845e064826af581a04d7d69f09c6d33ea7f091742a1e`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792e42a83bf2a4947f67042cf923515e418d9ec97cf08b7b58924d139a59f9b`  
		Last Modified: Wed, 12 Apr 2023 00:23:56 GMT  
		Size: 1.4 MB (1385474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc070176a58f6105215209e8c6e8bcdc1d0f55c8540d08fb580df7d1f8b8ced`  
		Last Modified: Wed, 12 Apr 2023 00:23:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:637bfc58e3812a5a5b02a4751346ee6014546c4cd668e0536f10819d9a5f070a
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
$ docker pull adminer@sha256:6d5d4a863c0f2e05e4a7a4dd5971a49afbe247bea72a6f7a2bf43586907cf541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95928958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db158f89ac5a0f88c7f20de5c8a1964aea8b3bbe6c772b62773b6733b1115a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:46:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb61091e569f770e9e3eeb7cba2097292a05032573e0eeee0b4f9718d93e7a4`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980a061c8abdef923339d3e40dc8918eefc42f128490760e6f166a29d229ee9`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5edff6748342b30b6494d181a231a8545de04b07f2897afa8df63d0b7c7b42`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 1.4 MB (1385369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4912d736721c397fde9b5cf74e064c968992ea39e919a1ed56e4b3660f52cfe`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:899a343626fc8810d226a61458c3f6a1a36e7153fc4fbffe2ea3b135977deddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320bf705fd42d0c6893ab05d9973f52e44426b520ef97e9a2e18dfc82dd97d4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:34 GMT
USER adminer
# Wed, 03 May 2023 10:02:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 10:02:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28efee19a53301da773979aa1ba4e7647846067c0116d6d2aa19a68a749ede6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914e558bc32eeb3cc306e62fc22b35b4ff39ff8061e8ec4e2ca563462a2dcfe`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb403fa885ad9ffe9d7aa45c3e3ef20c78f9d6fa066399fd3404c87e30bf7b3e`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9edc465f41bf147e1b537181b104da72da0c30391b3a8d353024659319dbe6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:11b430e911b282f7b89fbb93e596bdc12369fc5502d67f0253b2429aee5a95e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87787988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6444ff0fe647446d31bc994a5630051f8c77ad362d7aaa7981e59302fbbcce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:32:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:33:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f561379c54146ddd2458f085e6a3d5b2204723c1240c2d2412edd4f5d3a2de`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a423c569fd2659253482ece7f04c260b9444afd58d620996d80135dd0a292`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194cbe1af54b30ec82b63fde8d09b7d85d8e69dbca36214566275e5bb1cc19ab`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.4 MB (1385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0c7c232efc74415f1761279f4279cf28a9370861defc0a690d3b6f6df5e52`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:195c05e88c549ff323f21435965c2e6677fe8cb8c5d8ee7b76a6de45404ccef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d9739cd4b1dcd81fff9a99d2363ec5d41f2ad74bdd346bd8fac26bbff9d06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:16:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:01 GMT
USER adminer
# Wed, 03 May 2023 17:17:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 17:17:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822087af0bdecd28923ab32fa9fc2e00566083e121bcaf67c0a2e6598c52d149`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5107c70315eac1012c7e38609673cccd890714b8fcf925196c063dcac78e70`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a12d03495dfb72be5d6277086be719ff559fa5ef937eef42793040eab4138a`  
		Last Modified: Wed, 03 May 2023 17:17:29 GMT  
		Size: 1.4 MB (1385335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca70bf37e696c8b2a1c3fad1f023f0c22794bcd2204a7ea0a5fa5de57829ff`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:3afb22ffb88d7612ed522f5f71033289471231e486f2739dc2af1de73d369e51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96980313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329cf5198a48a26609da2510580bac1d30b5de950ab4e17ced60caa13b2e526`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:21 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 05:09:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e92def6d1a89ad8be4edd1fe6307df529888e0918f9a3140d3cf1b564ddadd`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66948adf173d2026ceca9bbe5f0fc41445c77f6a235aacfe41969757971d9311`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754922f697aa1043924559c6fd3ba2e8a00783527cdec3d1af94206ccb13583`  
		Last Modified: Wed, 12 Apr 2023 05:09:52 GMT  
		Size: 1.4 MB (1385257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26a1d2ae2cc6358b97468b25ab918d87440698fac4d21e31dd28c92fa1ad7`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:a2481b949767cc9590da2052f75848628236dfa191907db80e507c0be8bb8e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ae62b8893e269cc48d8ade6f0338175abd327f2d9084130449ad757261007`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:41:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:41:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:41:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:41:44 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:41:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:41:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:42:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:42:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:42:52 GMT
USER adminer
# Wed, 12 Apr 2023 10:42:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 10:42:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7821bb95c14057d16890732aa8b3209cb604db2861e9363fb1f87ff7acae7a`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c203307aba5cfeda96f4e1c642688bf6ecdc19ffb20410957b67e44b440bd12`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c4cc17a0efce3fe1f0ab6cf44e5e46ee93b5a69d688cd6e6a13789c263cee`  
		Last Modified: Wed, 12 Apr 2023 10:45:04 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb383fb5d40f95724fe352abe8005c904ebb884b1afb7c1d84115a3fdaa51c1`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:a55a2c1ff24d027a36e46d24a34dcbb8e854ae5392eec85f9620ba60c7b58694
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101256116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735ee16dfbcee3a436e08438e55c6dd5114b673eec23b536b6b3a2f043a76ad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:20:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:20:40 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:21:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:21:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:21:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:21:34 GMT
USER adminer
# Wed, 12 Apr 2023 01:21:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 01:21:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79148517f43f66f402dd39c8ce8a6104a51fe03f3ed892be0eb40a2bf3ac513e`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc627fe6d1eed682ead8566e47d1e2328da8a1df7864e5a52ac7d20d815572`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7bbdc982c8e7f315e96ecd620a4c3a9d486beb72d36f89daddaaca429d14`  
		Last Modified: Wed, 12 Apr 2023 01:22:41 GMT  
		Size: 1.4 MB (1385746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1791e7b6ab1e976b9698dd6aed465ae1b9badc2ae1c6b6cb91197748b149d`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:5472a0984af7a0bcb4f370188898007842266789e4d9cd931aea7e05ffa0c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93694065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ca8c09f92e5cedf5daa80fc0e9a2a1b8b7e032b3719641feadef4e6294cf5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:22:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:22:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:22:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:22:58 GMT
USER adminer
# Wed, 12 Apr 2023 00:22:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 00:22:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23597fac1b0ce84055df85a56ef40909911286a24879b39f37200567f8e6e63`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88da54b627b523974ad186c33e429711d0e4968550bc7b513fae7d58b9f3de1`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c6c7cf39dd303de3dcb8c7c363f95bfcf24b7dfbd409557940ced6e28cd6e`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.4 MB (1385468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640f1f42167e00265be1505a797a83c7cf74946f47391b62064c6fd44e4fee4d`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:637bfc58e3812a5a5b02a4751346ee6014546c4cd668e0536f10819d9a5f070a
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
$ docker pull adminer@sha256:6d5d4a863c0f2e05e4a7a4dd5971a49afbe247bea72a6f7a2bf43586907cf541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95928958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db158f89ac5a0f88c7f20de5c8a1964aea8b3bbe6c772b62773b6733b1115a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:45:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:46:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:46:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:46:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:46:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:46:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:46:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:46:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:46:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:46:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:46:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879178bf91e580da30477ac110d4992cd630576a5aca16339ed04a7dc93b1ee6`  
		Last Modified: Wed, 12 Apr 2023 07:46:50 GMT  
		Size: 39.5 MB (39486622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdf216e01a41f31e698186674057cbbe34e389726c5ae267c0cfcd3031d927`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb61091e569f770e9e3eeb7cba2097292a05032573e0eeee0b4f9718d93e7a4`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980a061c8abdef923339d3e40dc8918eefc42f128490760e6f166a29d229ee9`  
		Last Modified: Wed, 12 Apr 2023 07:46:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5edff6748342b30b6494d181a231a8545de04b07f2897afa8df63d0b7c7b42`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 1.4 MB (1385369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4912d736721c397fde9b5cf74e064c968992ea39e919a1ed56e4b3660f52cfe`  
		Last Modified: Wed, 12 Apr 2023 07:46:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:899a343626fc8810d226a61458c3f6a1a36e7153fc4fbffe2ea3b135977deddc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c320bf705fd42d0c6893ab05d9973f52e44426b520ef97e9a2e18dfc82dd97d4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 May 2023 22:48:45 GMT
ADD file:e5816cf9c67a55e94065100a95ed3b269817a643b21e5b9c060bfde394a56889 in / 
# Tue, 02 May 2023 22:48:46 GMT
CMD ["bash"]
# Wed, 03 May 2023 10:01:53 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 10:02:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 10:02:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 10:02:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 10:02:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 10:02:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 10:02:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 10:02:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 10:02:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 10:02:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 10:02:34 GMT
USER adminer
# Wed, 03 May 2023 10:02:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 10:02:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:a091ba323f94f60ffce46d1dad6471927a6d7136843d7bbc29ede769d6cafd86`  
		Last Modified: Tue, 02 May 2023 22:51:00 GMT  
		Size: 52.5 MB (52546533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c05b4d7d8785197fea71b7accffe99897dacf8ca50285c7fc4dac6ba20681`  
		Last Modified: Wed, 03 May 2023 10:03:12 GMT  
		Size: 37.2 MB (37247106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09f350fae8d5ff08d5c94186b5557bdf634a5baf3091ee6f2272e11b164fc`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28efee19a53301da773979aa1ba4e7647846067c0116d6d2aa19a68a749ede6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914e558bc32eeb3cc306e62fc22b35b4ff39ff8061e8ec4e2ca563462a2dcfe`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb403fa885ad9ffe9d7aa45c3e3ef20c78f9d6fa066399fd3404c87e30bf7b3e`  
		Last Modified: Wed, 03 May 2023 10:03:04 GMT  
		Size: 1.4 MB (1385329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9edc465f41bf147e1b537181b104da72da0c30391b3a8d353024659319dbe6`  
		Last Modified: Wed, 03 May 2023 10:03:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:11b430e911b282f7b89fbb93e596bdc12369fc5502d67f0253b2429aee5a95e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87787988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6444ff0fe647446d31bc994a5630051f8c77ad362d7aaa7981e59302fbbcce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:32:34 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 07:32:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:32:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 07:32:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 07:32:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 07:32:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 07:33:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 07:33:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 07:33:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 07:33:12 GMT
USER adminer
# Wed, 12 Apr 2023 07:33:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 07:33:12 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c1764ac32a7b56d38d400dd147278947f9b65548ee539516e7f343eae5dc2`  
		Last Modified: Wed, 12 Apr 2023 07:33:53 GMT  
		Size: 36.2 MB (36181564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49773f4a407d96e4956bb9c998ca7fa0d1035c587f4ecdfa7074d8ea66922ff`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f561379c54146ddd2458f085e6a3d5b2204723c1240c2d2412edd4f5d3a2de`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a423c569fd2659253482ece7f04c260b9444afd58d620996d80135dd0a292`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194cbe1af54b30ec82b63fde8d09b7d85d8e69dbca36214566275e5bb1cc19ab`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 1.4 MB (1385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c0c7c232efc74415f1761279f4279cf28a9370861defc0a690d3b6f6df5e52`  
		Last Modified: Wed, 12 Apr 2023 07:33:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:195c05e88c549ff323f21435965c2e6677fe8cb8c5d8ee7b76a6de45404ccef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94324844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d9739cd4b1dcd81fff9a99d2363ec5d41f2ad74bdd346bd8fac26bbff9d06`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:16:28 GMT
STOPSIGNAL SIGINT
# Wed, 03 May 2023 17:16:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:16:48 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 03 May 2023 17:16:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 17:16:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 03 May 2023 17:16:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 03 May 2023 17:17:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 03 May 2023 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 03 May 2023 17:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 03 May 2023 17:17:01 GMT
USER adminer
# Wed, 03 May 2023 17:17:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 03 May 2023 17:17:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f390884cbdf7437b9adc33383ab11920275f677b21cac4528c0f1de12655fd9`  
		Last Modified: Wed, 03 May 2023 17:17:34 GMT  
		Size: 39.2 MB (39242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a168533f0631d50dbab6d3eb2174b05de1644496fc8c5936489f20c2d691f898`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822087af0bdecd28923ab32fa9fc2e00566083e121bcaf67c0a2e6598c52d149`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5107c70315eac1012c7e38609673cccd890714b8fcf925196c063dcac78e70`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a12d03495dfb72be5d6277086be719ff559fa5ef937eef42793040eab4138a`  
		Last Modified: Wed, 03 May 2023 17:17:29 GMT  
		Size: 1.4 MB (1385335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca70bf37e696c8b2a1c3fad1f023f0c22794bcd2204a7ea0a5fa5de57829ff`  
		Last Modified: Wed, 03 May 2023 17:17:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:3afb22ffb88d7612ed522f5f71033289471231e486f2739dc2af1de73d369e51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96980313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329cf5198a48a26609da2510580bac1d30b5de950ab4e17ced60caa13b2e526`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:08:40 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 05:09:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:09:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 05:09:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 05:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 05:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 05:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 05:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 05:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 05:09:21 GMT
USER adminer
# Wed, 12 Apr 2023 05:09:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 05:09:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c743de6f4ab127ec44b64fa1ff5e440e71230fcf92269e98f04233fb0e95aa6`  
		Last Modified: Wed, 12 Apr 2023 05:10:02 GMT  
		Size: 39.6 MB (39558010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada18ec0e02476784ef2b0cc29a1970192d0129e2a552d6d9be9c9c91427d303`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e92def6d1a89ad8be4edd1fe6307df529888e0918f9a3140d3cf1b564ddadd`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66948adf173d2026ceca9bbe5f0fc41445c77f6a235aacfe41969757971d9311`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3754922f697aa1043924559c6fd3ba2e8a00783527cdec3d1af94206ccb13583`  
		Last Modified: Wed, 12 Apr 2023 05:09:52 GMT  
		Size: 1.4 MB (1385257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26a1d2ae2cc6358b97468b25ab918d87440698fac4d21e31dd28c92fa1ad7`  
		Last Modified: Wed, 12 Apr 2023 05:09:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:a2481b949767cc9590da2052f75848628236dfa191907db80e507c0be8bb8e6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662ae62b8893e269cc48d8ade6f0338175abd327f2d9084130449ad757261007`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 10:41:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:41:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 10:41:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 10:41:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 10:41:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 10:41:44 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 10:41:47 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 10:41:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 10:42:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 10:42:45 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 10:42:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 10:42:52 GMT
USER adminer
# Wed, 12 Apr 2023 10:42:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 10:42:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645807d1d15dda4ca689557c06b6d2acbb26ca7902572706a61756d5d196437f`  
		Last Modified: Wed, 12 Apr 2023 10:45:30 GMT  
		Size: 38.0 MB (37951078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb32ad2249a7402b64ab62f7ad423f67287f260f3891a5d3997ffed250ea2e6`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7821bb95c14057d16890732aa8b3209cb604db2861e9363fb1f87ff7acae7a`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c203307aba5cfeda96f4e1c642688bf6ecdc19ffb20410957b67e44b440bd12`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c4cc17a0efce3fe1f0ab6cf44e5e46ee93b5a69d688cd6e6a13789c263cee`  
		Last Modified: Wed, 12 Apr 2023 10:45:04 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb383fb5d40f95724fe352abe8005c904ebb884b1afb7c1d84115a3fdaa51c1`  
		Last Modified: Wed, 12 Apr 2023 10:45:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:a55a2c1ff24d027a36e46d24a34dcbb8e854ae5392eec85f9620ba60c7b58694
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101256116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735ee16dfbcee3a436e08438e55c6dd5114b673eec23b536b6b3a2f043a76ad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:49 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 01:20:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:20:34 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 01:20:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 01:20:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 01:20:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 01:20:40 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 01:21:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 01:21:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:21:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 01:21:34 GMT
USER adminer
# Wed, 12 Apr 2023 01:21:34 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 01:21:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b3857ba4d1c287f4bd1c09595f9053294a6077e3f60bd68c3fc212cec07ef7`  
		Last Modified: Wed, 12 Apr 2023 01:22:55 GMT  
		Size: 40.9 MB (40939523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa98a0c9bd42966fed41c5eda2aa7dcfe4f8c159749750edece4a361c0dc8f78`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79148517f43f66f402dd39c8ce8a6104a51fe03f3ed892be0eb40a2bf3ac513e`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc627fe6d1eed682ead8566e47d1e2328da8a1df7864e5a52ac7d20d815572`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7bbdc982c8e7f315e96ecd620a4c3a9d486beb72d36f89daddaaca429d14`  
		Last Modified: Wed, 12 Apr 2023 01:22:41 GMT  
		Size: 1.4 MB (1385746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1791e7b6ab1e976b9698dd6aed465ae1b9badc2ae1c6b6cb91197748b149d`  
		Last Modified: Wed, 12 Apr 2023 01:22:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:5472a0984af7a0bcb4f370188898007842266789e4d9cd931aea7e05ffa0c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93694065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ca8c09f92e5cedf5daa80fc0e9a2a1b8b7e032b3719641feadef4e6294cf5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:22:19 GMT
STOPSIGNAL SIGINT
# Wed, 12 Apr 2023 00:22:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:22:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 12 Apr 2023 00:22:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
WORKDIR /var/www/html
# Wed, 12 Apr 2023 00:22:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 12 Apr 2023 00:22:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 12 Apr 2023 00:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 12 Apr 2023 00:22:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:22:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 12 Apr 2023 00:22:58 GMT
USER adminer
# Wed, 12 Apr 2023 00:22:58 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 12 Apr 2023 00:22:58 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d938e9b1334125563c9088a8d038623c2c771370baf0646a8b00dc75c5022a`  
		Last Modified: Wed, 12 Apr 2023 00:23:48 GMT  
		Size: 39.0 MB (39017681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf86a2177eddadeff3c335ab21b72d776f97342c6d260ba5574cb81c3eeda25`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23597fac1b0ce84055df85a56ef40909911286a24879b39f37200567f8e6e63`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88da54b627b523974ad186c33e429711d0e4968550bc7b513fae7d58b9f3de1`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c6c7cf39dd303de3dcb8c7c363f95bfcf24b7dfbd409557940ced6e28cd6e`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 1.4 MB (1385468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640f1f42167e00265be1505a797a83c7cf74946f47391b62064c6fd44e4fee4d`  
		Last Modified: Wed, 12 Apr 2023 00:23:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
