## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:8b1d0eaa5023dae9891b8ad3fd3b49a12a452435288abc3fa1292917b80260c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:2990e158d77cee9e0085121d58f2278be10f0cb5630e9ff7816d2e64106b0a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102012743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223d6bb05ddb799db7c04bd10313f54add0d1856d1509b6970d81917b494775c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403ecc47633a8ac6ac1c5f0f530926fec03fd641d467126df30e0cd293baaf57`  
		Last Modified: Wed, 20 Sep 2023 00:20:29 GMT  
		Size: 44.4 MB (44441933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c9598c5d5c5768d84810215c8c172f114492a2cf441e953f04d54344c172f`  
		Last Modified: Wed, 20 Sep 2023 00:20:26 GMT  
		Size: 7.5 MB (7456597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26ba006724c718ad297027ee67390041b8f9c9776af882386fb9e0f648210e9`  
		Last Modified: Wed, 20 Sep 2023 00:20:25 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096a4e78ddcce1a9da32e825293c5516eb517d1e26225de9c605b6bfdaf4319`  
		Last Modified: Wed, 20 Sep 2023 00:20:26 GMT  
		Size: 20.6 MB (20564023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a26b0e85013435e1766cde88240a0a7e37d76155926fd2789995d6173807d0`  
		Last Modified: Wed, 20 Sep 2023 00:20:26 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51493e83087afee8799576101b08a1473d995c4b8b0455a60e10eaff80410126`  
		Last Modified: Wed, 20 Sep 2023 00:20:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2865c0e7e3f6b8df888ac2a4bbcbd65d00225516be7bdcf6a0b6b301ecbfe3`  
		Last Modified: Wed, 20 Sep 2023 00:20:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c483018217d9fc4ba8da9b43c584f84d15776fc06e7243a7f9a24845a56280d4`  
		Last Modified: Wed, 20 Sep 2023 00:20:27 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d8ab5ac52796cdb4ca28d2b05b017820fa5f1aa0f7a3a12ffc6a17eb6e97f630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d83df0292d4c3fdec1de7e26254fda00fbd8114023b0700f36c831365d910a`

```dockerfile
```

-	Layers:
	-	`sha256:202eeea594259559ca3fa719da4b3911f23abde1ac337e2757c7aaef6ad4c230`  
		Last Modified: Wed, 20 Sep 2023 00:20:25 GMT  
		Size: 1.9 MB (1853767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8842dc0d7028d5228e923a7f2cafc2b59bb79768b06ac4807c6c07557240889`  
		Last Modified: Wed, 20 Sep 2023 00:20:25 GMT  
		Size: 61.3 KB (61347 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:fb5604662c2c1681f253fe605106e1a0dcde96891decc7f2244dd644b5e0ccbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85437977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b46b74dd8011be150a0baf0795bfe9bc4aea2b684d5649e5a5b931b0f0bd98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 23:42:57 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:d79cf5fbd02b4f64ddfb1ba3ae0178a904f012bc2ff0e5603ffdb4668a8f529c`  
		Last Modified: Wed, 16 Aug 2023 06:32:59 GMT  
		Size: 26.1 MB (26142545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af3bcd7f02487f6d4e969ce01ad1f84ae6cdad35e2b01142cac1e2271530f34`  
		Last Modified: Fri, 08 Sep 2023 19:54:59 GMT  
		Size: 32.7 MB (32743816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02234538d6b7c3c6cbced8d161d0b2826aaa851e764c4c3bc818d9a7945bd11`  
		Last Modified: Fri, 08 Sep 2023 19:54:57 GMT  
		Size: 6.1 MB (6056717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f1bce024006826bd004b98151028d88c0bb8068e4198830518d6ae1640707a`  
		Last Modified: Fri, 08 Sep 2023 19:54:57 GMT  
		Size: 10.7 KB (10715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd449bbb69a6de2a1f657a158e4f7397bb19ea50302c6c6380bcaafbb1add050`  
		Last Modified: Fri, 08 Sep 2023 19:54:58 GMT  
		Size: 20.5 MB (20482434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204e3373d0e15cfaf2a99f29cfce074dbc92e1069c3eae064d7ba89ebed1637`  
		Last Modified: Fri, 08 Sep 2023 19:54:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e6644120571188c85ff5e2f8442ab126714c7009510caa9607236e7a08f5cd`  
		Last Modified: Fri, 08 Sep 2023 19:54:58 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa016e448e2fde5db1e1cd636303a2ac5efd4a262a9f1ad82fe87db4c733fb1`  
		Last Modified: Fri, 08 Sep 2023 19:54:59 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99397937e257410954e4a5ae93073e89432e3ca43480b45aafe3769679733d86`  
		Last Modified: Fri, 08 Sep 2023 19:54:59 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:782b8f163f881e24b9f0f42145eb83e371e39880ca3dca440e46cccb3de6a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1917305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcc25b24009e357e924479e5f8830c93778a155cd3944aa4f832e9686163c3`

```dockerfile
```

-	Layers:
	-	`sha256:f4ee2775da0c4d9702c31396f4d27d4672657af2b65bab101e2c13060d1341f4`  
		Last Modified: Fri, 08 Sep 2023 19:54:57 GMT  
		Size: 1.9 MB (1855770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f129e83719d8eb09bcaf05b8ccf827f7a84ddb7bffa5651a2a9c6a51c315`  
		Last Modified: Fri, 08 Sep 2023 19:54:56 GMT  
		Size: 61.5 KB (61535 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:8747034645797dbb264d33e5d0933b8691f01e01c15426d027e1d6e04f70c60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97231788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f49cbee247156381b11dfa2a4a64cdc07bfc226ecb82f75cd9326797560ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 07 Sep 2023 23:42:57 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 07 Sep 2023 23:42:57 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 23:42:57 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 07 Sep 2023 23:42:57 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e2a37747f4f97f394f253878f3faa164337e282c0218509ad15d5a9c9e4763`  
		Last Modified: Fri, 08 Sep 2023 19:56:55 GMT  
		Size: 42.3 MB (42277938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cecd22877e78dce9b4dd52bdd61e388e69222a9cb2812ae688706ff9dec2c14`  
		Last Modified: Fri, 08 Sep 2023 19:56:54 GMT  
		Size: 7.1 MB (7113281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc4a5422dd6695f12d578b145527036601d6ee7b1644f00c488b93d2d6ee81d`  
		Last Modified: Fri, 08 Sep 2023 19:56:53 GMT  
		Size: 10.7 KB (10712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58aa0b907c446d3a163796e873e9d0a827cb8ecd241fd064f0614921266a12e`  
		Last Modified: Fri, 08 Sep 2023 19:56:55 GMT  
		Size: 20.5 MB (20477004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a19476a78de310ea5b1eb67b77fe6a6d21a12c0ea1589090772272555069dd5`  
		Last Modified: Fri, 08 Sep 2023 19:56:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759a17239ade1127bb420a2250fce424ed8b8bd86326217a73671259fc58732a`  
		Last Modified: Fri, 08 Sep 2023 19:56:55 GMT  
		Size: 108.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322666c328d258a8f3c407d3fe879be0044d99189e96eb6957f65f3f9c4d8838`  
		Last Modified: Fri, 08 Sep 2023 19:56:56 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e4f3fc38b822936ed4f2bd81dbe34120613e4c1981c52e54d61b4ed3ec8e3`  
		Last Modified: Fri, 08 Sep 2023 19:56:56 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:1774f9ca6f777719ad427740b03155bda3747b3b45712fd269cb4c6419ddabee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9e8f9fa2d8f1c90269195fb416b46bcfdc1f357220f91c7516003157c6a2ec`

```dockerfile
```

-	Layers:
	-	`sha256:3d557ccd0fdc9ebc6bae7534015a1cbb3845cf1af310c42ad469f27c0537264a`  
		Last Modified: Fri, 08 Sep 2023 19:56:54 GMT  
		Size: 1.9 MB (1854134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4b11e28d7dd2636381b2303f1d4190af30336a1c347e1dfa031a41063439ad`  
		Last Modified: Fri, 08 Sep 2023 19:56:54 GMT  
		Size: 61.4 KB (61358 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:c444754269da6e66659c4ca0f123946f2fc62e4ba7760c38b2fd32129e18a40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101682184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455032fb7d10b3814e95ecdcce8768b8fbf9e8e6ed4bd169a582fec9b5b1ebe8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:c76fbfef684586d44d4a79c1a2c093ecf60b0f6c5deb0742082a5152ecd9a1fa`  
		Last Modified: Wed, 16 Aug 2023 06:33:06 GMT  
		Size: 34.6 MB (34567229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e332810206840740ae7ec069c427f7f3ea4e133ac678223a356224095961de6d`  
		Last Modified: Wed, 20 Sep 2023 07:36:19 GMT  
		Size: 38.8 MB (38759734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8725c209b9ea6a9d2386db3d196d19b1dc2a1544e27e3fd2114216198e31116`  
		Last Modified: Wed, 20 Sep 2023 07:36:16 GMT  
		Size: 7.8 MB (7836641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44d0f74407ec31acdc88a61088ebb44a854535daa6b5f6c3e4594d34479be0a`  
		Last Modified: Wed, 20 Sep 2023 07:36:15 GMT  
		Size: 10.7 KB (10685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb15c6b71fc323dc122cd5a75ba4c8afd49b7c9bb201fde8877f49f885316403`  
		Last Modified: Wed, 20 Sep 2023 07:36:17 GMT  
		Size: 20.5 MB (20506138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a6c8ac42e90933814e70c8bdb7b562ea2868d88746857dd885b806bce732eb`  
		Last Modified: Wed, 20 Sep 2023 07:36:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a81a2b9dce7a54b2566eddf98288c0f39e7acfe9743ae8c420f059e7ed853be`  
		Last Modified: Wed, 20 Sep 2023 07:36:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4132f413d49fb59e7b16bf30843eeee8803619acd780987c37ab0eca3d6539`  
		Last Modified: Wed, 20 Sep 2023 07:36:18 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c2f194c889309ff69315099426ef8b6b2d7f3e31a46794d256e48c13f25281`  
		Last Modified: Wed, 20 Sep 2023 07:36:18 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:88d3556571017dc1130f59a46549483e5b00cb21b871aabb9a36bd4bad21fe36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1919863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d1a2c00de0ac0ec6105f7d096f0dd7e7547af2fff98324c108ddf645242bb2`

```dockerfile
```

-	Layers:
	-	`sha256:8dbcc8ab3cfb618c7e3d83416319fc019c5eeef63899d2deb45c392934b781f1`  
		Last Modified: Wed, 20 Sep 2023 07:36:16 GMT  
		Size: 1.9 MB (1858459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cd8d22a24699bd3c21987d4a911155636f42facd47dfc588ad5e6dad37b26e`  
		Last Modified: Wed, 20 Sep 2023 07:36:16 GMT  
		Size: 61.4 KB (61404 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:de983c041e3cb86b527be2655ca3933a4147b53bade2ba134c03cdb711a85988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92488923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53d72423cb14f4f61568e5c1d8f70b5b8a6f24b0c2872b43407251ebc0be009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_VERSION=3.12.4
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Tue, 19 Sep 2023 17:44:09 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Tue, 19 Sep 2023 17:44:09 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Sep 2023 17:44:09 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Tue, 19 Sep 2023 17:44:09 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:e1b6153f78cbd4f98e7250bc413a393734736138dcb57f1e41f45c3e43c5a120`  
		Last Modified: Wed, 16 Aug 2023 06:33:12 GMT  
		Size: 28.0 MB (28016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a70d707ad666acd578b4df28a82258ac8e583dea06e7e59765ce35ce753f49`  
		Last Modified: Wed, 20 Sep 2023 02:35:46 GMT  
		Size: 37.4 MB (37420818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8947a2bf160de3bc437f9015fa3b79b25f69959c7e247d467a662dca02d8f1`  
		Last Modified: Wed, 20 Sep 2023 02:35:45 GMT  
		Size: 6.5 MB (6505055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb152f653a4c9af2707e460f8e70c29e319be8d1dad9a16b79f2ed3ab10941`  
		Last Modified: Wed, 20 Sep 2023 02:35:45 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578bee03dad905257a2b7801bbfe49a4542c97117c3e19c800d3521a5c6d1d99`  
		Last Modified: Wed, 20 Sep 2023 02:35:46 GMT  
		Size: 20.5 MB (20534524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf08b96d77e5a484e6ef21e5edb695c6544fd6536de3bb2a45507f015105662f`  
		Last Modified: Wed, 20 Sep 2023 02:35:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c447d52e050f82c299e08fa6f2fdf966dd629e57dfc20e4808398678ffe9f4ab`  
		Last Modified: Wed, 20 Sep 2023 02:35:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f435dffcadb4a8b6e38000ab85ca2ccb149da2c6c04603253646e8f4e7813242`  
		Last Modified: Wed, 20 Sep 2023 02:35:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3d2179ee5332efc956c62d13b4dde30948dccc8f5694d8dad0500bab102f95`  
		Last Modified: Wed, 20 Sep 2023 02:35:47 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:524f47e2eecb8d1fd3855d6c35c5951dab350ded2b1ed6f8825bd1cbd04893e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1916114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe0fcc7014d5cbf2053beeef85a87a3c116b17b04fbca9277069455dd862a93`

```dockerfile
```

-	Layers:
	-	`sha256:2f784d60c24bd03080e1362c9968acc8d31360c39978428ef0a601bbe65248bb`  
		Last Modified: Wed, 20 Sep 2023 02:35:45 GMT  
		Size: 1.9 MB (1854766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d521e24b318020cf6c12e3d681505724992357d00683fdb6c066e6054ce2720`  
		Last Modified: Wed, 20 Sep 2023 02:35:45 GMT  
		Size: 61.3 KB (61348 bytes)  
		MIME: application/vnd.in-toto+json
