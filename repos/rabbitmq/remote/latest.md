## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:0ce037ee7ad79a081b6c0310b09297e0822dbaf86c15c60f7584e6139be2ad55
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
$ docker pull rabbitmq@sha256:8d108329a660f1d9aa5d83e8bc503f024570e20f6cdbce3df5cb9f262174028b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105713469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c985c7f8894e8f65ee4841f0440fceb2bcc2b6225b893794ce16865d280ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
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
	-	`sha256:b237fe92c4173e4dfb3ba82e76e5fed4b16186a6161e07af15814cb40eb9069d`  
		Last Modified: Fri, 04 Aug 2023 05:10:57 GMT  
		Size: 29.5 MB (29536501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2cfb5ec44cfa488b9f01da6da447138e516418fc9244cc0c1d3482c0b7ed6`  
		Last Modified: Sat, 26 Aug 2023 01:01:25 GMT  
		Size: 429.1 KB (429117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8bb1fbaa2faf822e9d9af07305eec80b07b1926afbd193984e0ba28ace27a2`  
		Last Modified: Sat, 26 Aug 2023 01:01:24 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d6b4a95d7711e19119dde139fa6d1bd778cff5a746f4f9d668a20f25017c85`  
		Last Modified: Sat, 26 Aug 2023 01:01:27 GMT  
		Size: 55.2 MB (55161032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf2e15c53f4618a5fbffa05f77639d2555df95cafdf91c9e06dd582dbd29d73`  
		Last Modified: Sat, 26 Aug 2023 01:01:24 GMT  
		Size: 10.8 KB (10842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988725783fba1e87a16da7e280e7f9aa83f948365bbc56f187d5013b4e8de340`  
		Last Modified: Sat, 26 Aug 2023 01:01:27 GMT  
		Size: 20.6 MB (20564083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13c78ddfc234eb3e5c1f8df05324395f93d5c771fbca5ce2ffe91c2c1d320e2`  
		Last Modified: Sat, 26 Aug 2023 01:01:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73feae46200861ccbb3cabd3d4b3a735e87e107251294466c0b27045db9899a4`  
		Last Modified: Sat, 26 Aug 2023 01:01:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb37365844e2a20d472401747bba83812c677960f75a23d1256a6ff538ef4ab`  
		Last Modified: Sat, 26 Aug 2023 01:01:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2893efd85b51671740bdd10d058649e4dc9efe642366e00a19100bdb0ee19336`  
		Last Modified: Sat, 26 Aug 2023 01:01:27 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:7de7bea9536bdc09e11650efb760f6c69e599f2304c4268cc884494824213f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5212912cee79576bda6a74dc8ecbd004be4235e150c323d06be0eedba3f7e8`

```dockerfile
```

-	Layers:
	-	`sha256:b1042bfe590e53f7a8826f4f3bed6e5998479596e2e4fc7b1b56c27a1f56169d`  
		Last Modified: Sat, 26 Aug 2023 01:01:24 GMT  
		Size: 1.9 MB (1853756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14674c180f95235c68533fb436f7481316980d10deb324702a37fc5798c3a1a4`  
		Last Modified: Sat, 26 Aug 2023 01:01:24 GMT  
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
$ docker pull rabbitmq@sha256:8a7a69186edccdc7a49c7be9b683bba6ea728541fd57e5ef64fa2372ba1bef2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100622203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66800c0c3c554b4e36cf717d5d6b11b1554fcd4c5944819aed60f80f1fae75cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
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
	-	`sha256:db76c1f8aa176de7f2698c761088ac1e18cdbbafa6210e405f310221c7a9ea6a`  
		Last Modified: Fri, 04 Aug 2023 05:11:04 GMT  
		Size: 27.3 MB (27347607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031d0cc9c26673046f8416a6ff4f25de728d22001a66acbbce19ad088bcb036`  
		Last Modified: Thu, 17 Aug 2023 00:56:26 GMT  
		Size: 411.1 KB (411076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dbfca14fbe36c0fb8527024e0700b3e61ea3b46610991704770a0f60cc43f5`  
		Last Modified: Thu, 17 Aug 2023 00:56:26 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928717ebb726f6a6f14169c1e923798de763852b9cad93e3157b1f719a8b494e`  
		Last Modified: Thu, 17 Aug 2023 02:03:55 GMT  
		Size: 52.4 MB (52364797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efcfce051baedc255b58a5f8a6995feda3b9e35cfa853a9e16937dc9bba541d`  
		Last Modified: Thu, 17 Aug 2023 02:03:52 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ff04e56d92dc7f82dfa1bbeceb8d2a976118197184eb8d767f23ca63a14db6`  
		Last Modified: Sat, 26 Aug 2023 02:05:29 GMT  
		Size: 20.5 MB (20476028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d618578727485dbc10583afb3c130692587eb1dc7ef2aadd42bf039a40639`  
		Last Modified: Sat, 26 Aug 2023 02:05:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fbb1ddea8920e9e754e8163baf8a8f7309baf955aed02f80f38b65e4ad5524`  
		Last Modified: Sat, 26 Aug 2023 02:05:28 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff64d6411344098717c222bf23da92018f51d5c5ad88b383a416fac929b06735`  
		Last Modified: Sat, 26 Aug 2023 02:05:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e7b1f106977b26534286b9bd13f996245d29d1828e2ac45558d4d4b8ff9234`  
		Last Modified: Sat, 26 Aug 2023 02:05:29 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:ea1c884b17eae4fce3abe88bc900e8f8975049f0bb0d51e87586a50b29286abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1913533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a67a439e2b83d1f9002951aaaf5d688b97763b3f4916c716f176e475b9ad7d`

```dockerfile
```

-	Layers:
	-	`sha256:ffea7706668132ccc0d6b6e9d6aa0b597a2da51d1d7cd9a41dad8bf32a57b3ad`  
		Last Modified: Sat, 26 Aug 2023 02:05:28 GMT  
		Size: 1.9 MB (1854123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1b72cd904bcf25da03a90efbccea94121caec64c2777abbcdd694163edd989`  
		Last Modified: Sat, 26 Aug 2023 02:05:28 GMT  
		Size: 59.4 KB (59410 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:4e7eebd6c6bf85589bc6e5dc9654a3fd061d89aec292dcb12e866d394806f141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105461252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4d21ae25c4e52385cb2109c029d56bb90cb9ee0930e2691d8607f97561bdf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
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
	-	`sha256:e6140760330bb52aa780087331e6207156dc1d36e412010f0de6faacee7817be`  
		Last Modified: Fri, 04 Aug 2023 05:11:17 GMT  
		Size: 34.6 MB (34590887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3215a3a38c6e486070118522e82aa24683bf47f4174e2bf49384ec1aaeff0dd`  
		Last Modified: Thu, 17 Aug 2023 10:42:03 GMT  
		Size: 463.8 KB (463751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beca762f9fa3820d6df5fe10660121405e21725d290c7b83f78cf410f0a2c136`  
		Last Modified: Thu, 17 Aug 2023 10:42:02 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c95d765c6bcbf3ae66650276285cdbf495c8e4654858ab592b6208e9bd3693`  
		Last Modified: Thu, 17 Aug 2023 13:59:13 GMT  
		Size: 49.9 MB (49877989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252aea12bc8625f6a09239ea1243eb0faf186913220a883f1c9158a9d8dcf283`  
		Last Modified: Thu, 17 Aug 2023 13:59:09 GMT  
		Size: 10.8 KB (10769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a154f2b4d6a3a5247163500c8930de6f4fc93d2cf6df0da631bcc5929a2ef7a`  
		Last Modified: Sat, 26 Aug 2023 06:03:45 GMT  
		Size: 20.5 MB (20505958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e518ce822552ea85055df260bbf128584f9fb2388aa40f4497370dace81f6e8c`  
		Last Modified: Sat, 26 Aug 2023 06:03:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687a53073633a283a8e126a622f851fd5b63227e549494534a1862d3c1802258`  
		Last Modified: Sat, 26 Aug 2023 06:03:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f666cb7082a73a47103bc36d4fffb07ba15205630e394d4689178fa0135192`  
		Last Modified: Sat, 26 Aug 2023 06:03:44 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8a73e7b5216653b9dd66497a6172298977fbf68a00fb3796ff59f0734e7d73`  
		Last Modified: Sat, 26 Aug 2023 06:03:45 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:c78b94c1c24bffd7fc6d70db0f1393081cc116574d28510adb61cb7666f2c88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1917902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20f60cc406134b134e5b683237cd0ada832db2c9716a8fcefa3dd8e399cd2e`

```dockerfile
```

-	Layers:
	-	`sha256:9d60fa06bfe29e09a6daeb37f69ef81897cc7515e243d20c3b525801dd50562e`  
		Last Modified: Sat, 26 Aug 2023 06:03:44 GMT  
		Size: 1.9 MB (1858448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6d55c3423d17165db0fe8fb17304899b5d8744a865db9389ae18657590677d`  
		Last Modified: Sat, 26 Aug 2023 06:03:43 GMT  
		Size: 59.5 KB (59454 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:54c7a14a744b927c6184b08fe925e55c69e719cf0abe04d83d18012804b94576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95583824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a012ea7f63678d5f38de355ec32d77468079481be9139fa432e3fd14a073489f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
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
	-	`sha256:bdf265a933ffdd52ec28f006765d35d4119c012d520b564de8ea1b8cdc6c269f`  
		Last Modified: Fri, 04 Aug 2023 05:11:24 GMT  
		Size: 28.0 MB (28013360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eeb1731293e2e3ac5db1d7711621ddd2858b6a1890a63994c3f17c40c21d39`  
		Last Modified: Wed, 16 Aug 2023 21:31:44 GMT  
		Size: 432.4 KB (432415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017bc013e823a52bec726dcf5899f3beb3b23b07ea1dbe2ccdddd975500e5856`  
		Last Modified: Wed, 16 Aug 2023 21:31:43 GMT  
		Size: 10.2 KB (10150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45fd6b2f65c92a142bb2eff9c266426e4069a28d1dc527dacf2cd08f93d58a9`  
		Last Modified: Wed, 16 Aug 2023 21:43:06 GMT  
		Size: 46.6 MB (46580780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c76ff164b79f316320550f396a814b54b3c2fb5ed768fd51ff1d9e9339e7bd8`  
		Last Modified: Wed, 16 Aug 2023 21:43:04 GMT  
		Size: 10.8 KB (10841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329502d70bd3f5084ef75bdae6686199b7ca449e4f4c35720f764c8d2222929`  
		Last Modified: Sat, 26 Aug 2023 02:24:36 GMT  
		Size: 20.5 MB (20534530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c732bb98fc2314552032a2ab276b14bd63ed1199a7b9bb36f720142551fef3b`  
		Last Modified: Sat, 26 Aug 2023 02:24:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2df12578e0d57d1898dc8124e519331d68f258b60e2eb775d06075d7335eef1`  
		Last Modified: Sat, 26 Aug 2023 02:24:35 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c7e0c3d921287cbde0f49d8657ed041dad6a3d6865a60e3154c14f83c7854`  
		Last Modified: Sat, 26 Aug 2023 02:24:35 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07da2f3bb6bc7def69550fc3bddbf1b0533335c8de05ef94baedeaadddfeef68`  
		Last Modified: Sat, 26 Aug 2023 02:24:35 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:50bbf4b1d7a999937a09d4b9699743e53b47e13b7bf5f50189a95cbad6fca323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1914155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c49de391d2dcb4b0c3491c927bb7e86bd6529d35aa6f1c28b18b10e4568d3d`

```dockerfile
```

-	Layers:
	-	`sha256:1639b2e35753991ed4bd4b879f167fa7bab386dc47dbde14eb336426dac41314`  
		Last Modified: Sat, 26 Aug 2023 02:24:35 GMT  
		Size: 1.9 MB (1854755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadb2dc6653cc1cd25320d0d3a5ab67c653b4e0ee823e8addd1dbebbd033acfb`  
		Last Modified: Sat, 26 Aug 2023 02:24:34 GMT  
		Size: 59.4 KB (59400 bytes)  
		MIME: application/vnd.in-toto+json
