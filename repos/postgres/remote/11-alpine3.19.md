## `postgres:11-alpine3.19`

```console
$ docker pull postgres@sha256:5fccaafe25f1e414f74082c69e7150d33e03c473adbfba483a0a19e4c281c5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; s390x
	-	unknown; unknown

### `postgres:11-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:93d6dc7c9fea3535c331717465259b77e0a768ef5e2854bccf9501d340483d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90830494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d7fb41183afb2f06353ad0c08361a8af768a0c73bb6296018d3959792cf8b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV LANG=en_US.utf8
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_MAJOR=11
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_VERSION=11.22
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Fri, 08 Dec 2023 11:47:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.19"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 Dec 2023 11:47:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 11:47:00 GMT
STOPSIGNAL SIGINT
# Fri, 08 Dec 2023 11:47:00 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 Dec 2023 11:47:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d5f75d0d369cd541cf0a820f64f2dc12f0b847e733727f56a5dbae64334497`  
		Last Modified: Fri, 08 Dec 2023 22:16:13 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6e46f43853b9cb6a83754dbf20f0f0f24e60aa95947f37a24883a9f6369d36`  
		Last Modified: Fri, 08 Dec 2023 22:16:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461502dc2d2fc61c1d6eb622fb333b90f498090c5d4c79e5b49199b5e558b32f`  
		Last Modified: Fri, 08 Dec 2023 22:16:17 GMT  
		Size: 87.4 MB (87407572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143a11ba1b82cec139ce0b0f6c8895e4be26c70b5c02f67beca350df035e7a4`  
		Last Modified: Fri, 08 Dec 2023 22:16:13 GMT  
		Size: 8.0 KB (7983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea4ef0bd3f1ce32f77be9309ba63d482de988c729c37cd87dfb0322eb576029`  
		Last Modified: Fri, 08 Dec 2023 22:16:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7637f1518faaa79483494dc8dd7553d5a52c79d11acce381841bbbe435de12bb`  
		Last Modified: Fri, 08 Dec 2023 22:16:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c3c3e77d69865558473bddc3d02e6c47e902a9a9f501f31d65944d0071ca0`  
		Last Modified: Fri, 08 Dec 2023 22:16:15 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e33643a62077744f6a441c42fef5418bbd8aae74f5c9997208559546b355e964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.5 KB (841501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41eec042416f0fb6d401739325e7fcbb23a1db4d43a85662194a005b4e8a6af1`

```dockerfile
```

-	Layers:
	-	`sha256:d186b1abd7489a90ae698ed541c871b8fdb37738c710d4f26ec9f941a9736b70`  
		Last Modified: Fri, 08 Dec 2023 22:16:13 GMT  
		Size: 805.8 KB (805780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3949fba152c29153d5d6a7d5e2b06d6826ed50255af54bee414826dd3546e84`  
		Last Modified: Fri, 08 Dec 2023 22:16:13 GMT  
		Size: 35.7 KB (35721 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:9c3dd80e62ea76f1810a29fa19b6eeecbb1251349341aa0bd9627d0b965ec7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89696840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaf5bb20b6ad70ea5d80461d4f0622a1458c5aaf12daebaa81aff332fe495b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV LANG=en_US.utf8
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_MAJOR=11
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_VERSION=11.22
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Fri, 08 Dec 2023 11:47:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.19"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 Dec 2023 11:47:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 11:47:00 GMT
STOPSIGNAL SIGINT
# Fri, 08 Dec 2023 11:47:00 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 Dec 2023 11:47:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fe015dc9b3d1803ee85ee6a801a8a7e2d6311686b2f37622ccbe41860d2ed3`  
		Last Modified: Fri, 08 Dec 2023 23:56:18 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a72ec48bcaaa26d249e92564caffd5723eebb17b13de29d037b52a50729964c`  
		Last Modified: Fri, 08 Dec 2023 23:56:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc8cc77dd06177640cf3e4477dfa96285cb3fb3f61ba52afc7ea0751eca4548`  
		Last Modified: Sat, 09 Dec 2023 00:27:30 GMT  
		Size: 86.5 MB (86517255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520765392832afb8ce8ad5311d9f60c9174cdaaaed35d74f593f0932abde779`  
		Last Modified: Sat, 09 Dec 2023 00:27:18 GMT  
		Size: 8.0 KB (7983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46e58400f5cb63bf32ae08957bebe3f1535cf601fb88a8fa4c0cfb28e7c0a0b`  
		Last Modified: Sat, 09 Dec 2023 00:27:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ff1d22e5271320770eb0e7584bd9afc2ed72fcaac5f7edc2be07a6db897f46`  
		Last Modified: Sat, 09 Dec 2023 00:27:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb14f15e37ff577451898ed7eb8c5d9ab85ad4b4663e79b9d7ee8fd78f487418`  
		Last Modified: Sat, 09 Dec 2023 00:27:19 GMT  
		Size: 4.8 KB (4781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:089124d17f322a88f7a145e4ce471d93738375eefafd5a968db0ee8c6a464011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99515272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964d1b6ccdf23bf641e305caa144f3857caf233a079c8ddb094f99c953a9c2c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV LANG=en_US.utf8
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_MAJOR=11
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_VERSION=11.22
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Fri, 08 Dec 2023 11:47:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.19"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 Dec 2023 11:47:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 Dec 2023 11:47:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 11:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 11:47:00 GMT
STOPSIGNAL SIGINT
# Fri, 08 Dec 2023 11:47:00 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 Dec 2023 11:47:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98867b7d9ef52d8ea690ad6ab7a1162c3ffb223f498cfe46c5a0c19b26b5df4a`  
		Last Modified: Sat, 09 Dec 2023 02:05:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca1d0e320956171da67959a489db8954c94e3093132a48ee544fcaf765d7784`  
		Last Modified: Sat, 09 Dec 2023 02:05:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fb00dd51da13ead231162788e37d45da7303d6354c161bc2193db1a068fa96`  
		Last Modified: Sat, 09 Dec 2023 02:42:04 GMT  
		Size: 96.3 MB (96258500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e361b5713fd7387d3d7afe1e63e9d65edbd6d2596e6256acdb15e895bd4e832`  
		Last Modified: Sat, 09 Dec 2023 02:42:01 GMT  
		Size: 8.0 KB (7985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf8eeb2b44c369fd376d3ad1b4cc8f3120932398f844d716e62594bfc4ae5b7`  
		Last Modified: Sat, 09 Dec 2023 02:42:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fb327f87f37ee081f9612ad45d03dfa3c253ad98ec66906751b303505e369`  
		Last Modified: Sat, 09 Dec 2023 02:42:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7fa4af6338aa402c1b5b750c4a8dc75e061805cd81f4d1e7e451f88fd066f2`  
		Last Modified: Sat, 09 Dec 2023 02:42:02 GMT  
		Size: 4.8 KB (4780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:24596461be867f4c04f044eb72fa02b604d3a7c581e4624cbdbf98d83c5e918e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.7 KB (839698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1343afab22500e270392fcfa027285d38eca81cc75c9d17bd287eaf0d024ac`

```dockerfile
```

-	Layers:
	-	`sha256:0b8af6b229308fc1d80b03c06fb70261edc82c83c901cda03a694aaafad3980f`  
		Last Modified: Sat, 09 Dec 2023 02:42:01 GMT  
		Size: 804.1 KB (804144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aae6a254650864fe88f03ea317038484d0f99cc0bc30caed817194f851826b0`  
		Last Modified: Sat, 09 Dec 2023 02:42:01 GMT  
		Size: 35.6 KB (35554 bytes)  
		MIME: application/vnd.in-toto+json
