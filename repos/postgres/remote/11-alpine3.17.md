## `postgres:11-alpine3.17`

```console
$ docker pull postgres@sha256:c21725d7afb8c180d9fc3dfd350f2eeca69f38e4a0323d64376c44f4dfa26740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `postgres:11-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:f5827ce2649931eef73af3b1e95d0f55a580c69eb5b4e9748311e6ace09bbcd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90257561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac125138db7cbf60449195ce3113ffc4d5f0b1eb3238a31b7527575e5d57e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:13:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:13:15 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:13:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:43:13 GMT
ENV PG_MAJOR=11
# Wed, 14 Jun 2023 21:43:13 GMT
ENV PG_VERSION=11.20
# Wed, 14 Jun 2023 21:43:13 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Wed, 14 Jun 2023 21:43:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:45:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:45:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:45:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:45:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:45:39 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:45:39 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:45:39 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:45:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:45:39 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:45:39 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:45:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94726e0716821ec3d5f3d5b0b39ad2bce969dc1a6c20628067ab5337b37fffac`  
		Last Modified: Wed, 14 Jun 2023 21:47:14 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9106bcc0c876721d56943de59e549b33acd1aac5767c52af9b599b0741c0b8f`  
		Last Modified: Wed, 14 Jun 2023 21:47:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459dff915416444a6ec58ab66b80ae1e8835fd5b896ddf93ff32ec8e2b893755`  
		Last Modified: Wed, 14 Jun 2023 21:53:20 GMT  
		Size: 86.9 MB (86868283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cc5717aa3ebeebea91884c4ae241bf8b88a64cc2e6b98ac7e81f1513629ba7`  
		Last Modified: Wed, 14 Jun 2023 21:53:09 GMT  
		Size: 8.0 KB (7988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb553797185d792f59b38641feeeb05894e935caf82b1d18cd591d0d3adea7`  
		Last Modified: Wed, 14 Jun 2023 21:53:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef41489d1ef58518d4c4013b468a8d19ebc7f716429d4a44934f4528e63fab14`  
		Last Modified: Wed, 14 Jun 2023 21:53:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026cf3ac6b0312338da87393cc6a2d38379a0a773e7426928ea43b11d6417c5c`  
		Last Modified: Wed, 14 Jun 2023 21:53:10 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:57620d8052b85ccebaa9a9d18d5e2fd5d138a0d42054e7117fa1ccfcb0540701
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88116161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b6f25b09ccdca74e1950ba857e540fbb799fe27580da73d81147afac5817cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:26:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 22:26:22 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 22:26:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 22:58:57 GMT
ENV PG_MAJOR=11
# Tue, 08 Aug 2023 22:58:57 GMT
ENV PG_VERSION=11.20
# Tue, 08 Aug 2023 22:58:58 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Tue, 08 Aug 2023 22:58:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 23:01:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 23:01:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 23:01:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 23:01:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 23:01:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 23:01:43 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 23:01:44 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:01:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:01:44 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 23:01:44 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 23:01:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13901678aba6cc2a9a49b22c188c8048b16a39b6c3cc01361b87bef0f49c22ff`  
		Last Modified: Tue, 08 Aug 2023 23:02:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3c5a1f69a1a69ad92ea615b3b0c683557c5110025b19ca2d9eb4d8a153e346`  
		Last Modified: Tue, 08 Aug 2023 23:02:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1378541612b69d86c83736bb1b3a910aa600b9e86940bd13a523fa4ac0bb47c7`  
		Last Modified: Tue, 08 Aug 2023 23:07:20 GMT  
		Size: 85.0 MB (84989143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0d695dde0cd00aa49ea40ea5698f0332ad1e80dfb9db11fc11239acc4b1d5b`  
		Last Modified: Tue, 08 Aug 2023 23:07:08 GMT  
		Size: 8.0 KB (7991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f53616f9fc4a3cfb2b1ea0c396b2dae93059364ba6d643232d29f8fc3fa73c`  
		Last Modified: Tue, 08 Aug 2023 23:07:08 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ae6f3a026bb76e95580ddc67ec710367a57da8041504081708f138fa6f8f80`  
		Last Modified: Tue, 08 Aug 2023 23:07:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a80af4d262fedd241384b6109e359545b4ae932e3d1b7bfb69386ccd0ef953`  
		Last Modified: Tue, 08 Aug 2023 23:07:08 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:abaf5e91543c7b6e0bbcc76b86facb7744555cdbad4be1337fff3d0249a678ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82922909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1458acf98892e5aaf46348e2d238864c0a9a503cc680de315c783cb89f060eeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:29 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Mon, 07 Aug 2023 19:57:29 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 02:34:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 02:34:35 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 02:34:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 02:58:09 GMT
ENV PG_MAJOR=11
# Tue, 08 Aug 2023 02:58:09 GMT
ENV PG_VERSION=11.20
# Tue, 08 Aug 2023 02:58:09 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Tue, 08 Aug 2023 02:58:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 03:00:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 03:00:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 03:00:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 03:00:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 03:00:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 03:00:08 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 03:00:08 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 03:00:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 03:00:09 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 03:00:09 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 03:00:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e4be36b6da96b6e30bc8310d8b4fcd5b95acb1a4ccc7e1ad9d36dc06def768`  
		Last Modified: Tue, 08 Aug 2023 03:01:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5bafa018599d2138de5631f90e7b1ff7cd2deff996e3f053ef2d9beeceef65`  
		Last Modified: Tue, 08 Aug 2023 03:01:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c37c85a51a9712fe40277143904eb4cbeca20bf8dce3e3981387674c2371dd`  
		Last Modified: Tue, 08 Aug 2023 03:05:48 GMT  
		Size: 80.0 MB (80038918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b57499fe64ae56468a5a4b27eb3676c0d6dc47d4473544460e50e48934a80a`  
		Last Modified: Tue, 08 Aug 2023 03:05:38 GMT  
		Size: 8.0 KB (7986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3d217567aef5e2b114824db3146508d5a4f6a9c7df1b89d96471ad60e53acb`  
		Last Modified: Tue, 08 Aug 2023 03:05:38 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cdcdd827bd81e06aa3aad03a4a6c80c0cbda9fa158741baf8636eb733b2232`  
		Last Modified: Tue, 08 Aug 2023 03:05:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a522f7eaa8e118d86ec6fa616be7aa2d02d896a4c44adaab56672bf7b76941d`  
		Last Modified: Tue, 08 Aug 2023 03:05:38 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b0c8c18d7113c402c4b821aadb4d8f53c21b6d65cc4354549b7d16330f204ed4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88080542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec439eda9593252c7ec4313105e853d57aa8904c5c33a5419a30e65723402b30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:04:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:04:39 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:04:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:28:19 GMT
ENV PG_MAJOR=11
# Wed, 14 Jun 2023 21:28:19 GMT
ENV PG_VERSION=11.20
# Wed, 14 Jun 2023 21:28:19 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Wed, 14 Jun 2023 21:28:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:30:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:30:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:30:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:30:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:30:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:30:09 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:30:09 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:30:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:30:10 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:30:10 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:30:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8ff0e86baa37d1a94f26876e404eca60e0bff3f235c3dd9b8f04bff2b563da`  
		Last Modified: Wed, 14 Jun 2023 21:31:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128b35b7bff69ad7412c8b5ceabf4017d71a155e1d6dee928ffcf25678fba177`  
		Last Modified: Wed, 14 Jun 2023 21:31:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a470fe9ca592d5e062ee824d56c69a71fd280fc6a1f9fdaa32613f3b6fcdd276`  
		Last Modified: Wed, 14 Jun 2023 21:36:56 GMT  
		Size: 84.8 MB (84804832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264c43e8e8637f6f19be233a2c4ca120f7a6149f14ddfbb4fc7a5fb267539501`  
		Last Modified: Wed, 14 Jun 2023 21:36:48 GMT  
		Size: 8.0 KB (7991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d86ad8cbdcc044cf38a8c8299aa3e2a4699323abf66febbba62ed7a237d18c7`  
		Last Modified: Wed, 14 Jun 2023 21:36:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0994fe25272ad7fd27fd05ff1c44aa960e57ae6350a7ed897b453193a21359`  
		Last Modified: Wed, 14 Jun 2023 21:36:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6200e638c08939a96896d049120787e37ead95a1badcfbc715682110b988e08`  
		Last Modified: Wed, 14 Jun 2023 21:36:48 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:2d151de4d675636a66add5b95629633900f753f134cf65187dea8ce436ce66bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94899797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c600b8aef339e058c7cd9065d69bc52236f15e9a4e01e9cabc507f403159425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 20:44:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 20:44:22 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 20:44:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 21:34:45 GMT
ENV PG_MAJOR=11
# Tue, 08 Aug 2023 21:34:45 GMT
ENV PG_VERSION=11.20
# Tue, 08 Aug 2023 21:34:45 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Tue, 08 Aug 2023 21:34:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 21:39:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 21:39:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 21:39:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 21:39:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 21:39:04 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 21:39:04 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 21:39:04 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:39:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:39:04 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 21:39:04 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 21:39:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f18735277fba41a769569b43d4ef767a803e905d34e355012eb3eae6625a70`  
		Last Modified: Tue, 08 Aug 2023 21:40:15 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36be60f4dcdcee08649009c2417cfb66bfe07fde5f84a8ed7b7cd53eb9fd4b19`  
		Last Modified: Tue, 08 Aug 2023 21:40:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab907436042f756690a62c44584e3c1d66103a536d803b4ec86accf78d5ee4b`  
		Last Modified: Tue, 08 Aug 2023 21:45:22 GMT  
		Size: 91.5 MB (91471442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b02d86bd3390c6b57854a090b37040e9dabcd2bbf4e2d83e758a13cb5cd896`  
		Last Modified: Tue, 08 Aug 2023 21:45:05 GMT  
		Size: 8.0 KB (7994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6aad49c080912bc4e60f084d0615fadb8d7a94b5db503fcbf018b04b7ead4`  
		Last Modified: Tue, 08 Aug 2023 21:45:05 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5796dd193866e1416564a58900d89c1f033019ec8205a3af4a119dced90bf7c0`  
		Last Modified: Tue, 08 Aug 2023 21:45:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000c7af784e14cd9ebdfa69c17a359a0104cff98a1c3aaeb6e5f430dde0b5b50`  
		Last Modified: Tue, 08 Aug 2023 21:45:05 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:2c90dbb314d386f1c217de308004a7f7cb84a00236e92ce666e2d245b19ef369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95881659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09279309a93f3ec4e4209d00938aac76b566b29bd01de04dc8cc7833db67897`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:35 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Mon, 07 Aug 2023 20:16:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:11:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 22:11:14 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 22:11:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 22:51:28 GMT
ENV PG_MAJOR=11
# Tue, 08 Aug 2023 22:51:29 GMT
ENV PG_VERSION=11.20
# Tue, 08 Aug 2023 22:51:29 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Tue, 08 Aug 2023 22:51:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:54:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:54:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:54:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:54:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:54:52 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:54:52 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:54:52 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:54:53 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:54:54 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:54:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ee805c1332940deaa5547186e69fea1bfb3366abe4ba8ec0b1d18e3ca64d2e`  
		Last Modified: Tue, 08 Aug 2023 22:56:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666703c8b28accd4d26a4d7958273a5b2130cfe7f28d0a929665d042709193f`  
		Last Modified: Tue, 08 Aug 2023 22:56:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d34d048a738bd477ef249aaaee08ad48e8dc82a6a30f1ce1cd9f3a997bce4c3`  
		Last Modified: Tue, 08 Aug 2023 23:04:05 GMT  
		Size: 92.5 MB (92475731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a74bccce28e0077ee12db10fb3202be5c1a33c933bb8bb2db92f7991ca9349`  
		Last Modified: Tue, 08 Aug 2023 23:03:44 GMT  
		Size: 8.0 KB (7995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de46191f01ec6e42bfde94fa45c5324e99a3594a7a7eb7b5980cd69eb890479`  
		Last Modified: Tue, 08 Aug 2023 23:03:44 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e1d21b4a57016a7f7ed189478839e18909bf473344f9164cfa2afcf6830a3b`  
		Last Modified: Tue, 08 Aug 2023 23:03:44 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e05213d4e43fea260ecc7545838837c153c0823670c7a44a2bd9ef37a6a3d58`  
		Last Modified: Tue, 08 Aug 2023 23:03:44 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:17f001d802cf4dbff8fbd045c4d708d15fea94807b1c5d934cffc8022ac00f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90697383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaff78d36c737e54f29d2cbfb295e35f4e2fc1609d2841137f032b50377f94f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 15 Jun 2023 05:19:50 GMT
ADD file:8ad8a62cf274ba5a6568f68473359114136cb5c7704bfdfce6c38efef3081782 in / 
# Thu, 15 Jun 2023 05:19:51 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 12:43:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Jun 2023 12:43:43 GMT
ENV LANG=en_US.utf8
# Thu, 15 Jun 2023 12:43:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Jun 2023 13:41:41 GMT
ENV PG_MAJOR=11
# Thu, 15 Jun 2023 13:41:41 GMT
ENV PG_VERSION=11.20
# Thu, 15 Jun 2023 13:41:41 GMT
ENV PG_SHA256=3d7c8882f64a7e98534a044257dfee7abad77a5b7da12508d85d722b98b5acce
# Thu, 15 Jun 2023 13:41:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 15 Jun 2023 13:44:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Jun 2023 13:44:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Jun 2023 13:44:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 15 Jun 2023 13:44:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Jun 2023 13:44:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 15 Jun 2023 13:44:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Jun 2023 13:44:26 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 15 Jun 2023 13:44:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 13:44:27 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jun 2023 13:44:27 GMT
EXPOSE 5432
# Thu, 15 Jun 2023 13:44:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb857838eb854a669f87c5df4d936d905fb3129287a93ef485da9454c11d83cd`  
		Last Modified: Thu, 15 Jun 2023 05:30:48 GMT  
		Size: 3.2 MB (3174898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb85b75673264d757e1c2ad65668ad9e2037509bace619da019d954b96dfc8c3`  
		Last Modified: Thu, 15 Jun 2023 14:16:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c648b0050250f1bc449bc28437c275fb62b95fb7010611df14c5b14c99d4ee`  
		Last Modified: Thu, 15 Jun 2023 14:16:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b997ec6b2b72bcf04af1b24c3e8dc1b6a8c892cac98129acc616a9786e7cf9e3`  
		Last Modified: Thu, 15 Jun 2023 14:45:02 GMT  
		Size: 87.5 MB (87507914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e6273277fd4c669b767beef72dcb0b4ac0a6d6024fa25745eb5ffcb8df7a75`  
		Last Modified: Thu, 15 Jun 2023 14:44:51 GMT  
		Size: 8.0 KB (7987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d21aa14fc7f5c3281c6d40e3be2685d05838bb24c0d11751399c12b7c789d9`  
		Last Modified: Thu, 15 Jun 2023 14:44:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa0d8e0df7611c45e19213cb2bcd75b3d9da4ca89fccba9325cea4a1d14ada3`  
		Last Modified: Thu, 15 Jun 2023 14:44:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d950942e07b5aa55713c928d909fe91a3485e8632b5e53725bbc420e58d8c4`  
		Last Modified: Thu, 15 Jun 2023 14:44:51 GMT  
		Size: 4.8 KB (4793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
