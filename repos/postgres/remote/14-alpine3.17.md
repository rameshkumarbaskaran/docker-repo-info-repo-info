## `postgres:14-alpine3.17`

```console
$ docker pull postgres@sha256:3271fd48ec9ab8b078c419c3958b59e77fcd8665e5eccb8de6785cc474c380f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `postgres:14-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:79084ba391b38e09ac98c97183c6d42fdd43884f542e7582620cfab661161073
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91210707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53023276205526710f70ea25508a619e66bd1455b40180090244667df6145758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:10:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:10:19 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:10:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:14:00 GMT
ENV PG_MAJOR=14
# Wed, 30 Nov 2022 21:14:00 GMT
ENV PG_VERSION=14.6
# Wed, 30 Nov 2022 21:14:00 GMT
ENV PG_SHA256=508840fc1809d39ab72274d5f137dabb9fd7fb4f933da4168aeebb20069edf22
# Wed, 30 Nov 2022 21:17:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 21:17:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 21:17:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 21:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 21:17:10 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 21:17:10 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 21:17:10 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 21:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 21:17:10 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 21:17:10 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 21:17:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd022df475c75e388b1fd7a4163f33c0ff1b1d74fdc20b70d7997fe03aa044af`  
		Last Modified: Wed, 30 Nov 2022 21:27:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed70ce3a42bb46bc919e74b0e65503324722dcbef23cf71e04c33adf27e1835`  
		Last Modified: Wed, 30 Nov 2022 21:27:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2775bdb6ff3f8e97d19079564099c38204b1e0aad8e41e7147c0e5a234e1144`  
		Last Modified: Wed, 30 Nov 2022 21:28:45 GMT  
		Size: 88.1 MB (88087994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4ee63b83fd88407a9e116d9d265bc8cafaaec27210af5a782c3851f071e60`  
		Last Modified: Wed, 30 Nov 2022 21:28:30 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34036aac153747c6c158bc66dd673744f8399053c5c52058284af877ff286889`  
		Last Modified: Wed, 30 Nov 2022 21:28:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b6820ac2e6386b49db7ea584364ea0b323398ee71401f872a03b8ff999a2fc`  
		Last Modified: Wed, 30 Nov 2022 21:28:30 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf8724f8287156fc9fc946ee1c9a4d4cd03bbd21b43407c62901e3ed37fed2`  
		Last Modified: Wed, 30 Nov 2022 21:28:30 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:158e276c37a9835174b2aae15673af158c3b272a5a4fbad686b49986e9a6bd7e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85881618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4718d472a12ca7492cccce4dd3a467369149056b451e8ed236fa2522360f305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:24:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:24:31 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:24:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:28:06 GMT
ENV PG_MAJOR=14
# Wed, 30 Nov 2022 21:28:06 GMT
ENV PG_VERSION=14.6
# Wed, 30 Nov 2022 21:28:06 GMT
ENV PG_SHA256=508840fc1809d39ab72274d5f137dabb9fd7fb4f933da4168aeebb20069edf22
# Wed, 30 Nov 2022 21:30:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 21:30:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 21:30:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 21:30:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 21:30:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 21:30:47 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 21:30:47 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 21:30:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 21:30:47 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 21:30:48 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 21:30:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ff09f15b2005f6cc7b283cb6b00059ad4d0ac79d1fc45f9cc19812e2204443`  
		Last Modified: Wed, 30 Nov 2022 21:43:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1306f705d7bd596b648dce0baffcecc255840db04271a39efba39954d04d82e9`  
		Last Modified: Wed, 30 Nov 2022 21:43:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a4d2bbcd1b75befc624b3ada8b9d0f9b7b5ac1a77152b3aebd00a7ec5d987c`  
		Last Modified: Wed, 30 Nov 2022 21:43:50 GMT  
		Size: 83.0 MB (83000707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46d0472adf16666faa56525e3e386ea11d7d32dab53969b9e8f27a3cf6b2b7f`  
		Last Modified: Wed, 30 Nov 2022 21:43:38 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318c1a8085b3c414e756e4823596b9051bade5b806054aab6d68d70ec1a0ee6d`  
		Last Modified: Wed, 30 Nov 2022 21:43:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d554b6f8f49e692c037681546be6ed4df7b74862bdf6039d4243ea2b9828184`  
		Last Modified: Wed, 30 Nov 2022 21:43:37 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14b1882c2dfbb5e5a58fd30e360b9308636d852a0c7b27154eec3dff92df6e2`  
		Last Modified: Wed, 30 Nov 2022 21:43:37 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6df6d9642c8c9aeee826b6b0cd53cccc7dd3004ca2294e83ded9e9babfefdc26
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91137769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab9649908a6aec7273503dcc9f9da924149b2593f7016d3b105b90c328fbff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:41:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:41:48 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:41:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:43:58 GMT
ENV PG_MAJOR=14
# Wed, 30 Nov 2022 21:43:58 GMT
ENV PG_VERSION=14.6
# Wed, 30 Nov 2022 21:43:58 GMT
ENV PG_SHA256=508840fc1809d39ab72274d5f137dabb9fd7fb4f933da4168aeebb20069edf22
# Wed, 30 Nov 2022 21:45:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 21:45:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 21:45:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 21:45:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 21:45:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 21:45:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 21:45:57 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 21:45:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 21:45:57 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 21:45:57 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 21:45:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc5a1575ff6ac91556b51a6d477d71d5e2651299fd7bfb2c544e512dea7ce11`  
		Last Modified: Wed, 30 Nov 2022 21:52:51 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753903688c57201bee69249a606bbb11e98bf3158068094a6606a05a8b85eaa`  
		Last Modified: Wed, 30 Nov 2022 21:52:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afadd6a70e8ae11458cf77058b7fc73848099860636d5d5ae642823be3bbbf73`  
		Last Modified: Wed, 30 Nov 2022 21:53:26 GMT  
		Size: 87.9 MB (87862887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257391ea2d328974084808b21134beef4cee972a25f4ee95133cfffcde86f605`  
		Last Modified: Wed, 30 Nov 2022 21:53:17 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058995a64a202ea7ff52256be516e4655463b4056524f0cc192b00bfd7440cb`  
		Last Modified: Wed, 30 Nov 2022 21:53:17 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c965d7969de7f175461e52c114a7494cc2062f15b2694863df975070fe5991fb`  
		Last Modified: Wed, 30 Nov 2022 21:53:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6fa46b7563308f82d0df8cbe5e4cb23061ad297afc77e5c32518f793d2ac5`  
		Last Modified: Wed, 30 Nov 2022 21:53:17 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:6dacd62648a312df80ca4edb227dfae7536043fb98d0124254639a011633e73d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98231026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de2eca6ef4135615f66273091885e19a9824864d36036f546610de3d085e3a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:38:24 GMT
ADD file:f2fbc3153694110f7004f005c4e18435b171ed44a3b35498a1b4916ef1e9af43 in / 
# Tue, 22 Nov 2022 22:38:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 20:46:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 20:46:33 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 20:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 20:50:05 GMT
ENV PG_MAJOR=14
# Wed, 30 Nov 2022 20:50:06 GMT
ENV PG_VERSION=14.6
# Wed, 30 Nov 2022 20:50:07 GMT
ENV PG_SHA256=508840fc1809d39ab72274d5f137dabb9fd7fb4f933da4168aeebb20069edf22
# Wed, 30 Nov 2022 20:52:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 20:52:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 20:52:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 20:52:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 20:52:52 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 20:52:53 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 20:52:55 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 20:52:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 20:52:56 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 20:52:57 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 20:52:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3cc7ae06783159e8c992cfb745833f904e836c74a7704b7a90b4b45a598f878c`  
		Last Modified: Tue, 22 Nov 2022 22:39:08 GMT  
		Size: 3.4 MB (3408493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a37c442de2a21f08a06c070be942937c1aeb2d575ee7f97481ddb0824cf78`  
		Last Modified: Wed, 30 Nov 2022 21:03:52 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a23eec619e4e811c404de0e825eec062d21d1d543ff1e9c155b84e71aeac772`  
		Last Modified: Wed, 30 Nov 2022 21:03:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f1f76dee1e27cef35e75ebc25a6fdee7ad22a9e147a57fdefdfa77dc2cd916`  
		Last Modified: Wed, 30 Nov 2022 21:04:38 GMT  
		Size: 94.8 MB (94806953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5d0f315af85a583c7376fcf78c39d62798b6f518795102bd25f1891dc92fba`  
		Last Modified: Wed, 30 Nov 2022 21:04:26 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb305bef7f007fd65fe4b04f4a3f2baf6b3148775118756030632a81f3638c8`  
		Last Modified: Wed, 30 Nov 2022 21:04:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2592bb237438be605a105a5ca39457ed5019a8ac7584883f233f592bd3c3c6c5`  
		Last Modified: Wed, 30 Nov 2022 21:04:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94008fc5561f83eddc0201e54aa285a4cbda1e07f9e0f63eb276c104c509fa42`  
		Last Modified: Wed, 30 Nov 2022 21:04:26 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:3df9a1140c452add82c0b15f5f1aa820c24a37d034112d2c006f166fe6ec9ca3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93974677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c877ff1974e1440578a13d9b996555d7aff2402710db4d237f4dcd010bc8c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:47:02 GMT
ADD file:d8cbd162b64e4b7a8b83086be37ef5ee69e955ac955ebbe59e70c6be2a2d1a9f in / 
# Tue, 22 Nov 2022 22:47:03 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:25:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:25:41 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:25:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:28:39 GMT
ENV PG_MAJOR=14
# Wed, 30 Nov 2022 21:28:39 GMT
ENV PG_VERSION=14.6
# Wed, 30 Nov 2022 21:28:39 GMT
ENV PG_SHA256=508840fc1809d39ab72274d5f137dabb9fd7fb4f933da4168aeebb20069edf22
# Wed, 30 Nov 2022 21:31:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 30 Nov 2022 21:31:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 30 Nov 2022 21:31:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 30 Nov 2022 21:31:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 30 Nov 2022 21:31:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 30 Nov 2022 21:31:09 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Nov 2022 21:31:09 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 30 Nov 2022 21:31:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Nov 2022 21:31:09 GMT
STOPSIGNAL SIGINT
# Wed, 30 Nov 2022 21:31:09 GMT
EXPOSE 5432
# Wed, 30 Nov 2022 21:31:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:844b8973ca9523380e35625da9a5fd2d50338c403129146541e13d0722c056f7`  
		Last Modified: Tue, 22 Nov 2022 22:47:59 GMT  
		Size: 3.2 MB (3170814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e278c29da4e88947f0cf508855d1d896131ea7b8ddbe6f306e8314d9a3edab`  
		Last Modified: Wed, 30 Nov 2022 21:41:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5e60a6975908e5003d121a4ff442fc39146ab3c7f7c4e0d9dd52b9814f59c2`  
		Last Modified: Wed, 30 Nov 2022 21:41:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f77f1d51d4e3dce1cd61e3ac13546c9b4b2ea2be91771df2454efb09e4d8473`  
		Last Modified: Wed, 30 Nov 2022 21:41:51 GMT  
		Size: 90.8 MB (90788164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6805ba5e5fdf508f8c5bf7c4359d07617e6b20c5052a128b52c718132702`  
		Last Modified: Wed, 30 Nov 2022 21:41:40 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f57fc879f5b3bef7ef77e6e73400059079341378ba80bc79691d8debee297e`  
		Last Modified: Wed, 30 Nov 2022 21:41:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388763d7b5df1d1a9a6ad2469aa2fc04314b4bb17b0ea93e9e591b78d4ee3fb3`  
		Last Modified: Wed, 30 Nov 2022 21:41:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c3fcc5d47e265e3ce6ddc8ba29f884b8344a5fba82e4d55c79aba511c1248a`  
		Last Modified: Wed, 30 Nov 2022 21:41:40 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
