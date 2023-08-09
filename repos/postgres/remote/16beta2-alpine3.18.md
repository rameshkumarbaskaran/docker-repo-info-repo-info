## `postgres:16beta2-alpine3.18`

```console
$ docker pull postgres@sha256:138a109dc482728e86bf2bae6fdd3574f9156b7db7f609facda7d7e7c8ecc7f0
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

### `postgres:16beta2-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:893b092656cd3cccedfaddcbd824092cc4f6d0797027ccf6f48151fa16013f6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94233074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338ccfade89d2f4e9c8989038d977d7bd6408e625a46ed6184b947236c038703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:10:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:10:06 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:10:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:10:07 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 02:08:09 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 02:08:09 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 02:08:10 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 02:10:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 02:10:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:10:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 02:10:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:11:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 02:11:00 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:11:00 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:11:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:11:00 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:11:00 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:11:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c8ef16402f7d0f3d3c7c581b33d4ab851efed851826633154d90c08d5e1f89`  
		Last Modified: Wed, 14 Jun 2023 21:46:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb57831f5201e337de1dd5b1fb077701af0afe39fd7fa8143f9e552eb6ae20`  
		Last Modified: Wed, 14 Jun 2023 21:46:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94945c3bd343db82506da799b7935fe946fecf51c45eb5b18de73084218b804b`  
		Last Modified: Tue, 04 Jul 2023 02:19:53 GMT  
		Size: 90.8 MB (90819042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733e7b63772393fda0828044343b461bbc3c310f8a3b80279f0fdc28ddbe2bac`  
		Last Modified: Tue, 04 Jul 2023 02:19:42 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651f9aee7f5973b0a6837ad302981d3855d29c1884902838e899548214de5efc`  
		Last Modified: Tue, 04 Jul 2023 02:19:42 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3249f6a8ba916642b7cec53969dc4a9779cd954ef6842e6f45134cbf0028689`  
		Last Modified: Tue, 04 Jul 2023 02:19:42 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9963fa78ec7e7064b3cfa891c9276b5ec0c9277b3f50ef3baf9bf2451f576fa2`  
		Last Modified: Tue, 04 Jul 2023 02:19:42 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a2e433dacfeef0469c56dee9f0adc3f2797c7cd405f1ff411718f198d8b63af4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92875085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56607450ec165f0baf3471e5e773a2872102bc90fdb2021a6d0da6e5061cbc57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:22:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 22:22:43 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 22:22:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 22:22:44 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 22:22:44 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 22:22:44 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 22:22:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:26:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:26:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:26:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:26:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:26:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:26:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:26:17 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:26:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:26:17 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:26:18 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:26:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b73a3c9920448aa9f1c953bcee2cf61da8e037ec17962798e2b2578a774d2f`  
		Last Modified: Tue, 08 Aug 2023 23:02:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dd824c881352b4f681664d1a1038cb7cacc538bcd635a4f61fb6ed0388db1e`  
		Last Modified: Tue, 08 Aug 2023 23:02:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089f59e2f1f6a7ec33c434b7f24f05202e1f17b026a750277d8e80ffd0571c94`  
		Last Modified: Tue, 08 Aug 2023 23:02:34 GMT  
		Size: 89.7 MB (89714128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5312b16fa6210ac7416b630e713c023a2de2626dba967deb5eb7c37d244ed3e5`  
		Last Modified: Tue, 08 Aug 2023 23:02:18 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26e8081556d25fecc467efcf74c16279c1beb5840c669e45f1edf88b578a459`  
		Last Modified: Tue, 08 Aug 2023 23:02:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b59bea28bcc80eceffbaf5e1deb921f9d801c5d026b8b3c7371bfba17fee25`  
		Last Modified: Tue, 08 Aug 2023 23:02:18 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64207b30c049cdad75efdb002af0fabb226c2aa941c0c9be0ca5c359e5de22b2`  
		Last Modified: Tue, 08 Aug 2023 23:02:18 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:dd63e154710187f3c8bd39c977faeacfd1892ba81a32b8084159bd7d75b80001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87520570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1f213583741146f3253cb9154e5d124226441eea0e7c3f09b994e72409eb70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 02:31:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 02:31:57 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 02:31:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 02:31:58 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 02:31:58 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 02:31:58 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 02:31:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 02:34:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 02:34:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 02:34:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 02:34:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 02:34:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 02:34:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 02:34:24 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 02:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 02:34:24 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 02:34:25 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 02:34:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5c2c99c4018a6602af0b3f90590873658820fedbb99ccefdcc9843a41607a`  
		Last Modified: Tue, 08 Aug 2023 03:01:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bb3f13868e7bfeadf5ab1f5864ff0fc2b75674a04e07e30b6c68bf462762aa`  
		Last Modified: Tue, 08 Aug 2023 03:01:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43cc8c2d9018f3c148b8ff6eab9ad040a4c0478eec99d77ebaab844b4e3f10`  
		Last Modified: Tue, 08 Aug 2023 03:01:24 GMT  
		Size: 84.6 MB (84604932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d87b19255a2a986aa22140b2a5c7cade859c370abff867cdd9661a4794e96dd`  
		Last Modified: Tue, 08 Aug 2023 03:01:13 GMT  
		Size: 9.6 KB (9570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9e2aa9a4c724bb016e96cfdee96ad8244f9473ec677f227ce7e85a210649d`  
		Last Modified: Tue, 08 Aug 2023 03:01:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dc0f4dcaabbe18d84a29feb5668279b1df73560ebdaf0689c8739bddcdaff`  
		Last Modified: Tue, 08 Aug 2023 03:01:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1f1f14f2476a6e01b69cf1a4023f66800026706c9178aca3e381ca94d6a59d`  
		Last Modified: Tue, 08 Aug 2023 03:01:13 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7976059b7582170a997a7dee17b185ea0b601a0ecfeae031a747b732c87803e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93179623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d2d397001d72185b674184ca023da7f9426b19a1e7af5bc2b6826a7bf21e2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:02:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:02:16 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:02:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:02:16 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 00:44:06 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 00:44:06 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 00:44:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 00:46:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 00:46:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 00:46:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 00:46:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 00:46:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 00:46:26 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 00:46:26 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 00:46:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 00:46:26 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 00:46:26 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 00:46:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d285f268e220aa1ae37b8ad4f59c7c59f60c721d1f433c9c58e4f9e52e814f61`  
		Last Modified: Wed, 14 Jun 2023 21:31:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4388b4d68d1c49bc6e6b54f3d73762850870a8281138568a35e656553686e84`  
		Last Modified: Wed, 14 Jun 2023 21:31:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914092affb1ae784f9785d4345b5e6bb26f2e3d6f6a8126b3d302b57af94ff54`  
		Last Modified: Tue, 04 Jul 2023 00:50:59 GMT  
		Size: 89.8 MB (89834217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed1d7dadd494d1ef9c985c72d13bbd03a6a07cd635820837564515e64ffc50a`  
		Last Modified: Tue, 04 Jul 2023 00:50:51 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50dd0cbe4da7e78e1b8086a6bba2462129e43a87f4b699b88f0e6189695bd32`  
		Last Modified: Tue, 04 Jul 2023 00:50:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e352e041c1281cff21485d25417dc4afc9b0c2cda122dcf8d4a2bf3705966`  
		Last Modified: Tue, 04 Jul 2023 00:50:51 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1a790a327b2388965f47f22436fa69d2c52e0486553a37ed3cd5983787860f`  
		Last Modified: Tue, 04 Jul 2023 00:50:51 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:2b250581142c05feb6056e88cf008548ba862391ad5f964e68ebcd2be54b2ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99200879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0477f8a39304c3a84efadfcd988a3a97dbdd0127e52d1d965c2b55fbbff1ff35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 20:38:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 20:38:44 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 20:38:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 20:38:45 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 20:38:45 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 20:38:45 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 20:38:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 20:44:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 20:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 20:44:18 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 20:44:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 20:44:19 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 20:44:19 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 20:44:19 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 20:44:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 20:44:19 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 20:44:19 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 20:44:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffc9b02160bb312a7ec87e959a3a9f5cc15bd3ee2c9686dc4b0723e53b4df62`  
		Last Modified: Tue, 08 Aug 2023 21:39:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c784e4e00ce4d87e5b67f8577ead880344f425d991d943e54f61738ab5535b`  
		Last Modified: Tue, 08 Aug 2023 21:39:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52bce706be701f353740720c3756869f06e976aa3d5869e57fba76fd6c48fb5`  
		Last Modified: Tue, 08 Aug 2023 21:40:04 GMT  
		Size: 95.9 MB (95949585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4011454210b2a64410075aebe58fa36ce4724456770899ee1dfd6a8dbafb55`  
		Last Modified: Tue, 08 Aug 2023 21:39:47 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac01dee775e2d23617353a9ba48c26a3938f66f8ccab7fe1bbee76f0280696a`  
		Last Modified: Tue, 08 Aug 2023 21:39:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691e4b3ea5d07fe20219001c1c6be2d872d4c525ad3e6d336cb60729ad515ef`  
		Last Modified: Tue, 08 Aug 2023 21:39:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594ce83b42f356a9d0839199e37e56927abda2968f3ff3b27122e836cd855496`  
		Last Modified: Tue, 08 Aug 2023 21:39:47 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:12bb7f1c56504fcd64eb5d01f5dc8bc36067d1f482390e196628a83ba3d40f72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99956451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54ce3e60b7e90b7be4306b526ad4a9afd1e6465c74b3038fc730c4337389827`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:06:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 08 Aug 2023 22:06:52 GMT
ENV LANG=en_US.utf8
# Tue, 08 Aug 2023 22:06:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 08 Aug 2023 22:06:54 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 22:06:55 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 22:06:56 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 22:06:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:10:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:10:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:10:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:10:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:10:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:10:56 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:10:56 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:10:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:10:57 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:10:57 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:10:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d85e956d8abee510b053a42fd1ed47c684f6838ffba3cccca8a7eb65f59bcc`  
		Last Modified: Tue, 08 Aug 2023 22:56:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22205f49560580d8e9777856387c309094391a1a0346669b180abc602b5016dc`  
		Last Modified: Tue, 08 Aug 2023 22:56:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f251efc3c738d12751c2dfa102dac063670e050373084c173563b33b885cdf60`  
		Last Modified: Tue, 08 Aug 2023 22:56:41 GMT  
		Size: 96.6 MB (96594045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb1ebb76b75b3563fa9202ea1edd9072202f76a3ccf8ea68ffd1b2f61bb59bc`  
		Last Modified: Tue, 08 Aug 2023 22:56:20 GMT  
		Size: 9.6 KB (9570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b69fcf6d9d2b29334aeaf888035318f9f9dd0f4b9f389c48c2c999457b755b`  
		Last Modified: Tue, 08 Aug 2023 22:56:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ad54346acb4c87eb42ea1b8001839d4d87d2195970fa8719b0fb4c1ce1783`  
		Last Modified: Tue, 08 Aug 2023 22:56:20 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a91fc3806fe8b749d22a7a7a1777a018954b930899dd3e88f8f122e72350ca`  
		Last Modified: Tue, 08 Aug 2023 22:56:20 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:edb98afa09e286457010562e400cd2143c03e1c5685022e35914d31edd2148c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95896440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20dba48acf292a22e5c30860dcd4df4691d85a2f2fd32866075f7478078eeb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 12:38:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Jun 2023 12:38:50 GMT
ENV LANG=en_US.utf8
# Thu, 15 Jun 2023 12:38:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Jun 2023 12:38:51 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 02:00:03 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 02:00:03 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 02:00:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 02:02:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 02:02:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:02:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 02:02:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:02:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 02:02:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:02:54 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:02:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:02:54 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:02:54 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:02:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b902697f47ace1a7710262b6d5d8b157d1111e483c46aa83c9d2b90fb5b76c`  
		Last Modified: Thu, 15 Jun 2023 14:15:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aac0290be5a2aa79e42f5c357733559922c12517f41247dcf4dd56ec5f4f9ea`  
		Last Modified: Thu, 15 Jun 2023 14:15:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5001241899caf1e24e072f25cf3103ae349370277790e79ebdd10683855a45`  
		Last Modified: Tue, 04 Jul 2023 02:16:19 GMT  
		Size: 92.7 MB (92666785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda27bc5fb4fcb0dd2b6864a2e724c7ee5f5ef87dc59f23cf790e0667bcf869b`  
		Last Modified: Tue, 04 Jul 2023 02:16:08 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5e3905e80d32b732d34cdab65c934b544bd7c8757766c095f464727093d936`  
		Last Modified: Tue, 04 Jul 2023 02:16:08 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9db795a9982f0a7fff53bda1056bfe1c6030765af6abf53b132663abc5f4852`  
		Last Modified: Tue, 04 Jul 2023 02:16:08 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48349a0793383400bef191e0cd4fc7a4946a6311d46e37dbd52ea69e8cb5ce7b`  
		Last Modified: Tue, 04 Jul 2023 02:16:08 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
