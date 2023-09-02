## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:c847b92fbea1590e43ef4f8dd51d8f94904f7c78f8315b7597ebd55e8948354a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rabbitmq:latest` - linux; amd64

```console
$ docker pull rabbitmq@sha256:38d5167aa0a88b91a575eb5dc266168e79c258292316648a99eb8328cf809abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105714596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814bc72e3297281c1bfac8fbc1caef9bdf385c75bd959ecc6c08c80a056da798`
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
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 24 Aug 2023 23:29:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 24 Aug 2023 23:29:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:29:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 24 Aug 2023 23:29:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9cea1972f33844108fcd25a8336c5b41f07eef99dd364eaa17eb39fa2505f0`  
		Last Modified: Sat, 02 Sep 2023 00:01:07 GMT  
		Size: 429.1 KB (429116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5dd5e30dc2a2f886b14d45d297fdc59117590d06fc6679094b7d40953a6c3a`  
		Last Modified: Sat, 02 Sep 2023 00:01:06 GMT  
		Size: 10.1 KB (10130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e381aabb23250f02ce8664d0788cd14b5cbb54ed4cc420e736f2a7b21605adb7`  
		Last Modified: Sat, 02 Sep 2023 00:01:10 GMT  
		Size: 55.2 MB (55161081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6f3c07bd1f15ecac3d1e38992e2fa03275d9ccd1bcf98bfd9b93cc35765952`  
		Last Modified: Sat, 02 Sep 2023 00:01:07 GMT  
		Size: 10.8 KB (10822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0246ae3c64860adaef2e80d6359a317f02a0e7f44f7faffecafcc3c8dcc6965e`  
		Last Modified: Sat, 02 Sep 2023 00:01:09 GMT  
		Size: 20.6 MB (20563978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988a4dbb4a417056122ace0bacec0b9cec7a774d0c09ee7ad3771560dff8ad6`  
		Last Modified: Sat, 02 Sep 2023 00:01:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6564b22d1396d19e7624d23fadff6a65f6e6e6a0f95dfa30d76b4636c0beda`  
		Last Modified: Sat, 02 Sep 2023 00:01:08 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8607e6d253d0a2e13218576a0986016bc80ca4659dc7d6d1b5ae354af7e31ccf`  
		Last Modified: Sat, 02 Sep 2023 00:01:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f122ae8dbcbf0ee755befa7a5e9d0581c3143c417437db130d7a6c886dfb96`  
		Last Modified: Sat, 02 Sep 2023 00:01:09 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c68424642b3be6c300c7b1240aab2d3e9a4aa720348dc5263c6508a8372aa3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afbfce743009c3b241c58a33f400edaf61d00893eb461bdcbcf038764e7ec86`

```dockerfile
```

-	Layers:
	-	`sha256:5e4e0c38d36935e243283a761fef00d95f015ba7cbff23e66d430249f69d2a7a`  
		Last Modified: Sat, 02 Sep 2023 00:01:07 GMT  
		Size: 1.9 MB (1853767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7535d2dcec078f07b3788b13a0f99d2906d08c15ea790cf591d5f2a5ecb64255`  
		Last Modified: Sat, 02 Sep 2023 00:01:07 GMT  
		Size: 59.6 KB (59561 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:85459ff6dbced849c92d5fd82c14d6cc6ce41fe3c061312b6f9b1e6b877b3ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90306948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b4a886742b3bbd52800066ce56a568f20f33d64a18bfe6ca6dd9aebc135917`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
# Wed, 07 Jun 2023 11:43:59 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 07 Jun 2023 11:43:59 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
ENV RABBITMQ_VERSION=3.12.0
# Wed, 07 Jun 2023 11:43:59 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 07 Jun 2023 11:43:59 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 07 Jun 2023 11:43:59 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jun 2023 11:43:59 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
ENV HOME=/var/lib/rabbitmq
# Wed, 07 Jun 2023 11:43:59 GMT
VOLUME [/var/lib/rabbitmq]
# Wed, 07 Jun 2023 11:43:59 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 07 Jun 2023 11:43:59 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Jun 2023 11:43:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jun 2023 11:43:59 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Wed, 07 Jun 2023 11:43:59 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:2d97abfcf215d35e8a846b390350fea9f455676b41221360fe8782163a1c46bb`  
		Last Modified: Thu, 15 Jun 2023 03:47:54 GMT  
		Size: 24.6 MB (24589116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea55c791dc3b03c096321b91f121ca2a705c4743ac6977c8821f6911e288a2a3`  
		Last Modified: Fri, 16 Jun 2023 01:07:12 GMT  
		Size: 391.5 KB (391474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211f3f9b240b81388e1d6605657c90108ec1d4c3750761c270f75a06939a333`  
		Last Modified: Fri, 16 Jun 2023 01:07:11 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5efb30d20d0ca9fdd974e99b00dff7096808f99c17a5364c7e4994d1f6d1c86`  
		Last Modified: Fri, 16 Jun 2023 01:07:17 GMT  
		Size: 44.0 MB (43956436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4a430e86c33f44ad81570e09f4932d29d421df268835a8ea9c98ce8f59377`  
		Last Modified: Fri, 16 Jun 2023 01:07:11 GMT  
		Size: 10.9 KB (10909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6513dd9ce3f15eb5e52257a871b0c23f4770acfb72949f3cb5f8036055832334`  
		Last Modified: Fri, 16 Jun 2023 01:07:12 GMT  
		Size: 21.3 MB (21347114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9253ebdbbacb15acd9019018e55f86d1b12df4ee84ddda44b0fd51a84fde2b3`  
		Last Modified: Fri, 16 Jun 2023 01:07:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83df928b43f09213834abc7ea11c3f12d17082b80373c2f2639ce7b2b3f21701`  
		Last Modified: Fri, 16 Jun 2023 01:07:10 GMT  
		Size: 107.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de163b85ffdf251371f1d892d5eb7df0c5739120b3f64615255447e854a88b4`  
		Last Modified: Fri, 16 Jun 2023 01:07:10 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ec308b6b71f90921dbaacb3181f842e5283371c25f5a813c205f3d2d998507`  
		Last Modified: Fri, 16 Jun 2023 01:07:10 GMT  
		Size: 832.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:71c7b86a8ab7667c444591a2029474ce4889bdf959b5ed607bff5a1b24ddb9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100626795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5070370b2ceff844c164c3573c6e330c11e32c63f33ea4651a407f40797a31a`
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
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 24 Aug 2023 23:29:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 24 Aug 2023 23:29:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:29:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 24 Aug 2023 23:29:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51abf30937047a66ff07f22331e2485ceb2cf7864d2a6eff02eb893b045ee136`  
		Last Modified: Sat, 02 Sep 2023 01:22:35 GMT  
		Size: 411.1 KB (411076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97328c93683eeb2c7e73553d8e02f8ffd828baacec4cbbcb47ddf6dcd2f7f2a7`  
		Last Modified: Sat, 02 Sep 2023 01:22:35 GMT  
		Size: 10.1 KB (10148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acbfd8c527ae919a49e2b4e14afbac2f0ee7fe298e5c035fa1f903de0f869ec`  
		Last Modified: Sat, 02 Sep 2023 03:25:29 GMT  
		Size: 52.4 MB (52364863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c76e5e7b8ef8dcc566ae39195b0b7789b9ce2098f85e58b9b8dc19286c798f1`  
		Last Modified: Sat, 02 Sep 2023 03:25:26 GMT  
		Size: 10.8 KB (10809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568ebf0f741b9e884ce1cc98a24dbbe4cd4e406adba487f31981942f14396ee`  
		Last Modified: Sat, 02 Sep 2023 03:25:28 GMT  
		Size: 20.5 MB (20477041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a747c38e6b164330397810f07dd35ed1d44caa65ee8590a1afba16c6f3105562`  
		Last Modified: Sat, 02 Sep 2023 03:25:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745e63cb3268d2c56deb905af8089f7ccb30a6a4979e8ef995e5f0be233d7f5b`  
		Last Modified: Sat, 02 Sep 2023 03:25:27 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f16b23240ef19b952b65b99082fab97e4f0c4b3f9228716a7f2d916bf3a8`  
		Last Modified: Sat, 02 Sep 2023 03:25:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f50f1fb5da62c6442cf577339330cdab8b7ddd539fb3ef29b65617b7dd606`  
		Last Modified: Sat, 02 Sep 2023 03:25:28 GMT  
		Size: 836.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ecb666d1f88ce8c8f5772b97ab80bd6964e80cac3aeac93228e23bf8f0927124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b970278aa99b707ed82e2e8135b96fadc0f2f1fdb00ea3363738e5e81c859e`

```dockerfile
```

-	Layers:
	-	`sha256:c66c3c19accf20c6c4090a8194974322e2a13bdb5fe73bebd08e6a47b49afe59`  
		Last Modified: Sat, 02 Sep 2023 03:25:27 GMT  
		Size: 1.9 MB (1854134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12be343d18ee5b578b66860211e81a121c4a167e4d85a02e55a50411f2848f4`  
		Last Modified: Sat, 02 Sep 2023 03:25:26 GMT  
		Size: 59.4 KB (59410 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:49981c860a01e7cede890903abaa0e92994950534b4b419655c3d8a9e2a3cd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105437346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91f34c7ba66bd3d57948e80b0444afa5af9280e461a7bf4859ad64a937f25c`
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
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 24 Aug 2023 23:29:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 24 Aug 2023 23:29:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:29:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 24 Aug 2023 23:29:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:c76fbfef684586d44d4a79c1a2c093ecf60b0f6c5deb0742082a5152ecd9a1fa`  
		Last Modified: Wed, 16 Aug 2023 06:33:06 GMT  
		Size: 34.6 MB (34567229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04053a66a1d2e0246196168d8537ca10f7e360fc6eab590615361bb593a676c9`  
		Last Modified: Sat, 02 Sep 2023 00:02:51 GMT  
		Size: 463.8 KB (463756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1351ca26cbc67101d9a4b5e81368c1f8fd8f4b412bea47d99d557cc9d85a412`  
		Last Modified: Sat, 02 Sep 2023 00:02:50 GMT  
		Size: 10.2 KB (10152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fce799f32bec2b0d7518c68f0b472b6ab974e5a54b369695558b5f0f67163`  
		Last Modified: Sat, 02 Sep 2023 02:05:03 GMT  
		Size: 49.9 MB (49877695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda3436b8009fcefeb28a294898792d440c1442cbd5d4f9898f827998b1e9098`  
		Last Modified: Sat, 02 Sep 2023 02:05:00 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5adb55bb7f9d29c5197162daba671f468644cee7327a5ab1634325858573f17`  
		Last Modified: Sat, 02 Sep 2023 02:05:02 GMT  
		Size: 20.5 MB (20505993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a026965b81f5c9bbcdb53e3937742c56c0b6c7542865a724ad5e06a7c4c2100e`  
		Last Modified: Sat, 02 Sep 2023 02:05:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef9a3c9607d164f5cc06a82e779def401b7e9c756c183c7e273757a5779cb1`  
		Last Modified: Sat, 02 Sep 2023 02:05:01 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90097a2250a0d671476d6fe210fc75fdda7aade417a452e26dd7581db97c5d1f`  
		Last Modified: Sat, 02 Sep 2023 02:05:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203cb68b3cc44d7e7efe0758a20fe385293a3af6e4e29b4804e59bcb2514eaa8`  
		Last Modified: Sat, 02 Sep 2023 02:05:02 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8918878f972b08f8324540dc606267b6830901bdefceef3aac653dd14ccb8366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1917913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1aaa60db0400cfc622afa69c87272a252dcfe95e3ff13c16aeda5ae28fc023`

```dockerfile
```

-	Layers:
	-	`sha256:f0e3f241e8376cd446ced374804eeb2a25e9601f5e8b35a8c45f6ea08763ce82`  
		Last Modified: Sat, 02 Sep 2023 02:05:00 GMT  
		Size: 1.9 MB (1858459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8550f3e6e80c39a5acb8121f7caaea66584597bbc577ae80014bcbdaf1e80c5b`  
		Last Modified: Sat, 02 Sep 2023 02:05:00 GMT  
		Size: 59.5 KB (59454 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:3c6b03b1d44ee1439716e66423b0ac97195a3adb0b12f67ee4c86aa83bea2de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1025396f9ad94b0c58cb498424e70a59f195b60c02449dceefcba50764d25e6a`
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
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/bin/ /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/etc/ssl/ /usr/local/etc/ssl/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY /usr/local/lib/ /usr/local/lib/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private /usr/local/etc/ssl; 		ldconfig; 	sed -i.ORIG -e '/\.include.*fips/s/.*/.include \/usr\/local\/etc\/ssl\/fipsmodule.cnf/' 	    -e '/# fips =/s/.*/fips = fips_sect/' /usr/local/etc/ssl/openssl.cnf; 	sed -i.ORIG -e '/^activate/s/^/#/' /usr/local/etc/ssl/fipsmodule.cnf; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_VERSION=3.12.4
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 24 Aug 2023 23:29:02 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
ENV PATH=/opt/rabbitmq/sbin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:29:02 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENV HOME=/var/lib/rabbitmq
# Thu, 24 Aug 2023 23:29:02 GMT
VOLUME [/var/lib/rabbitmq]
# Thu, 24 Aug 2023 23:29:02 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 24 Aug 2023 23:29:02 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:29:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:29:02 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Thu, 24 Aug 2023 23:29:02 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:e1b6153f78cbd4f98e7250bc413a393734736138dcb57f1e41f45c3e43c5a120`  
		Last Modified: Wed, 16 Aug 2023 06:33:12 GMT  
		Size: 28.0 MB (28016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462bf599d8f25906e850590437134835128cb4e223d384eef647a89fa90a9bf1`  
		Last Modified: Sat, 02 Sep 2023 00:48:54 GMT  
		Size: 432.4 KB (432416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecd2471c3a0b98e092469d6b1c2d6f21571f2a2e5349048cbb8202466dfb268`  
		Last Modified: Sat, 02 Sep 2023 00:48:54 GMT  
		Size: 10.2 KB (10150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40966040bfe01cf18a6ad15a5975c1b62705ab164aa202bc22a2db1bc1bd77b7`  
		Last Modified: Sat, 02 Sep 2023 01:59:41 GMT  
		Size: 46.6 MB (46580219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3473441412f2733807b3348882205e1013cab3a60c7e97cd011078efb9f6cfb`  
		Last Modified: Sat, 02 Sep 2023 01:59:40 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f40e4bcbc26296c7da992fb9a3e3262c4cf38cdcfa4b108c3273b7c11ed0cf0`  
		Last Modified: Sat, 02 Sep 2023 01:59:41 GMT  
		Size: 20.5 MB (20534487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fcb2390d8396e78b55d2e2d6987e415abd603fb1fe49944eb1b2a1b7091cfa`  
		Last Modified: Sat, 02 Sep 2023 01:59:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d027cfb28c27e7aa61baa59446cab910e70128dedc00634adb23b5c368e5368e`  
		Last Modified: Sat, 02 Sep 2023 01:59:40 GMT  
		Size: 107.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aeb236884421efe86c452f36dcec9ed4d1915b907db62cd00a4162f8a59524`  
		Last Modified: Sat, 02 Sep 2023 01:59:41 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b94b5339f8ac724892b4efc68c82e4061dd59d633ec465928e46168b712ad0`  
		Last Modified: Sat, 02 Sep 2023 01:59:41 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:0c4e43d6d3d3e0c89ebbd240ec2d30373834877578d977ac28a6b8077663b1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1914166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db3665b87d84c58638891e8b3fe911858bb54f9f988c13b56285ff24ab55329`

```dockerfile
```

-	Layers:
	-	`sha256:ec41f5add34dfe6a3f413e00f9f27fd05a6f60d81529465bc836a5c258d22477`  
		Last Modified: Sat, 02 Sep 2023 01:59:40 GMT  
		Size: 1.9 MB (1854766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab3b3310d031e05cee7b167bc978395f094e023ded20bf97c63a49494c37c74`  
		Last Modified: Sat, 02 Sep 2023 01:59:40 GMT  
		Size: 59.4 KB (59400 bytes)  
		MIME: application/vnd.in-toto+json
