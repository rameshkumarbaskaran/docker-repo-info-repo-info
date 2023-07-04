## `postgres:16beta2-alpine`

```console
$ docker pull postgres@sha256:439f2215d6e93b5fa0dcb621aef983e5ab99836e23ed2e1d29ff34e991758082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `postgres:16beta2-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7079207be5a4a09a2b997d36c8f7cca41f71b8cf61e2b3419fed12391a769ff7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92873663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09820e7162099a9f68221f5f0ab7043d389079ae71dad9fb00df31e58c4509f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 18:56:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 18:56:23 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 18:56:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 18:56:24 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 01:01:43 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 01:01:43 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 01:01:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 01:04:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 01:04:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 01:04:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 01:04:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 01:04:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 01:04:29 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 01:04:29 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 01:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 01:04:29 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 01:04:29 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 01:04:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd788ea942919017d4b7ef0045f6562b5dedeeea5929dde74db00394b9effd7`  
		Last Modified: Wed, 14 Jun 2023 19:34:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3230cb44ffa2c0e180c66587eea332cbdfa3f7b41a5ed589836a7c1924851766`  
		Last Modified: Wed, 14 Jun 2023 19:34:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d6c1ed8794d7f35488ec7ec52a8f86ec1e86134011c6b24668e7dcd4c8a575`  
		Last Modified: Tue, 04 Jul 2023 01:08:31 GMT  
		Size: 89.7 MB (89714158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631ad3d03ca55b42820731d312f82e0d3e8b7ff0a3a2f7a19f8ba7d1f0a94334`  
		Last Modified: Tue, 04 Jul 2023 01:08:19 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a2ec42948394bf30214bef3c6cdc4cf40d93d10e420f6db7d46f38eb1c61`  
		Last Modified: Tue, 04 Jul 2023 01:08:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3653a3b0fdf7c2ad9d5591e693abd93141c8bc18674a211da2149345b6c0c5`  
		Last Modified: Tue, 04 Jul 2023 01:08:19 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827ccfc892eb3acf6ec7e6accbc913f32453bfd76988c51d13a86371a8dacbdd`  
		Last Modified: Tue, 04 Jul 2023 01:08:19 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine` - linux; arm64 variant v8

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
