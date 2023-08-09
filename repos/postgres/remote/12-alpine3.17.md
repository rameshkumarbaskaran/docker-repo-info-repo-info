## `postgres:12-alpine3.17`

```console
$ docker pull postgres@sha256:e7e2d72fdc40e64cac9c845cfa103aee97be0460f7f30cbf01eb6020a7741df2
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

### `postgres:12-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:988c289a6dfaf8e6e2f0eda6bcf318276c1a4ef05e61747d902becf2abf8cb9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91372842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2aa3f2ad7005ebe84e24c5e639eaae95c00e03e84abc65b0ab682d543db3a8`
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
# Wed, 14 Jun 2023 21:37:29 GMT
ENV PG_MAJOR=12
# Wed, 14 Jun 2023 21:37:29 GMT
ENV PG_VERSION=12.15
# Wed, 14 Jun 2023 21:37:29 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Wed, 14 Jun 2023 21:37:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:39:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:39:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:39:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:39:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:39:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:39:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:39:58 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:39:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:39:58 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:39:58 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:39:58 GMT
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
	-	`sha256:41165c6c6cf4b0c95a0dca1f37f772533cb40b63c3cd5c1a4190762c058f314e`  
		Last Modified: Wed, 14 Jun 2023 21:52:15 GMT  
		Size: 88.0 MB (87982858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc560467f137386ba1dad5ca22623f0ea68bdfe263372421148fda217b8727c3`  
		Last Modified: Wed, 14 Jun 2023 21:52:01 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b477c2a21f8c9cefaa8b7c6ff42b94f203bdd13ae02817b042e386b5350276`  
		Last Modified: Wed, 14 Jun 2023 21:52:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e5da728c2564c00a55c3d772d4a96cf80d78012677e81af835be7452ce332`  
		Last Modified: Wed, 14 Jun 2023 21:52:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d6b83902f74ddbbd1188f7238cc15008842e123c2aaeff708eaf324e1bd581`  
		Last Modified: Wed, 14 Jun 2023 21:52:01 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a9ba2489a689cf1ce01ad0af563563e9332e39e8f292ddf4a8f7fd7a48d21e00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89250355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc3e6e23aa8c4a48e8a66113d97f16580c4ea1e87992ee3e0922924b0d9247`
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
# Tue, 08 Aug 2023 22:53:11 GMT
ENV PG_MAJOR=12
# Tue, 08 Aug 2023 22:53:11 GMT
ENV PG_VERSION=12.15
# Tue, 08 Aug 2023 22:53:11 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Tue, 08 Aug 2023 22:53:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:55:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:55:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:55:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:55:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:55:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:55:59 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:55:59 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:55:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:55:59 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:55:59 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:56:00 GMT
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
	-	`sha256:1e1d211e8383a3181969882b8df5869a81d50dd637329963e7d5507cd3d3c307`  
		Last Modified: Tue, 08 Aug 2023 23:06:31 GMT  
		Size: 86.1 MB (86122637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5dde2b3e3aa1752dca486939fb235e344828e10394c12461a1347ff9c3811c`  
		Last Modified: Tue, 08 Aug 2023 23:06:16 GMT  
		Size: 8.7 KB (8691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfdb98b416b594a8cdfbcf7d2b3db80ec6003f87678ba9ca50a082915ff1d47`  
		Last Modified: Tue, 08 Aug 2023 23:06:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4dd5cd2704f3dbe720acd1390dce8a000835a373d52b2c382979f53f23c03`  
		Last Modified: Tue, 08 Aug 2023 23:06:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca72f63fd86045b597d9be9cb5c6130d181fed9773215e626bbe2c4de657ced`  
		Last Modified: Tue, 08 Aug 2023 23:06:16 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:17c372fb3ed01eab6f510fd519013f3ea63c25bace50b7f91e76cab64185dc19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83992559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097edd0e6baab8681e8f39ee98471411a006ff4b4652f49912d0756dc7c0618f`
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
# Tue, 08 Aug 2023 02:53:50 GMT
ENV PG_MAJOR=12
# Tue, 08 Aug 2023 02:53:50 GMT
ENV PG_VERSION=12.15
# Tue, 08 Aug 2023 02:53:50 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Tue, 08 Aug 2023 02:53:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 02:55:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 02:55:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 02:55:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 02:55:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 02:55:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 02:55:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 02:55:54 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 02:55:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 02:55:54 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 02:55:55 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 02:55:55 GMT
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
	-	`sha256:6f6bbbf32820c8c2977444b5b54c0a630d3ceda6e1e508b26c61b4219d7c3068`  
		Last Modified: Tue, 08 Aug 2023 03:05:02 GMT  
		Size: 81.1 MB (81107864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9503c9322be20d7db5df9c05e976767f0757d57c59ca1b5814fedcecc7c07f08`  
		Last Modified: Tue, 08 Aug 2023 03:04:52 GMT  
		Size: 8.7 KB (8692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fde75bd1e826b609ac7f2f03c0197ecca27fb223ada0d38004edd98b05e0412`  
		Last Modified: Tue, 08 Aug 2023 03:04:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0b4044f5dcc96ab9d40cc3c0e578a1e7f0ada5a6c433d1ae597a6087de4d29`  
		Last Modified: Tue, 08 Aug 2023 03:04:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22ecd54a301b220d1a12cfc3e4aef5e88b9af890d7f56e1a0400090625a6744`  
		Last Modified: Tue, 08 Aug 2023 03:04:52 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6546c14fad2b75294205c18ab266083494cb672fe4df8822a844913c96718530
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89179142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2607f95da29361ef1a6b6c25f88657b9f30e3d838822331e645dee8cb9ea2aba`
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
# Wed, 14 Jun 2023 21:23:38 GMT
ENV PG_MAJOR=12
# Wed, 14 Jun 2023 21:23:39 GMT
ENV PG_VERSION=12.15
# Wed, 14 Jun 2023 21:23:39 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Wed, 14 Jun 2023 21:23:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:25:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:25:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:25:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:25:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:25:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:25:31 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:25:31 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:25:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:25:31 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:25:31 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:25:31 GMT
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
	-	`sha256:dd12ee38d5dd46d732ef75d1ade7eb661b6e4dc5d270f0bb0bfc084951edc669`  
		Last Modified: Wed, 14 Jun 2023 21:35:58 GMT  
		Size: 85.9 MB (85902738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635bb477c5056ed42beca8769fe7e49d29d6230c91fd99342a181ed76fed7b4`  
		Last Modified: Wed, 14 Jun 2023 21:35:49 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affe1250084e3a6993b95924a763d1aab4eb721e88c9b8de468bb1d1f59bcd93`  
		Last Modified: Wed, 14 Jun 2023 21:35:50 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2ba1a1c9c8b4b1f68a3c2176206d968e847ea982428fb26fe2564dc29b852c`  
		Last Modified: Wed, 14 Jun 2023 21:35:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f15d02cf8ed6c99f6edcf67c5c6f355eaae1c23c0daf6c499a2cf8641e54e11`  
		Last Modified: Wed, 14 Jun 2023 21:35:49 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:60b154f18d67a936b77282e1e9220b1b9eb6f77fa9dfc83e1c70e7f9a6bd5744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96126334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9a8b2b62f703a0da51bb52a8f1d94a0d909250d5b75d1f640ad89c64aa7780`
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
# Tue, 08 Aug 2023 21:25:25 GMT
ENV PG_MAJOR=12
# Tue, 08 Aug 2023 21:25:26 GMT
ENV PG_VERSION=12.15
# Tue, 08 Aug 2023 21:25:26 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Tue, 08 Aug 2023 21:25:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 21:29:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 21:29:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 21:29:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 21:29:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 21:29:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 21:29:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 21:29:54 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:29:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:29:54 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 21:29:54 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 21:29:54 GMT
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
	-	`sha256:fe68f0773b35a2770df1d07786a8747b6cacfaa738261d4b11627ea57d56f8a2`  
		Last Modified: Tue, 08 Aug 2023 21:44:26 GMT  
		Size: 92.7 MB (92697285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41e0aa697611e9b561593d549a4e69e6fe9f0500ae8211ac3b4c1bed23c4cc`  
		Last Modified: Tue, 08 Aug 2023 21:44:09 GMT  
		Size: 8.7 KB (8693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81dba18ae127b3e070faa7013adfbe423609c70fe294f49fdf70dcfdc7598fc`  
		Last Modified: Tue, 08 Aug 2023 21:44:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadf9caaf601be478cf56f6c120b78eb2ee1c489393cf2d8fe76f1c900a562d7`  
		Last Modified: Tue, 08 Aug 2023 21:44:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ec44033fdbac7c010d5588916c12dd0e83dc45edb4e650e3b84b778def1afb`  
		Last Modified: Tue, 08 Aug 2023 21:44:09 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:a093864a2aa7b7dcbd61d783f39f1cfc8a1a2fbd171d4b90e78e87763f5329a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97060573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab12e4d26145c8fd99858214bc237342584c210fccd22ce9f9fa6427d8c393c`
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
# Tue, 08 Aug 2023 22:44:05 GMT
ENV PG_MAJOR=12
# Tue, 08 Aug 2023 22:44:05 GMT
ENV PG_VERSION=12.15
# Tue, 08 Aug 2023 22:44:06 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Tue, 08 Aug 2023 22:44:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:47:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:47:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:47:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:47:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:47:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:47:35 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:47:36 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:47:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:47:36 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:47:37 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:47:37 GMT
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
	-	`sha256:54f59ea3ee70ebd494615c65a4f78a146d2df481cb2cf1393a84de1518b348ac`  
		Last Modified: Tue, 08 Aug 2023 23:02:48 GMT  
		Size: 93.7 MB (93653944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da946035f68cd923e4e6cbacaf33efdf13c3e88432d9f3cb6b14349bf14617db`  
		Last Modified: Tue, 08 Aug 2023 23:02:27 GMT  
		Size: 8.7 KB (8695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ff9c6184830b03679327f18777288876011364284a6da1210e15bef376ed4`  
		Last Modified: Tue, 08 Aug 2023 23:02:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef25928595cdb1546b1849cb9dca41608e996994c25edd307fd26cc0122f597`  
		Last Modified: Tue, 08 Aug 2023 23:02:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc266705941c96bd4236e9a619474dbbca51280a31b2847acc9660ff531edd4f`  
		Last Modified: Tue, 08 Aug 2023 23:02:26 GMT  
		Size: 4.8 KB (4793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:006812bdf09aa1bdb53b8a720d778af75de7039e1b921774f175cc2439f8e6df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91839145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b075fd73d31b965339c77ffb716fc1e69d74fd83cd9ce0cad465bab22949568a`
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
# Thu, 15 Jun 2023 13:30:47 GMT
ENV PG_MAJOR=12
# Thu, 15 Jun 2023 13:30:47 GMT
ENV PG_VERSION=12.15
# Thu, 15 Jun 2023 13:30:47 GMT
ENV PG_SHA256=bb5206e2864c1c4579938b96ea6096d155f22abf2d2cc2aa57571e3c4cb12b36
# Thu, 15 Jun 2023 13:30:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 15 Jun 2023 13:33:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Jun 2023 13:33:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Jun 2023 13:33:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 15 Jun 2023 13:33:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Jun 2023 13:33:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 15 Jun 2023 13:33:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Jun 2023 13:33:40 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 15 Jun 2023 13:33:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 13:33:41 GMT
STOPSIGNAL SIGINT
# Thu, 15 Jun 2023 13:33:41 GMT
EXPOSE 5432
# Thu, 15 Jun 2023 13:33:41 GMT
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
	-	`sha256:29b8a8446a984360e3b11a0c23be36f76d47e1e295743de5198ef338e87633e4`  
		Last Modified: Thu, 15 Jun 2023 14:39:38 GMT  
		Size: 88.6 MB (88648975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bc78f62a474e4e9daf123478a861d957bc2fe5c87ac2d1829e99d5590d571d`  
		Last Modified: Thu, 15 Jun 2023 14:39:26 GMT  
		Size: 8.7 KB (8691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467d36d621d0cb0d3b8592b0c193eb6ed341fbb586f5a81eefba1a06dfca34e6`  
		Last Modified: Thu, 15 Jun 2023 14:39:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3093ed43c1bd4d4540e96e63e1b260335f6072042f1ec01551f9cf323c36f6d5`  
		Last Modified: Thu, 15 Jun 2023 14:39:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5514d2dc89b2fe535122d79b14999147e1b14edc968a29af7cb2021d6213fc0e`  
		Last Modified: Thu, 15 Jun 2023 14:39:26 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
