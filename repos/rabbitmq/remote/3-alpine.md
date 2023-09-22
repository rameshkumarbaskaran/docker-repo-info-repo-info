## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:97dd24c8c951c3075891048230e22d92cb9a5efd888e4941310d0190f6d62790
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:3-alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:3e51f138a09c63a46b5fd56acd9498a50d226d2d1e0cf6746bb39344e74853b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71038440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89075ce3f843d028696108f358e86b6b7efdbfc26de43081e32f8d16740b7e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c7969b815567442ee90e730a6c266bb35c8fbc3c079197d4c89bdcde19133`  
		Last Modified: Fri, 22 Sep 2023 01:01:32 GMT  
		Size: 40.1 MB (40075694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3120cdff8159d880cd6bc5a57176dd316420b9c3319ff85881065f980a863f87`  
		Last Modified: Fri, 22 Sep 2023 01:01:30 GMT  
		Size: 7.5 MB (7545685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afb840a0e8564cf424c3aa2eb0662f2ba2276c8eff7821154ea5979d3e7585`  
		Last Modified: Fri, 22 Sep 2023 01:01:29 GMT  
		Size: 2.3 MB (2297414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5070dc03b6bbcd715bc367e6b79a7a534d0d5b4e1ec358db3a0d6d1ed60624`  
		Last Modified: Fri, 22 Sep 2023 01:01:30 GMT  
		Size: 17.7 MB (17716284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65361806a0b60b81da06adf93467ea716368c82efb95b2ff679ae2e179078124`  
		Last Modified: Fri, 22 Sep 2023 01:01:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d6689be45e92d946195956b42c6f4ca23134139a517db92db1f86900fc1180`  
		Last Modified: Fri, 22 Sep 2023 01:01:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3637d8998cd746f39d59d618c31a9f5e01b4c163cef10cab1b90dc20d118cbe`  
		Last Modified: Fri, 22 Sep 2023 01:01:32 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5716d711e46260633a4bb85d3b91bf4849f6ec5fc18bac969b4a7f9f34674`  
		Last Modified: Fri, 22 Sep 2023 01:01:32 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:68f8cb0463ecd71a04d8fdcd1c23c1110ca50e589afff448622891d198755312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.1 KB (763070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be985c47cb63e719070629fe8a56d949a06698ee53831e5c3c3aa20dec20d582`

```dockerfile
```

-	Layers:
	-	`sha256:990224ecac381ca83d263129161c729db79957fb22fb9a3df07251a3167d1d0c`  
		Last Modified: Fri, 22 Sep 2023 01:01:29 GMT  
		Size: 701.5 KB (701508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e45c8dee6393cf862edee7aaa892cfdef72759068b6d0187203300205815e9`  
		Last Modified: Fri, 22 Sep 2023 01:01:29 GMT  
		Size: 61.6 KB (61562 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:e52f3a76a78c665089fcf0f7ee56e0025148249251ee92332826fbdbbfbde15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61040310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b08ba569fd882f3f8abe36d62e1ccd8c909a5ac78d1bf8c9a6fe2df2609315b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fca504aed6a382d225007e2809700d071b7ec32a28ae66cd0949fa1047946d`  
		Last Modified: Wed, 20 Sep 2023 03:25:49 GMT  
		Size: 32.4 MB (32389524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1fb3f16431a00ae406c4505d889c7d04a484f713eff8ea507eb26c58d5cbe0`  
		Last Modified: Wed, 20 Sep 2023 03:25:46 GMT  
		Size: 6.4 MB (6375339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebb7571cdfb0ab7c17ba7bba5a2a9b347705581e5d09900636b6745eb202376`  
		Last Modified: Wed, 20 Sep 2023 03:25:44 GMT  
		Size: 1.4 MB (1412521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992ff67238a02826f4e5d945bd9d6ccce87b9f46c29b2c42c99bdb3e99e9554a`  
		Last Modified: Fri, 22 Sep 2023 01:22:36 GMT  
		Size: 17.7 MB (17716371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33136a7537841ff8b69a97802a76cbffbea99c7acb5d34b3ae86eb95e70c5dcd`  
		Last Modified: Fri, 22 Sep 2023 01:22:35 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b4816aacf1db9507e1b0ff6630b7b3d976dd3fb9b06c67ca73653b68ffaac9`  
		Last Modified: Fri, 22 Sep 2023 01:22:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afcde8d5e57cc93b66d7ab756e5d2223678e3b8b0ea29f9f6797a219c6a7f72`  
		Last Modified: Fri, 22 Sep 2023 01:22:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9316df1f43f5df6694e633c5bcddce92ed92e5a1162372316015b664db2dedc9`  
		Last Modified: Fri, 22 Sep 2023 01:22:35 GMT  
		Size: 828.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:119e52f85e98dfd6dade66100cdb118c01f1554b1017d2bd7318063a92b1bc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60265943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5376d31a25465628ffb7ff94373edbbef334940712cce3e9b8ec459c52c76f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9aa11752e21d53b8ddc71456f282180ac82aab3aabb7f3e2c45b6523fe1ad0`  
		Last Modified: Wed, 20 Sep 2023 11:45:58 GMT  
		Size: 32.3 MB (32267884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d68aa42458019573125737bc5d39532faf59e3952dc03e09d3d06222f4657e`  
		Last Modified: Wed, 20 Sep 2023 11:45:57 GMT  
		Size: 6.1 MB (6080057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075220e4c956ce1b1819016d45dd2461c3369dd30e1923d7ba9b5d68dc7a9de7`  
		Last Modified: Wed, 20 Sep 2023 11:45:56 GMT  
		Size: 1.3 MB (1300454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f73f4424e4025b2e0232647f773e219bd1b4cf30ec51384ef5d39d9420477f4`  
		Last Modified: Fri, 22 Sep 2023 01:04:39 GMT  
		Size: 17.7 MB (17716317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fdbccc2c0af6726ae925d1b583e26bc4c20d5b4f2e9bd80d547dd975b16bcf`  
		Last Modified: Fri, 22 Sep 2023 01:04:37 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2bab0e3180d52d814c5272b7cfbdb4d3b3caab5e256e297e29de3cfc66944c`  
		Last Modified: Fri, 22 Sep 2023 01:04:37 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b7455d57f69a861297d8d4343399c2d4877fe2c9e25153cc7e063901f04c3`  
		Last Modified: Fri, 22 Sep 2023 01:04:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1794ad4a0922951af99c37f89d91a85584bb4ffc3d7e0ca5f2fa98c27bbf4e9`  
		Last Modified: Fri, 22 Sep 2023 01:04:38 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:fb4995da9442f9f041574f5b01fb7f65743ba4cc44bf944c57432020adb5d714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (759009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5f17fcaf9a73b39549bd66a33dd48aee7c196dc8b9d71e6c91295b45ffefe7`

```dockerfile
```

-	Layers:
	-	`sha256:95264d65cb53c45758ba5ed14b196ef476e1fe8e9af328b6766836328ca1f745`  
		Last Modified: Fri, 22 Sep 2023 01:04:37 GMT  
		Size: 697.4 KB (697426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd39bdbf7f065ef910cc46b97feaa41b8831eca7cf942d18b429a182c67985d`  
		Last Modified: Fri, 22 Sep 2023 01:04:37 GMT  
		Size: 61.6 KB (61583 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:51b8af2ebd0437f6170bb1b3a9d7d2fbc5d87ef354db2618c4027527cb2bf5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68429384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d021a2f3c650d7acb4e81989ca8de6f86032d65ba8562b14d8973bc38e94625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c7765b0d8d4f70e001f2b32626fd09732fb82c6f9dbd7cf6f4802080d686d7`  
		Last Modified: Thu, 21 Sep 2023 05:34:22 GMT  
		Size: 37.9 MB (37874066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceef8ebe5ac239ded38039ead06f8c8434d8fd16a041a3897af7e347b4780c1`  
		Last Modified: Thu, 21 Sep 2023 05:34:20 GMT  
		Size: 7.1 MB (7137759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4cc5a4fabcc804763e217b569abc6d3e146128635b76963d7c63acad641cc8`  
		Last Modified: Thu, 21 Sep 2023 05:34:20 GMT  
		Size: 2.4 MB (2368800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fa8dada2054b1a60563d6654717747d6f08c6d8652fbecf88aaba155ac86b2`  
		Last Modified: Fri, 22 Sep 2023 02:30:59 GMT  
		Size: 17.7 MB (17716247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd1969aeaa8017dd1c9e4c3ae29a0fff1271981baf5612e767a309ff164e80`  
		Last Modified: Fri, 22 Sep 2023 02:30:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7628e068eeca86bfe30c012f9e763373d33534a6fc79a07787585b2352b4312`  
		Last Modified: Fri, 22 Sep 2023 02:30:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedb660c6583ac196fd78be37cb7192080598d0c8e65ecaa4a915b41b549866`  
		Last Modified: Fri, 22 Sep 2023 02:30:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287bfb711d18924414188b96ee8657f513c8bbb8294d0118a99a2a39daeb83c0`  
		Last Modified: Fri, 22 Sep 2023 02:30:58 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2d6b5c9b0368293caa1d04dcee786fc67b887dd72b6a3094fbe5313ca8e4febf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **762.9 KB (762936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356d93d56f46dbdb5ec64be906f3f2d44b7bf0eba5021d0ef62903811e684a5a`

```dockerfile
```

-	Layers:
	-	`sha256:577d87c9b57f5520d5be95fbc05bec53164524ff1c3d3bcb7948d5139642459b`  
		Last Modified: Fri, 22 Sep 2023 02:30:58 GMT  
		Size: 701.5 KB (701530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e11beebd35191ccc736ae425484d3c5722d58dd2075773753acb92e813ec347`  
		Last Modified: Fri, 22 Sep 2023 02:30:57 GMT  
		Size: 61.4 KB (61406 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:f1e949ad30e083ad62ad364857d190a9cd5897e348e702da1005a40d79a90032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62415616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef661bef0c7297dd2c1f8a9be9177ed7f321843d21c8248ee3429da98665e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c9a21323a13217e3852f14103ea7c209a5f785999abf65cd9a2fd2bc221118`  
		Last Modified: Fri, 22 Sep 2023 01:01:12 GMT  
		Size: 32.6 MB (32623451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f384d10061fa643fdc38670783eaff91ab53726397e844eeb21e4942d9836`  
		Last Modified: Fri, 22 Sep 2023 01:01:11 GMT  
		Size: 7.4 MB (7437042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2936d706f45f8cffbd28e6972badd49a09d34c13dd721633b23d134291f9fb6`  
		Last Modified: Fri, 22 Sep 2023 01:01:11 GMT  
		Size: 1.4 MB (1401874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de470d16da0391e70c29154155f28e3856be1e7f6e4ec705e8edac334b4318a8`  
		Last Modified: Fri, 22 Sep 2023 01:01:12 GMT  
		Size: 17.7 MB (17716355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2e18c377c84e1ed1f2f6d011fd309f8767b226bd48e6fd396937f8c92fa071`  
		Last Modified: Fri, 22 Sep 2023 01:01:12 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0259cddba644b88c7cc074f3dfd68b3202e37b4d9dcc647f89ecb7058b76ad63`  
		Last Modified: Fri, 22 Sep 2023 01:01:12 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4b1ef490c796a78ab32455a772de535066d5f8322642f572f2347a301ba93b`  
		Last Modified: Fri, 22 Sep 2023 01:01:13 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc778c387abeb3e04daba135575342112832120e2d7d7f9fbc56346a0316db8`  
		Last Modified: Fri, 22 Sep 2023 01:01:13 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:dca5ba5137f22995b5c83b43c978b3b6ddead770228bad5ee7721ae6100b78bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c38e4c3534531b8cb1223ade589bc1f4e38a3c9242eb58421367698e71dcda`

```dockerfile
```

-	Layers:
	-	`sha256:812347c8d61dd914ecc298a4e0664d0e42a5e64c595ef502762b4654b7001654`  
		Last Modified: Fri, 22 Sep 2023 01:01:10 GMT  
		Size: 61.3 KB (61290 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:4b8f07599a8517026f590d7d286b277a4a9c20f0b818a8c59c22f8fa37ac18ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63343661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7619fc2bb8d8c2061f3a17f348e5a1c6950877027a0059e290c5ff5ee1ac451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a045c25fd11b9fd90c9e8967e9490e0eb21f7b1e405473eb8c85a73a08769c`  
		Last Modified: Wed, 20 Sep 2023 08:44:31 GMT  
		Size: 32.8 MB (32805164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f9d6257a6f4981201814c155a708f761c5077b00a95895bc7ead8d675dd561`  
		Last Modified: Wed, 20 Sep 2023 08:44:30 GMT  
		Size: 8.0 MB (7951879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7fc7533ba9756c4efc58f88a7a7f79f986adf9c7d39dae5811e8c313aa087`  
		Last Modified: Wed, 20 Sep 2023 08:44:29 GMT  
		Size: 1.5 MB (1522272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34628d068bf1102bb311fc873ced44f396da00a746c95c703a30a8d18d9ea5dd`  
		Last Modified: Fri, 22 Sep 2023 02:14:07 GMT  
		Size: 17.7 MB (17716344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c862d55f13f1356eb157cf3cbdf71b03ce2734b4e15866679182d1cc160a8fd`  
		Last Modified: Fri, 22 Sep 2023 02:14:06 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357b19a597f591258e320453a42068d152c2c70b7df0b9c69c432c38be97c1b`  
		Last Modified: Fri, 22 Sep 2023 02:14:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff03c900512264aff65227a68454ff671591bd92fc78c273626b74c731b8952`  
		Last Modified: Fri, 22 Sep 2023 02:14:06 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b4adf5196a34776810f9a50546ebc2e0372af7eee0274cadad31d4fd7b3a86`  
		Last Modified: Fri, 22 Sep 2023 02:14:07 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:94cb0de2466f4146c1aae00eef30cac09b5cb1ff4c657c350f2ea9a4cc14f79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.4 KB (757429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f934a0e05da6a3f4b1d4af0ec4e20b8d50479b199a9531c8721c0cd271d5e6`

```dockerfile
```

-	Layers:
	-	`sha256:d0645ac3ee3fd6fba9400ec7c8fdce143702652e69ccaa553c8ed4f562107e91`  
		Last Modified: Fri, 22 Sep 2023 02:14:06 GMT  
		Size: 696.0 KB (695977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03f33a97a4e1a1e057651354f8593f1fd225825374e22d811911d44d69af065`  
		Last Modified: Fri, 22 Sep 2023 02:14:06 GMT  
		Size: 61.5 KB (61452 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:dcdf137091607abe36bee14a2ac2a654f783a4a7d881dcdd3c51d4e2fc9739f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61333638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6ee5b3db00de9d75550f97ec74f4accc3772385fcf41e60f74ac17241afd3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 21 Sep 2023 11:05:32 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 21 Sep 2023 11:05:32 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 21 Sep 2023 11:05:32 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Sep 2023 11:05:32 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 21 Sep 2023 11:05:32 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88d919c3d0ab39d1f9e97c5a1fac53063d4389b588dcea8d0863754cdd1965`  
		Last Modified: Wed, 20 Sep 2023 02:50:25 GMT  
		Size: 32.5 MB (32478793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299a5ba791ff5c4429a715201d1eebfcc7f2c60923469bbe55323441f899454`  
		Last Modified: Wed, 20 Sep 2023 02:50:24 GMT  
		Size: 6.4 MB (6427072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e3bec233c1d961d75a55a6356c6fa1354aadad599a98a845a6dc543a1781f`  
		Last Modified: Wed, 20 Sep 2023 02:50:24 GMT  
		Size: 1.5 MB (1495500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e69e3a890aacf056e960a82387b79833ade7efe252dedc25147bed7eca8643`  
		Last Modified: Fri, 22 Sep 2023 01:35:03 GMT  
		Size: 17.7 MB (17716338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2838349a2031c48c1e62e67f65b7e02b5d483d815919134d3007066cd4a54751`  
		Last Modified: Fri, 22 Sep 2023 01:35:02 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1fc90f8e0b1722cbfa6b03d7754c84631b1ea76a09f1f83377187117ff1636`  
		Last Modified: Fri, 22 Sep 2023 01:35:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97ea84ca6fc79c86d472fc032d618dff0dd4b9aab3200da24b899275a419e9c`  
		Last Modified: Fri, 22 Sep 2023 01:35:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c13e13773ee98f373935ba45bf108eea2dd0268e9db40ea8ab7c9211ec8e8c`  
		Last Modified: Fri, 22 Sep 2023 01:35:03 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2ad2dd1907d485a0e8e7f597745900d9c9edfb116f6ec89135f45d39104fc1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.3 KB (757306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7415d4508589f7ab3895bc1cafd8d79ed011625e84a36fe419f5b0f316745c29`

```dockerfile
```

-	Layers:
	-	`sha256:a6fdb2b5486746146463058e2f25b0caa160b6ecfbe613c23dba0c90e724669b`  
		Last Modified: Fri, 22 Sep 2023 01:35:02 GMT  
		Size: 695.9 KB (695910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206e0d4bbc205dc849cb33cfe5f82684b915901be4c70662117c9d92a8d8c47c`  
		Last Modified: Fri, 22 Sep 2023 01:35:02 GMT  
		Size: 61.4 KB (61396 bytes)  
		MIME: application/vnd.in-toto+json
