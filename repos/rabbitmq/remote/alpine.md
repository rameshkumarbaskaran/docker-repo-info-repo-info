## `rabbitmq:alpine`

```console
$ docker pull rabbitmq@sha256:8db41fcec066c37c8ce0d21b48d5373f948586362e0a9159f0c36665b45eafb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
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

### `rabbitmq:alpine` - linux; amd64

```console
$ docker pull rabbitmq@sha256:0ef4a5074ae490fbd34e5e2be4365618f784e3db41ea7567bb2e2a975b1d993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71003173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad9acd977771eede62ee26745cb7cab2d5fb1275694f5ab233d66dcefba6068`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:25:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 09 Dec 2023 15:25:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 09 Dec 2023 15:25:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 09 Dec 2023 15:25:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_VERSION=3.12.10
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 09 Dec 2023 15:25:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:25:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 09 Dec 2023 15:25:14 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 09 Dec 2023 15:25:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 15:25:14 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:25:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 09 Dec 2023 15:25:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c6bd9f2f476ac8ca381111358834f1eda42d20a7b66fc92fb6ffcf16741a44`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 39.9 MB (39898182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d788cbab00d72d13b60a6ba065354c10d164774c1c8f6ac0b497eb0b4a2a7f`  
		Last Modified: Tue, 12 Dec 2023 20:56:17 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e3f3c4daae27dca3e24dd1187d1bf866da5669f418010b023acbd45b827f7f`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 7.6 MB (7554025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fdf6d9b3ad47c899f1a3f52d68a08a9001ba37dadcb5916db647891db96817`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb011bdfe98916d78ec812fa2f3471332ca9bf4850dfbde8ee3b56b708e5e4d`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 2.4 MB (2407695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d217240abed832febda1c576f1ccbc55af5c1a5dcd2787af1e8c7bcc6b59930`  
		Last Modified: Tue, 12 Dec 2023 20:56:19 GMT  
		Size: 17.7 MB (17732264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1d576cf15e654dfb707e3f0134c9675791a87771796f49b60277fcaef9c89e`  
		Last Modified: Tue, 12 Dec 2023 20:56:19 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf1653df82cd6166cd804aee895e11075e4820606f286b9a1143598a25ed360`  
		Last Modified: Tue, 12 Dec 2023 20:56:19 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23fdb4d0a8eb6da1798d392989ea3bfaafbc85e8f29fed272db727337c1d330`  
		Last Modified: Tue, 12 Dec 2023 20:56:20 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa26e965cc6fba14785af94f4e90c740664e94800f949a05fd95952e8c73f45`  
		Last Modified: Tue, 12 Dec 2023 20:56:20 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e8f6a879bd11a99e706754fc84a9fb6f77f308103fa3928908545af7fdaca15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e88fac3a2f4f35238caea5d83bceda1be96203239ad36f0210724229a2a9c0`

```dockerfile
```

-	Layers:
	-	`sha256:45303b55287ff6a7859c3216626a35e0f67ab48a8081f1cdf0217372a653869c`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 760.7 KB (760731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b870e1fd23c76b621241628c167a5140eabad57c00edc9d4b95c2135dc1c19c6`  
		Last Modified: Tue, 12 Dec 2023 20:56:17 GMT  
		Size: 2.3 MB (2296534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f309b51064305faeb191cb9d3c2f7ff139ca0b2907687497c83c7910dab0a30`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 2.3 MB (2295644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63466cbf7d1dc72d06b7d1b2950532d0a72d2d3b5e0958a5c21d6e33e1bf164`  
		Last Modified: Tue, 12 Dec 2023 20:56:18 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v6

```console
$ docker pull rabbitmq@sha256:925ff96e40bdfc64e878da51d3b5ba9ce0f492069f73517c63230b25928ba9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61114109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e23c8154330ba253b3bb84fac0fc226a8e2a1d61b43fe4f5eda6cacb6b307c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:25:14 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Sat, 09 Dec 2023 15:25:14 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Sat, 09 Dec 2023 15:25:14 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Sat, 09 Dec 2023 15:25:14 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_VERSION=3.12.10
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Sat, 09 Dec 2023 15:25:14 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Sat, 09 Dec 2023 15:25:14 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:25:14 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.19"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENV HOME=/var/lib/rabbitmq
# Sat, 09 Dec 2023 15:25:14 GMT
VOLUME [/var/lib/rabbitmq]
# Sat, 09 Dec 2023 15:25:14 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 15:25:14 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 15:25:14 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Sat, 09 Dec 2023 15:25:14 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f150da36f6f625d41b8fd26d929990bd7bfd608b2a60c1f32137e63fa0a85f`  
		Last Modified: Wed, 13 Dec 2023 00:10:33 GMT  
		Size: 32.4 MB (32426806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2dec8adf19611e8329250ff0fe76f5b78a753f12e2dbd411c033d3e875b7c1`  
		Last Modified: Wed, 13 Dec 2023 00:10:32 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c87e745935637777a0bc3844e082e2510dde383d5a7e337b2673e9ae302f4`  
		Last Modified: Wed, 13 Dec 2023 00:10:32 GMT  
		Size: 6.4 MB (6384103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6c5597f69cf12305f4d149b2174d1bff4c9dbbd5d8c2f1bdb6c362a30fcba3`  
		Last Modified: Wed, 13 Dec 2023 00:10:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5cc845affc7b41592001efac993b102d09d127e59b54f2a6d11f748eeadc28`  
		Last Modified: Wed, 13 Dec 2023 00:10:33 GMT  
		Size: 1.4 MB (1403285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cfd8ab1746f4e68f469cff61c9c47169ea6f4476d72a5beb4ed99cc9b30461`  
		Last Modified: Wed, 13 Dec 2023 00:10:34 GMT  
		Size: 17.7 MB (17732235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de0695c541b2934c38c06a487e061dcf1b9a2ffa79a3f5ed63d8d174500391`  
		Last Modified: Wed, 13 Dec 2023 00:10:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbbe23ea092fecf38d5cfb1691597cc5df798745ca3666626f305743e5b017`  
		Last Modified: Wed, 13 Dec 2023 00:10:34 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfdc3bae8d76367a954b7dd4a3fd97265351f534db12a74994b4bbec4905f0e`  
		Last Modified: Wed, 13 Dec 2023 00:10:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf75266cf5f1ba68b3306754989673a371829458c9bb17f324c0421aab60b12c`  
		Last Modified: Wed, 13 Dec 2023 00:10:35 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:99dcda433ef2970bf15cf44c1ec872507bdf6db23ba2b93fe18d84fb58bd07e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 KB (69275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6b6edb6b1eb8883e5b176b88039d3713c2b0fdfa37ef4e4e8589e6ed9af3bc`

```dockerfile
```

-	Layers:
	-	`sha256:f05ac1e36425c4d9b57ebf0a2c030cf50cf962cdfa3f4b604f7c8002538e0a8c`  
		Last Modified: Wed, 13 Dec 2023 00:10:32 GMT  
		Size: 69.3 KB (69275 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:ddebe8e861f7b9376653f0bf9b8b339a8ff10509133b107cb6613c77daf384fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6e0cdfbf7ce06ac6028958e2ff61ccd6ace7bc566affab1db77c7d6aa49fab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Nov 2023 06:55:25 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331debf178bfa2d4de78fcbc3e75e0ffecbba6fad807fddebfbed0931db9f61`  
		Last Modified: Fri, 01 Dec 2023 11:50:05 GMT  
		Size: 32.3 MB (32270999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbde64275927b4b941cb79d9e66909812ff604cb9857b38b59583b93b0ea9c83`  
		Last Modified: Fri, 01 Dec 2023 11:50:05 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4264acb750412f4cae5cd5c69b25919f7d6f221fdafeab9c5e3a2f1be6050ce`  
		Last Modified: Fri, 01 Dec 2023 11:50:05 GMT  
		Size: 6.1 MB (6082539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f10cd2b59f4a2ad7ccec0893c166c325f6e887e5c7831cd8c6b7fc306ed9491`  
		Last Modified: Fri, 01 Dec 2023 11:50:04 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732717bdbd37b15116e6349db1c61bd31b3e75e9f666b39acec1cd15fb0133c6`  
		Last Modified: Fri, 01 Dec 2023 11:50:06 GMT  
		Size: 1.3 MB (1300457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97f3fbd7f024164dea8ed6511caae6846bee0abf659a813d788bc7f9fd56f5`  
		Last Modified: Fri, 01 Dec 2023 11:50:07 GMT  
		Size: 17.7 MB (17732075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e6729e55dfd5eb87ca1dad65e2cd42a31425df99b0b5c68fe2925bcfc40639`  
		Last Modified: Fri, 01 Dec 2023 11:50:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5f257587a4bacd357f72862ba1ea327651c12aef25e47d622fe73691e673d5`  
		Last Modified: Fri, 01 Dec 2023 11:50:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa1b8086f23d648f4c4febf56233efdfe67536bbf74c3e6bb7bb6ddd897e0df`  
		Last Modified: Fri, 01 Dec 2023 11:50:08 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca38902fa00d404956098062494c03db0c2175108c991e66b9b6748fa54eae3`  
		Last Modified: Fri, 01 Dec 2023 11:50:08 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1cf7cd49e81788ff8b0ddaf3f54fb82e6179fc07c9639ceac12df30d9c092f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d992e7bcbb70b8de29032c8e68f2b4305ca2bd6b91b1c0c90ac3f63ccb7e67f`

```dockerfile
```

-	Layers:
	-	`sha256:2173d31b159a9e480d6f9147916f249a0a3d569e9e5b44f31bb2366d6e5185d1`  
		Last Modified: Fri, 01 Dec 2023 11:50:04 GMT  
		Size: 756.3 KB (756329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0182d3e66ca4c086eed1df77daddcfdc037a62f43958cd895922860aba4fe1ed`  
		Last Modified: Fri, 01 Dec 2023 11:50:05 GMT  
		Size: 2.2 MB (2201692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b039bba141a16aabbb29e48f6e2ba17790480763d6daf7d88fe2fbc8f9e4297`  
		Last Modified: Fri, 01 Dec 2023 11:50:05 GMT  
		Size: 2.2 MB (2200802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b743ffd802d4a29e615db612ca17a804f782ac30e5dfc4ad60abfee09080d0`  
		Last Modified: Fri, 01 Dec 2023 11:50:04 GMT  
		Size: 69.5 KB (69490 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:050bcf6d5a19bc70baef89d180d8af756b30c4cfc6d9d2dbf91a686a16054b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68457926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5f195dcacd8b0d0f0ebd900598a2ca829c89d5bbb817a96837ff88881dbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Nov 2023 06:55:25 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3106a027651f6a6fa5e7ec19b7a262fe4d5e63e0d29d5c8acb8198f1daf2fab`  
		Last Modified: Fri, 01 Dec 2023 14:15:14 GMT  
		Size: 37.9 MB (37873889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db8eb8baa15fd3bc01714a6a8d8c3a8979f6c522c2e73006ad3b5ae937b66ef`  
		Last Modified: Fri, 01 Dec 2023 14:15:12 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a05223def9bb4c8ebce68625bfd4290604316346eae5c744e7f35fe969884ef`  
		Last Modified: Fri, 01 Dec 2023 14:15:12 GMT  
		Size: 7.1 MB (7147432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0379fbbfb7dee8d1ebe12469cb99947b72bbb680d5e2912a5bbfac7676a3b04`  
		Last Modified: Fri, 01 Dec 2023 14:15:12 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f04c97d73c765550604181461b1db82e444edd0fdf4a3fd599fed5bce4d1bc2`  
		Last Modified: Fri, 01 Dec 2023 14:15:13 GMT  
		Size: 2.4 MB (2368800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768883aa80614831f97b1e0017a78f070e117e59611ed379b33e72be1c6eaa6d`  
		Last Modified: Fri, 01 Dec 2023 14:15:14 GMT  
		Size: 17.7 MB (17732234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4538dbc6bb198cea08f07de6460bc6cc4a95e15b312222d057db9e77cbd51f9`  
		Last Modified: Fri, 01 Dec 2023 14:15:14 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe97c8066382cb38e339378ccde742a2a04923904f8444325a14a6610a4c980b`  
		Last Modified: Fri, 01 Dec 2023 14:15:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be86aa3ec736dbadcfd612c491ba1c2efb591547c3a7785de16068ee113f2156`  
		Last Modified: Fri, 01 Dec 2023 14:15:15 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322eae68d677a43ce4feb091230977b3f1f8d63c0557157ca12005dfbef1e0b`  
		Last Modified: Fri, 01 Dec 2023 14:15:15 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:96d1c120739069b3ab6489d53b7c9392a869a0831cd39b50f90a544ba40778a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1581edde38d82dd5caa72bcd1675190525b18a07d270e18672d7d2ba80b80c65`

```dockerfile
```

-	Layers:
	-	`sha256:4de5ab07db329196ce55502e42fcafb6578c643db5fd95e6aa94b41da8fe1737`  
		Last Modified: Fri, 01 Dec 2023 14:15:12 GMT  
		Size: 760.4 KB (760368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0b8cb1ef171bb961f6abe2bd2c2e27975fa1a55f46bf388a8aed248b340261`  
		Last Modified: Fri, 01 Dec 2023 14:15:13 GMT  
		Size: 2.3 MB (2296114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a8264b10d891a3afb3561597e2221cc942d59b5ec0519845537bf548c2eea5`  
		Last Modified: Fri, 01 Dec 2023 14:15:13 GMT  
		Size: 2.3 MB (2295224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3aab00d44099291154d672a0b0ad20e9923c7b868a9b7b2ac2b07cb7974cf9`  
		Last Modified: Fri, 01 Dec 2023 14:15:12 GMT  
		Size: 69.3 KB (69286 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; 386

```console
$ docker pull rabbitmq@sha256:4c3f610f79a094748981d5dd6f3a1acae00923b064cb47f16683383e10e365ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62439481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d624f09c9fcc2b912bb2a420234e7cb1e144dd161dd24a97df84b607d49c5a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Tue, 31 Oct 2023 17:27:40 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_VERSION=3.12.8
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 31 Oct 2023 17:27:40 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 17:27:40 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.8","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.8?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENV HOME=/var/lib/rabbitmq
# Tue, 31 Oct 2023 17:27:40 GMT
VOLUME [/var/lib/rabbitmq]
# Tue, 31 Oct 2023 17:27:40 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 31 Oct 2023 17:27:40 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Oct 2023 17:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Oct 2023 17:27:40 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Tue, 31 Oct 2023 17:27:40 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7084bb4371909a4112132e957798d4b5e7b50751077d645e59cd3604215428d2`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 32.6 MB (32624623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc02584d5330d01f3c7b0339d95c22295337150e12f43414aac19939a818970`  
		Last Modified: Wed, 01 Nov 2023 00:08:54 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26efdf331dbe9ea75e002721b8d804e79e40472c57b073a422f626b66d803e06`  
		Last Modified: Wed, 01 Nov 2023 00:08:55 GMT  
		Size: 7.4 MB (7445765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f283ef0c9903e04c158f080244f27a16e718c75e46ecb2bca266f1d959cbc`  
		Last Modified: Wed, 01 Nov 2023 00:08:54 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881f1f4cc75515fc575c3ceb089acc544fc52d98e4a8f8a55ea230ef30f95342`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 1.4 MB (1401887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd41d86339012cc649dd94138a2d35fb741e45f0e9221c50a2256b939c52426`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 17.7 MB (17728923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb867b3c114cf41c2f851556efb691b881687e838c3439ec1620e3c9fda0c4d6`  
		Last Modified: Wed, 01 Nov 2023 00:08:56 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ad88ac80f833d6d54b077df19944255557c71944bff93520129310b5306e5d`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e29799fc2d6f3831bf629ad3a67bdf208589d60e9c51490c5303aee3552ee66`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90f15fca4ec148efcff160597b9826ac8803fa5519930724b93aa08e95f48b4`  
		Last Modified: Wed, 01 Nov 2023 00:08:57 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:93aca3e41147cd53b8799d9560d7841a74e7c3ac028db80c58acd2e59f4cad4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 KB (68999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bb69509fe5c75b80aadde7174872ab1e4d229026d6c9ce297537d6f266c29a`

```dockerfile
```

-	Layers:
	-	`sha256:43d003fcb5a04cfeb673e9901edd25026438627dcaa4b5123b35f0908acfd27b`  
		Last Modified: Wed, 01 Nov 2023 00:08:54 GMT  
		Size: 69.0 KB (68999 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:0355b6b644d945ecda4186be25eb98a6a3534756fb9f69382a3e29d4f4a97f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63370914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7820636c9de7264a85ab2319c6d47a42d6205ea89c16403f22fc2062325d0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Nov 2023 06:55:25 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ea86dc9ee9484329236e6179d4f0886c13018e58159d2f0163587232b59082`  
		Last Modified: Fri, 01 Dec 2023 12:57:02 GMT  
		Size: 32.8 MB (32804838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ce98db808cb9e7402b0969a004eb9b52ffb9dd828cfd237fd248297169f75`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdcbe39669caff36f3bdb6ecba74275489e800e7c0c5f737fc1c43e4f64b659`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 8.0 MB (7960950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7982c09dbce749126b4854d9e9714fe3e9e30710f5f4248ab3eeec80045f2442`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79989656c5b5ece6ebc0939015a34e3532bf686405e6fcfd9dbddee0c5e61fc9`  
		Last Modified: Fri, 01 Dec 2023 12:57:02 GMT  
		Size: 1.5 MB (1522235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8d6df9e7c7a5eaac6cf08bb0406a96b8748b568115483860566aadad92e508`  
		Last Modified: Fri, 01 Dec 2023 12:57:03 GMT  
		Size: 17.7 MB (17732034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74afb1367e26d179806e84a59ccb803b684c8a9785f79a349760d207b9f1f49a`  
		Last Modified: Fri, 01 Dec 2023 12:57:03 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefbd6ebf4f0d8b1ba66fb8353aaca1d873d6aa576c92adac18af8bf24a1f614`  
		Last Modified: Fri, 01 Dec 2023 12:57:04 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed845f7162a01296e8bbcea675bd9ef2f784d320c7c28bb0157a00a5143950a`  
		Last Modified: Fri, 01 Dec 2023 12:57:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32c307964e2fb29a11c6a03934f5b0caa52ffa03f848a9d00b96119bbef52dd`  
		Last Modified: Fri, 01 Dec 2023 12:57:04 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:31da0e9697dac5560b075e558370d6c01b49dee6a7cf0e23477219a7112588ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aa98bfca5ac0e880c19290c8dea1ace71ca31cff661ebc5cbbb635d9b78e50`

```dockerfile
```

-	Layers:
	-	`sha256:c0c63d90b2b0083ba4ca1c327d3289745cdccccc348496a1a01a4824cbcebd7d`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 754.7 KB (754691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c4842decbffb749d27643a91c8afdf085829e0ac5951e32119b2c5fb29c22c9`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 2.3 MB (2274163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:678462fb2d173335c70c771c8ef3802326cb6e0e59ff8a3d3743b3d9f69f9bee`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 2.3 MB (2273273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9846129d711087bb7957f83d7c0a5f0118ab68d66173079c8698ed113db2301b`  
		Last Modified: Fri, 01 Dec 2023 12:57:01 GMT  
		Size: 69.3 KB (69337 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:alpine` - linux; s390x

```console
$ docker pull rabbitmq@sha256:a175ad7f0beed9cb5ed97b9e23fb542612b9b75a8060a4e7020bbb84962b94be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703dce6f9ffeddd863c0212d1b649ab7ec3876b80c5f92986541dfee28daaabb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=alpine&os_version=3.18"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive $ERLANG_INSTALL_PATH_PREFIX $OPENSSL_INSTALL_PATH_PREFIX 			| tr ',' '\n' 			| sort -u 			| grep -v '^$\|lib\(crypto\|ssl\)' 			| awk 'system("test -e /usr/local/lib/" $1) == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .otp-run-deps $runDeps; 		sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		addgroup -g 101 -S rabbitmq; 	adduser -u 100 -S -h "$RABBITMQ_DATA_DIR" -G rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie; 		apk add --no-cache 		'su-exec>=0.2' 		bash 		procps 		tzdata # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	mkdir -p /usr/local/src; 		apk add --no-cache --virtual .build-deps 		gnupg 		xz 	; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apk del --no-network .build-deps; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	su-exec rabbitmq rabbitmqctl help; 	su-exec rabbitmq rabbitmqctl list_ciphers; 	su-exec rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie";		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=alpine&os_version=3.18"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json; # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN su-exec rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 22 Nov 2023 06:55:25 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Nov 2023 06:55:25 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaf109ed768228eb29adb4476d0e0db9b9d0f4c6d93d39ce09eb5f3256ed934`  
		Last Modified: Fri, 01 Dec 2023 12:19:41 GMT  
		Size: 32.5 MB (32478984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904fd8c67df3b8dbb95f849d021dfa5102ec9c9fb44c905a891b69a990a918dd`  
		Last Modified: Fri, 01 Dec 2023 12:19:39 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d46330a3ef88498a6f7bb6107fa1c0c267066e67783e312de05eead7e6039`  
		Last Modified: Fri, 01 Dec 2023 12:19:40 GMT  
		Size: 6.4 MB (6432233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4e2bcb16d97ff877e080c1e58a6c86ff6311331d0055d78bc12ceb85f97aa8`  
		Last Modified: Fri, 01 Dec 2023 12:19:40 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecdec0c8a8072e48775defc0c6ed3c333e3b548f673405f4ee03c2f163c10ec`  
		Last Modified: Fri, 01 Dec 2023 12:19:40 GMT  
		Size: 1.5 MB (1495514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23810c50ab671f8ed65b78dc76e6a7b7e327414d4153774565dac587009e5d90`  
		Last Modified: Fri, 01 Dec 2023 12:19:41 GMT  
		Size: 17.7 MB (17732061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4389bc1ba8106e4caae313170962f9b0ad1a90cc017163f378a59b8d965e660`  
		Last Modified: Fri, 01 Dec 2023 12:19:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc3a745d09d4b2e7201e62d8a3e4c3ea4a7e9a182b51fe51a3e0d1179d7d6a`  
		Last Modified: Fri, 01 Dec 2023 12:19:41 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3542bcdefdb3437121d11c816dae2d04534e160001a648fcc7fb86e3eac10`  
		Last Modified: Fri, 01 Dec 2023 12:19:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3cd858d6c36d6d276970964753d680f3f26bc8dcc239fe3a6efb6a0b68756d`  
		Last Modified: Fri, 01 Dec 2023 12:19:42 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:alpine` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7265da72771c45e9075e7d62af48078252fc5012ceb7ab816bbcd5fe197638ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62176e36516563c89149557537f93efbb230914fd827dc7b459a595277aa96c9`

```dockerfile
```

-	Layers:
	-	`sha256:427f2a305921f50b06a85107db678fe659a1f441ac94d2dccdee6846a833a8c4`  
		Last Modified: Fri, 01 Dec 2023 12:19:40 GMT  
		Size: 754.7 KB (754657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b18d17e6752f6d9c8ae5173e07ca0a7b2bc2f54a3a1044574201fe201924ff`  
		Last Modified: Fri, 01 Dec 2023 12:19:40 GMT  
		Size: 2.2 MB (2207143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c302eaf2029f165de4d61bc3ce94340f8587f9c031989148958f6d1edc1c9558`  
		Last Modified: Fri, 01 Dec 2023 12:19:40 GMT  
		Size: 2.2 MB (2206253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d82eb79ef053e04e90ca3cb3aa7a25c3ad0a96b3d8db8f2935fdad68063fce7`  
		Last Modified: Fri, 01 Dec 2023 12:19:39 GMT  
		Size: 69.3 KB (69277 bytes)  
		MIME: application/vnd.in-toto+json
