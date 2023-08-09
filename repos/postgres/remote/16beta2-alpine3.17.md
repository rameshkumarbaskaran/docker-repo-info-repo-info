## `postgres:16beta2-alpine3.17`

```console
$ docker pull postgres@sha256:51e76290ac7848effecdb8048e3f18a4dc616f74170065712e5bdd61cfd2c1fd
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

### `postgres:16beta2-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:fe267ade8bd44bdf3527be7a5d1a8e91a854f3ef4572bbbd6db35e364fcc5f04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94989072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5b048bc2fc4a7862b2ddd807ece19df57190143cab023e220bba45fea73cf`
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
# Wed, 14 Jun 2023 21:13:16 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 02:11:03 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 02:11:03 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 02:11:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 02:13:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 02:13:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:13:52 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 02:13:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:13:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 02:13:53 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:13:53 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:13:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:13:53 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:13:53 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:13:53 GMT
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
	-	`sha256:870449159f756b9b73318fd20bb7c6eec290907a62af101ba27376b2f6e4fa51`  
		Last Modified: Tue, 04 Jul 2023 02:20:12 GMT  
		Size: 91.6 MB (91598215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f299a65bd53807084d85d7d7bfdc3784e0f44187adb6e6ada56fb8d84476024`  
		Last Modified: Tue, 04 Jul 2023 02:20:01 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754ec3ec9c4cc589c8939126bf7951108b213aaae91c5232ddc28ef9cd1d862e`  
		Last Modified: Tue, 04 Jul 2023 02:20:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2714ad5d05b692c63a422109e9780985eeeab914a4e58cf93b5a456bf0a5ec5`  
		Last Modified: Tue, 04 Jul 2023 02:20:01 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8248616bae60fbf1d7450f2605b884c3c769d882a31f0835078be066cc732c99`  
		Last Modified: Tue, 04 Jul 2023 02:20:01 GMT  
		Size: 4.8 KB (4794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fd17893398860d932950ccec7bed28df023a345719b2fc93075a1cbc7de8e709
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92761443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7c287e03fee34be1fdcfdb1631e927f79859ec4f49f0f35693585389d9d92`
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
# Tue, 08 Aug 2023 22:26:22 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 22:26:22 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 22:26:22 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 22:26:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:29:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:29:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:29:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:29:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:29:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:29:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:29:17 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:29:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:29:17 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:29:17 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:29:17 GMT
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
	-	`sha256:ccd836d65f1cdd8e21bbf0749ab2955a18c2313689bb21af3cc4c0cf81d8672f`  
		Last Modified: Tue, 08 Aug 2023 23:03:00 GMT  
		Size: 89.6 MB (89632844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f3a1eb76d734f6a074b6c5151b6493c24dab62ad63ad4ed353549ea5788b6a`  
		Last Modified: Tue, 08 Aug 2023 23:02:44 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d14e69b67d5a890f5c9076bfbb6f8379543b9139f3d10cb1d9e7545fe95023`  
		Last Modified: Tue, 08 Aug 2023 23:02:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0348a5e7a857ac0dd68412a7acdd46272da3b464b9dedd0a9ac1405a76db2`  
		Last Modified: Tue, 08 Aug 2023 23:02:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d0ba8230e5977b8862454d8e60f2b51515ef658b36626709bde31a49f3b789`  
		Last Modified: Tue, 08 Aug 2023 23:02:44 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:518a5ad1a8efacf66bfb34eb739e8300a9532209beb19396e6400f25e6035900
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87404723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110d70a35683ab70ec0513b1f056faaf7f47a54c213d2943b11fea60cb9400b`
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
# Tue, 08 Aug 2023 02:34:36 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 02:34:36 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 02:34:36 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 02:34:36 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 02:37:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 02:37:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 02:37:05 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 02:37:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 02:37:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 02:37:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 02:37:05 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 02:37:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 02:37:05 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 02:37:06 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 02:37:06 GMT
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
	-	`sha256:e136434424fc4b828c090f4f54d79213be6d62130334a4aff0466e8c4762b465`  
		Last Modified: Tue, 08 Aug 2023 03:01:45 GMT  
		Size: 84.5 MB (84519152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adbd19e417ce43da7be81e1bf5e05fa1ad8dfc7607641bc92a01ad99ac9e088`  
		Last Modified: Tue, 08 Aug 2023 03:01:35 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0859ac1fdec85c25633ebba37128fdccff83f0abb268806ddad832456a1ce000`  
		Last Modified: Tue, 08 Aug 2023 03:01:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150e11a909ec2fd5980e39965350a8b4a78d00d0ab0059e7a5b931b4c1951140`  
		Last Modified: Tue, 08 Aug 2023 03:01:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4509f1fb6e85c70636a797128aabda519efbe5b6e8cb62cf5dde8a809a68dce1`  
		Last Modified: Tue, 08 Aug 2023 03:01:34 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f5c25cd1e29f5b80c1aae2e0634816b0bb2de2381c4d9a708fb0c41ffb6c49d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92708107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2190e4b7179546bb5f4d29268a55f0adc7faacaf9304761c3ecf0629a870f5b`
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
# Wed, 14 Jun 2023 21:04:39 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 00:46:29 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 00:46:29 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 00:46:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 00:48:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 00:48:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 00:48:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 00:48:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 00:48:51 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 00:48:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 00:48:51 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 00:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 00:48:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 00:48:51 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 00:48:51 GMT
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
	-	`sha256:2afc919f0fd7a79058f8014a36881eb9ffecd8ddc65c4528d771c957af879fda`  
		Last Modified: Tue, 04 Jul 2023 00:51:16 GMT  
		Size: 89.4 MB (89430823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d58c81e38234159ddece4735ca524cac8334141338afa5c1632d80b059a59f`  
		Last Modified: Tue, 04 Jul 2023 00:51:08 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a4c9e148d093368169fc0da50d6211df83ea138076c0639690840fc03db82`  
		Last Modified: Tue, 04 Jul 2023 00:51:08 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925497c9a54e79c48267f10127bc2a59bb58a0b83a31683b2244f09d45778ce9`  
		Last Modified: Tue, 04 Jul 2023 00:51:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc0e56af49eb720238d46559958b84e067fd4dfd039831ffbeb5a204cf2ed2b`  
		Last Modified: Tue, 04 Jul 2023 00:51:08 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:be0f43267c54d91848ed63d59ea4eb80c662af30954b041a8a90b7a2742d6bf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99863752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea675977f537d61066f8868878e538bd381c42ceef31d0245ef1b9b2a635ea4c`
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
# Tue, 08 Aug 2023 20:44:23 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 20:44:23 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 20:44:23 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 20:44:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 20:49:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 20:49:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 20:49:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 20:49:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 20:49:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 20:49:49 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 20:49:50 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 20:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 20:49:50 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 20:49:50 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 20:49:50 GMT
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
	-	`sha256:c0a6a21379e2ca6b48f7887698e4a5431f0e76d8ae38e4f14147133636ce8f42`  
		Last Modified: Tue, 08 Aug 2023 21:40:30 GMT  
		Size: 96.4 MB (96433828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b89fb7a35a4434a0a07a2f361b1945131a5c938aa91826ce85db25d90f00f`  
		Last Modified: Tue, 08 Aug 2023 21:40:13 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d20c23f658e33bc6319e0076cf0c968ee4c1bb0afce9c8123f37404f13df80`  
		Last Modified: Tue, 08 Aug 2023 21:40:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e81f531912437308ee2c752ed2719a1b1c618127bf2aea2d196d799df7de452`  
		Last Modified: Tue, 08 Aug 2023 21:40:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f592603b68fbcf7fc04a7cd2b12b14d5b8c10ac11b656f8aabe5785d1453c77`  
		Last Modified: Tue, 08 Aug 2023 21:40:13 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:266a59c0cdd2c1d8e83d0a5734219bdf500a6c62855da80b4a8063af53d8b0a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100869482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aaf48ee26e6bac09c1393aa43f28c760b7a38dc9b88ac74cb30d24f9441e8e`
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
# Tue, 08 Aug 2023 22:11:16 GMT
ENV PG_MAJOR=16
# Tue, 08 Aug 2023 22:11:16 GMT
ENV PG_VERSION=16beta2
# Tue, 08 Aug 2023 22:11:16 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 08 Aug 2023 22:11:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 08 Aug 2023 22:15:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 08 Aug 2023 22:15:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 08 Aug 2023 22:15:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 08 Aug 2023 22:15:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 08 Aug 2023 22:15:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 08 Aug 2023 22:15:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 08 Aug 2023 22:15:25 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 08 Aug 2023 22:15:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:15:26 GMT
STOPSIGNAL SIGINT
# Tue, 08 Aug 2023 22:15:27 GMT
EXPOSE 5432
# Tue, 08 Aug 2023 22:15:28 GMT
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
	-	`sha256:e341e1e63992abe6aa45a153fbeb9014b8aa803f62a082df0aec05e3074b2463`  
		Last Modified: Tue, 08 Aug 2023 22:57:15 GMT  
		Size: 97.5 MB (97461982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13703ad0bd2e46008add8f988c0f6490e931d655fae55c27225a1a64b4ea43c8`  
		Last Modified: Tue, 08 Aug 2023 22:56:53 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c974b61b7fc11ea26d3fc525214ab95e94de7bb65b8669216bedf5d82ab0ede`  
		Last Modified: Tue, 08 Aug 2023 22:56:53 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56739a2a31da9521657f00e27a4b7bc561eb39e6324942445696632b764506b`  
		Last Modified: Tue, 08 Aug 2023 22:56:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7ec71deff48c01730b43895cd13c0074148de1d8c8899a1e31776bf3d5b25`  
		Last Modified: Tue, 08 Aug 2023 22:56:53 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:c05ece789211f6f3591d670db2581b5e5eddd03e2f2e36835121c2b129c80d27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95550118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70692b2a5be6d8701c9d19d59a7fc96f150274d420ec36c068160e7e1e6d1691`
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
# Thu, 15 Jun 2023 12:43:43 GMT
ENV PG_MAJOR=16
# Tue, 04 Jul 2023 02:03:09 GMT
ENV PG_VERSION=16beta2
# Tue, 04 Jul 2023 02:03:09 GMT
ENV PG_SHA256=ba653197465180c93775b4949a89dc6fbfebae2a44587ae7168fdfd24f519b50
# Tue, 04 Jul 2023 02:03:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 04 Jul 2023 02:05:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 04 Jul 2023 02:06:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:06:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Tue, 04 Jul 2023 02:06:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:06:01 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Tue, 04 Jul 2023 02:06:01 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:06:01 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:06:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:06:01 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:06:01 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:06:02 GMT
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
	-	`sha256:7a56e0c898cabee85f79f159705e12e67a2e35430deef951ee204d66326e4083`  
		Last Modified: Tue, 04 Jul 2023 02:16:36 GMT  
		Size: 92.4 MB (92359079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c072d31f4a03ddfb11e077f03cac84110f5c93a9daa974d9325ce4ca9c781f`  
		Last Modified: Tue, 04 Jul 2023 02:16:25 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301ff84b34190ebc1fa03fd637b1275649b32e6b16fba746be07d8f555c0083b`  
		Last Modified: Tue, 04 Jul 2023 02:16:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf219316750e76f541bd06f574704a1b3045226706c35fc605080754fac219a6`  
		Last Modified: Tue, 04 Jul 2023 02:16:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10330a335172c2f72958a399ff6c675be67417ab970a2829f99df380f6b17eb`  
		Last Modified: Tue, 04 Jul 2023 02:16:25 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
