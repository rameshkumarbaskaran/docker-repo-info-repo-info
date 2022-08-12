## `postgres:15beta3-alpine3.16`

```console
$ docker pull postgres@sha256:6a9d2699118bab7b614f6b071446103ca3bf60f2a008067124efc733f7b77dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `postgres:15beta3-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c7d3be7fa9419a4ee045427454b4422fc1d1e1eab4765a6cf35de1994a69765c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84379997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f8fd75aa2fbf355ac8516b4a3961240c6a82740a9be8a377633bd7114b9f70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:26:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 10 Aug 2022 02:26:40 GMT
ENV LANG=en_US.utf8
# Wed, 10 Aug 2022 02:26:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 10 Aug 2022 02:26:42 GMT
ENV PG_MAJOR=15
# Thu, 11 Aug 2022 23:47:45 GMT
ENV PG_VERSION=15beta3
# Thu, 11 Aug 2022 23:47:46 GMT
ENV PG_SHA256=1a6e2a454b6bcdf76aa4e50573d2fa1ea8db2cdfaa3282a7538830bd285b27bf
# Thu, 11 Aug 2022 23:51:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 11 Aug 2022 23:51:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 11 Aug 2022 23:51:20 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 11 Aug 2022 23:51:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Aug 2022 23:51:22 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 11 Aug 2022 23:51:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Aug 2022 23:51:25 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Thu, 11 Aug 2022 23:51:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 23:51:26 GMT
STOPSIGNAL SIGINT
# Thu, 11 Aug 2022 23:51:27 GMT
EXPOSE 5432
# Thu, 11 Aug 2022 23:51:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75aada9edfc58771473e8896a13640c97ada8da22ee2296fb12338c45d0ab8d7`  
		Last Modified: Wed, 10 Aug 2022 02:49:40 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8207736937506f07b9ceed008216a1acbd1e12c8e770a48463266154eea5a296`  
		Last Modified: Wed, 10 Aug 2022 02:49:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76da40a90edf77ec2b06e08547ec77b865950d03924d5d761ab25bf61491c774`  
		Last Modified: Fri, 12 Aug 2022 00:13:31 GMT  
		Size: 81.7 MB (81656498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f534f62a061a38dbefc530f1b366c9f41a8d9aad3d2f01bbaae2495c021c85`  
		Last Modified: Fri, 12 Aug 2022 00:13:20 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aca7edd1d6378f8b8e056b70ae9dc6aec17d0d825bffb7f747360d0fca73275`  
		Last Modified: Fri, 12 Aug 2022 00:13:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa3798e7c3f716c259220617c653f00e63594c1e52bd911907a04805e83b952`  
		Last Modified: Fri, 12 Aug 2022 00:13:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cf39226911bf39fdf8e159ada13fb0e636adeb2d1178c04ab9fbc49a6c1a70`  
		Last Modified: Fri, 12 Aug 2022 00:13:20 GMT  
		Size: 4.7 KB (4700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
