## `rabbitmq:3-alpine`

```console
$ docker pull rabbitmq@sha256:13f1d6925638b44bb9c547f65d2aa3c54d3b1c634530cc9004f9215f7f37fed7
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
$ docker pull rabbitmq@sha256:218a435a95a1f94f601d24d8dd579aa13cac35cfa837a35e4bb77c31bbc9b301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626e2dcef36f0f3a99c48c397f87d84d3440b5f4b090e12f14341a8334f33ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 19 Sep 2023 17:44:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 19 Sep 2023 17:44:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 19 Sep 2023 17:44:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d58c5fc6e7bce2c1b6757b8ecf8e3e23964916697c1a41849ba95e0708ccb`  
		Last Modified: Wed, 20 Sep 2023 00:20:03 GMT  
		Size: 40.1 MB (40075638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a411a0d5aeab714a96b15fbb19d9ad5992bb9aa0c60fff24635e151aeb1ceb`  
		Last Modified: Wed, 20 Sep 2023 00:20:01 GMT  
		Size: 7.5 MB (7545707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f901c3f766950c03c9461f5678f7864eb940368edde7135ab3caff473f604`  
		Last Modified: Wed, 20 Sep 2023 00:20:01 GMT  
		Size: 2.3 MB (2297462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf77ff4a4ebd1acbb3ff75b42975205ef56be942a19a7253b4f899d38e3c5aa`  
		Last Modified: Wed, 20 Sep 2023 00:20:02 GMT  
		Size: 17.7 MB (17700891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b855fe5d992285891bcd6fe7c91aeb5e43bddfc49ba4339a45a41f420b0378b9`  
		Last Modified: Wed, 20 Sep 2023 00:20:02 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8797e080a72b62c2438b0d4894add9aa34c744194a408bbecbccce7d410be3a0`  
		Last Modified: Wed, 20 Sep 2023 00:20:03 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6290719de3e7bfe6e9663a8f4684f759da5452bf2289b3bb62fab524b4785919`  
		Last Modified: Wed, 20 Sep 2023 00:20:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc6fee3a8d6203ed0e4567f7ea4b5bedba1207490bba924a78e9ace626d9b54`  
		Last Modified: Wed, 20 Sep 2023 00:20:04 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f955ad1ec45dfd3790a143c00fdd86ca7625ecbd28baa001dc210971edd09cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.1 KB (763070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af53fa7f492668118eee1d971a84d1d8476288d457307bf0c01329e4898da8f`

```dockerfile
```

-	Layers:
	-	`sha256:46b203e37e4cd444247b9698580442b237592c50002c5ebf1ae3d8f15c697b89`  
		Last Modified: Wed, 20 Sep 2023 00:20:01 GMT  
		Size: 701.5 KB (701508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e734a3c3808eb84cbfdea7f8d6fb3f2b90842c36a9bc43ecebf5099af3bce1`  
		Last Modified: Wed, 20 Sep 2023 00:20:01 GMT  
		Size: 61.6 KB (61562 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:43dec371736b17f07fb8873a8d4246a124e7a783b65a816e90e7a6c11dab7b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61024742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c7cc61da3a2a0801ec03779e8bad4c2a1e119f9dcb6d280f922824e59c91e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 19 Sep 2023 17:44:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 19 Sep 2023 17:44:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 19 Sep 2023 17:44:09 GMT
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
	-	`sha256:9d39c2857a3a5cb83da8059da54988182558e4648ef3a394b79b86cae90d6272`  
		Last Modified: Wed, 20 Sep 2023 03:25:44 GMT  
		Size: 17.7 MB (17700799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb9917d5e7d8b9ec80be0d7a6e8ddd153d812da40ce796f41ca6984a5f2de38`  
		Last Modified: Wed, 20 Sep 2023 03:25:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1ba75188e6b129975e482fab9c7096e394b284532870e5b4681836f52b8383`  
		Last Modified: Wed, 20 Sep 2023 03:25:42 GMT  
		Size: 109.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adf068bd3b9b3688bab042b93c65859eff48d67a8460fcfe1d24d56f6fcdae`  
		Last Modified: Wed, 20 Sep 2023 03:25:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5137f5738e716a8fd5fe61981c7c3643d1e9e10e66dcc2f2f922ed4d4de`  
		Last Modified: Wed, 20 Sep 2023 03:25:42 GMT  
		Size: 831.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:3-alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:bc8ec046b3a4a05d0cc786e209e5324efd514e19b0f2e90c41fd66e3b0421b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60248258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce532895271a9e210be4aa3b7fcf26f2be92c31b345a830d79014560c71b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Thu, 07 Sep 2023 23:42:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 07 Sep 2023 23:42:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 07 Sep 2023 23:42:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 23:42:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 07 Sep 2023 23:42:57 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 07 Sep 2023 23:42:57 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 23:42:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 07 Sep 2023 23:42:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e2984ce9ac058e6d7122cb3dff7d1a4096b12154d9ef49f5f6f61c8effddb`  
		Last Modified: Fri, 08 Sep 2023 19:58:56 GMT  
		Size: 32.3 MB (32267806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bacd49a0f53986543faf56792c5e5801cb524cba85182bfb4aae53ee7ef7aaf`  
		Last Modified: Fri, 08 Sep 2023 19:58:55 GMT  
		Size: 6.1 MB (6078147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0def42fee5bb893bfe95bc98ecda64a9dac509134dc22b16a712d31f75c1687`  
		Last Modified: Fri, 08 Sep 2023 19:58:55 GMT  
		Size: 1.3 MB (1300432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822eee5002f3d6447da9b22c60c54e8f8817a70486b62b7928b13370cf528e73`  
		Last Modified: Fri, 08 Sep 2023 19:58:56 GMT  
		Size: 17.7 MB (17700648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326098823c0f96231a02578d994bf55309951e1acd6758013ea5498b4673ceda`  
		Last Modified: Fri, 08 Sep 2023 19:58:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366a6146a85ec6216b68d92777c49590ee183d426f9a7b304fde6314ecafc6ae`  
		Last Modified: Fri, 08 Sep 2023 19:58:56 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba8381702a443830c1ab021d60311ded5401a731891cbf52ffece9d90cc8d4b`  
		Last Modified: Fri, 08 Sep 2023 19:58:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a616b94319e38a45eacfba90c37e13464a48dd3b16edb3e0f8e3c24402d55724`  
		Last Modified: Fri, 08 Sep 2023 19:58:57 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6330c993e00166ef5361bac02824f0dc70bb316f17af60df1d528ff7191a29ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.2 KB (759175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a0518e2b3d9d4b52ae7302cbdbc9ca3c15ea1a7088199ec6c5d3ad1df4898a`

```dockerfile
```

-	Layers:
	-	`sha256:f0748d78fb33516147b35bc81e163e61b4991f07c87bc2815f14d8f021daeff3`  
		Last Modified: Fri, 08 Sep 2023 19:58:55 GMT  
		Size: 697.4 KB (697426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d093847d686157ef5f3dbb3a7e403249722593e7b7f8a85b396c9d8014c1d7`  
		Last Modified: Fri, 08 Sep 2023 19:58:55 GMT  
		Size: 61.7 KB (61749 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:dd6245c5be469397ed5bf54ed687d3694f05576ced01c04cb7e27a011ef8ce59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68410215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b35d3d5609e2306726aca525e03652912f1c1ce95b317d52fedae581a54ebaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Thu, 07 Sep 2023 23:42:57 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Thu, 07 Sep 2023 23:42:57 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Thu, 07 Sep 2023 23:42:57 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 23:42:57 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 07 Sep 2023 23:42:57 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 07 Sep 2023 23:42:57 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 23:42:57 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 07 Sep 2023 23:42:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2a808869b034b95cc0a0d3b69316eea32a6991dbcac77f8314c07c9c5ec19`  
		Last Modified: Fri, 08 Sep 2023 20:00:15 GMT  
		Size: 37.9 MB (37874018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1a531d1fdb00741e1a8ea8eb99e36ff2087177fb5922a2a2a02c087bfbeb7b`  
		Last Modified: Fri, 08 Sep 2023 20:00:13 GMT  
		Size: 7.1 MB (7134005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5575b6d4e13c058fb9c67c80d2aeee17e4f008d7e4659c55c8e4fc965d5f14`  
		Last Modified: Fri, 08 Sep 2023 20:00:12 GMT  
		Size: 2.4 MB (2368794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832a088f2e9e1c109f86ed4c3dd9220eebe795bd212beb33c23a90aff68c91b2`  
		Last Modified: Fri, 08 Sep 2023 20:00:13 GMT  
		Size: 17.7 MB (17700887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4796fc747dc8fa104ce1e76dc465342e2c398e0fac9625b7426b8d6818c69`  
		Last Modified: Fri, 08 Sep 2023 20:00:13 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1343d29e49ae74113e1010dea89ab17c026b71bc6103bc88a2229990ed926449`  
		Last Modified: Fri, 08 Sep 2023 20:00:14 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac1cb8178fe6902fc3fd8c3790b65d471fd4e5e9716579b9a317b88214875d`  
		Last Modified: Fri, 08 Sep 2023 20:00:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35d6d60d41e86f806f02db76ddc63910f16a2f0ba3dc6c5c23c2ad8b943f75`  
		Last Modified: Fri, 08 Sep 2023 20:00:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:67b88938b300a68552f615e79c08b35d17814154f599bfc9e78f0fbc22206e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.1 KB (763102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d0ce76265910ddae5df2967dc796de5dd737f195be8db8e4eb7cd7a287d585`

```dockerfile
```

-	Layers:
	-	`sha256:802581a8ba1fd626d62919ac0c801f36b6daa6010990c8e466f67b17d45c10c2`  
		Last Modified: Fri, 08 Sep 2023 20:00:12 GMT  
		Size: 701.5 KB (701530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf5fb5592af449e1e49411a9efba896090b7db82ee7cb1141908d9363feab0ff`  
		Last Modified: Fri, 08 Sep 2023 20:00:12 GMT  
		Size: 61.6 KB (61572 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:247ddb0407ef38778304a6f27bdf1b2403e531fe4e959d23311bf6fc1618485e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62399989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17210b164b119f1bea41c681ba2dc3c48f190a5822e8bd449c95301ef1c5db6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 19 Sep 2023 17:44:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 19 Sep 2023 17:44:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 19 Sep 2023 17:44:09 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400e8c7465b337e20adfbb9a061f92dab69f494bc9ad9b31a062fa059b70d42`  
		Last Modified: Wed, 20 Sep 2023 00:19:59 GMT  
		Size: 32.6 MB (32623545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04ecaf87856a6785cffca94d7a45feb013641ffefa5bea69f90e45b6a999b15`  
		Last Modified: Wed, 20 Sep 2023 00:19:58 GMT  
		Size: 7.4 MB (7437012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fa1f8deb1d63fd9a9248749dba056760093fa49adc9f133782bf20fac8df9f`  
		Last Modified: Wed, 20 Sep 2023 00:19:58 GMT  
		Size: 1.4 MB (1401869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d8d98334e67d141de14744e9361a8eb55ffd20e85e3593a93fe1a7266a101`  
		Last Modified: Wed, 20 Sep 2023 00:19:59 GMT  
		Size: 17.7 MB (17700670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7a9f82b36640f3ecc845510b8ed1a5d3f95ffeb30679525d77228a44c3329`  
		Last Modified: Wed, 20 Sep 2023 00:19:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6039ff0c3abfdb05b3762c1b333001bfb6282bfbebb688ec114c538d5eb791e`  
		Last Modified: Wed, 20 Sep 2023 00:19:59 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe03b836d4b39df7f588f391a46dd6b222ecdbcc6c761df1fbc91ad67eb1e01`  
		Last Modified: Wed, 20 Sep 2023 00:19:59 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce52a8655bd52d94a07c722ede16f5de3c7d0acfc881ea711bfcb12c1e06d2c2`  
		Last Modified: Wed, 20 Sep 2023 00:20:00 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4eb695594e08bf5a0cc914c4b928847158796b9f3a6f02833c0997f62b16782f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54efa4a1233a146d32f19f1605dc3f19793a3b36b4d14e2cfe966d12a8e94ba`

```dockerfile
```

-	Layers:
	-	`sha256:e091daaa26ca470f6968ebf84ea06e42a2c3845d8a13b4ec09b85aa623c84b4a`  
		Last Modified: Wed, 20 Sep 2023 00:19:57 GMT  
		Size: 61.3 KB (61290 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:20517e5848a815f18ef24e6aaf30e4946a4e20f01a2c9f494e9fc60b13bf8756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63328013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3933dabba95e9e34a1b0fc856469f635a7079146f9fc06f7ec127e89d8be1f37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 19 Sep 2023 17:44:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 19 Sep 2023 17:44:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 19 Sep 2023 17:44:09 GMT
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
	-	`sha256:81925cb039eeec16fa7d3c3e0970311ac4af891dc5ffa4209ea2d02f9e7f9810`  
		Last Modified: Wed, 20 Sep 2023 08:44:30 GMT  
		Size: 17.7 MB (17700692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449aebcf829e2a1d40fcca4926298e84626207762cd3296663feae36fad72f4`  
		Last Modified: Wed, 20 Sep 2023 08:44:30 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80208fd6b834692a698f99c1e2009ddb9def9ef49570cc5a3a15ae26561352de`  
		Last Modified: Wed, 20 Sep 2023 08:44:31 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ffffc6372594fd0cd6aa36e1deacca371b79ae269f2c62df3c8f15bd7efe51`  
		Last Modified: Wed, 20 Sep 2023 08:44:31 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeef0dab71b1ccfadf3d89b6f9e94d331e48bd73c51719974a1d64b6693adf0`  
		Last Modified: Wed, 20 Sep 2023 08:44:32 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:547571248fcb5652ca4550567ebfed75464269d4005c9b2d023718f3157f5e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.6 KB (757595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d087f8c42066ad4d5375826caf858d5dc00ad21864444c33c9c5cc6981b1a4c2`

```dockerfile
```

-	Layers:
	-	`sha256:c046017eaeaa7e30a05ffa8dbb261ace6de56ce7ad6a72819f100d9f59ba197e`  
		Last Modified: Wed, 20 Sep 2023 08:44:29 GMT  
		Size: 696.0 KB (695977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accb0bb89a594dfebbd55878ac03cda1f2b0b19dbb71172239da1602c9f47166`  
		Last Modified: Wed, 20 Sep 2023 08:44:29 GMT  
		Size: 61.6 KB (61618 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:3-alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:cc48596b18b628cfff67f444ecfd2ae7197f73338c4ee6cd7ab45967e170c3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61317986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e0513426d6ece92d200572de7f3fb4afeb40703ed2fbefebcc61e941e349d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 19 Sep 2023 17:44:09 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 19 Sep 2023 17:44:09 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 19 Sep 2023 17:44:09 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 17:44:09 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 19 Sep 2023 17:44:09 GMT
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
	-	`sha256:fc5824a940948170888b1275d003abb9d2a11ff2d5f82a8eba96cf5343a1eb6d`  
		Last Modified: Wed, 20 Sep 2023 02:50:25 GMT  
		Size: 17.7 MB (17700680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8982ed10a46991a25fe046c43d22a35621a3b741ea36da2b422f21a2b068b5`  
		Last Modified: Wed, 20 Sep 2023 02:50:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706a9b609da62c81ca7f2ea4c9ffc5d820466d1b80085ecde5e5dd8ffa92a1a0`  
		Last Modified: Wed, 20 Sep 2023 02:50:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bae7a4beea770aa5aaad6515a1ca0e15a322072bc6410fb2c95c22fce55fdce`  
		Last Modified: Wed, 20 Sep 2023 02:50:26 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c7b4add3ee16f9c484503bbc1502928feece1463e5555d78d3fee9ffd08792`  
		Last Modified: Wed, 20 Sep 2023 02:50:26 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:3-alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:3c803d60f29e0541a0e3507829c012e6828a1e322ad5593c742a690a39c0bc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.5 KB (757472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22623b771d764a54ebbcb0d044a5496589932394c3ce2436788a59107811034a`

```dockerfile
```

-	Layers:
	-	`sha256:c2cc692a4d64ae1f39f49626ea13c4582d12bc7bd2928e4f923e6db75a895c47`  
		Last Modified: Wed, 20 Sep 2023 02:50:24 GMT  
		Size: 695.9 KB (695910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83717a022e7b86ee3c734d406335039d88460e8f8fe6284e2c026c85c5603d49`  
		Last Modified: Wed, 20 Sep 2023 02:50:24 GMT  
		Size: 61.6 KB (61562 bytes)  
		MIME: application/vnd.in-toto+json
