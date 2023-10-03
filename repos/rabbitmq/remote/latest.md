## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:ea8273fba7df876f647fb5bd49d8036029d44e50ef342a80c39c261f94fff825
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
$ docker pull rabbitmq@sha256:4972d1d87eb5bd2fc0a880bb6352c8b45cf5a22374b6121ab8353547d2f27a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102024898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25af5fb9e30b275f412626aff0cd19e7f19f6e9d9a6c65d58caa1b8e7abaf9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ARG RELEASE
# Fri, 22 Sep 2023 11:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:37aaf24cf781dcc5b9a4f8aa5a99a40b60ae45d64dcb4f6d5a4b9e5ab7ab0894`  
		Last Modified: Mon, 25 Sep 2023 10:30:37 GMT  
		Size: 29.5 MB (29538209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83098b347fe110dfaf8d80228ee529a5bb6a6d1f1185fc2dddf913f7951bc9e7`  
		Last Modified: Tue, 03 Oct 2023 06:05:18 GMT  
		Size: 44.4 MB (44442134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8bc3103c98119cdfe4a2e110645fa0003462a12df579cb9290cdc4d1c5ca1`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 7.5 MB (7456688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9c00f6aeb54b0de545ef7ef87bd21e9f1f8ef4d58a1c1f0cb798ca56d9c98`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf31d35f1dd1a2924811c335c47575b005e90732135296f878048386f2895fd`  
		Last Modified: Tue, 03 Oct 2023 06:05:17 GMT  
		Size: 20.6 MB (20575388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3305cdb865c5952a07d6d26f81ddee69c0524e87f8b2817a011f9155df8eab`  
		Last Modified: Tue, 03 Oct 2023 06:05:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94d30d3af7fec20dd3acbe2caf9cda388027dde7b145935104a9983d9164304`  
		Last Modified: Tue, 03 Oct 2023 06:05:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd90db7491a58bfd9c31bde9fe493e5fa9daae2cc6ea94491aa337f50c72617a`  
		Last Modified: Tue, 03 Oct 2023 06:05:18 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfd185b71c079e34537a00d3b92851bc1571ce7b353068a66879e8272a732fc`  
		Last Modified: Tue, 03 Oct 2023 06:05:18 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e66a3ed89288ba5ca16500ba729a9bf59514a593a52009f166581c7cbaa54b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542884231f22546d94c2b47440dc6ed40923ce7e7a3a89f6869061a6c44ca9d2`

```dockerfile
```

-	Layers:
	-	`sha256:656749a58e4cbb1d4fc23e49e60fb4f2057c8528bf56ab4c5b4ad57fd58d8969`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 2.5 MB (2479516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d97fab55dd90abcea471224aaa2de49f00d9575326077da7dee187a7688780b`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 61.3 KB (61337 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:89bfd6a2a2a4de26b7ac77fadcf0b60407e6b4fb971f17f79aef38427f2f84e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85937060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88bd81a4ee143bddf645e630f7a2da9ca89416b7a5bf0249cbb87dd4e6cd625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Fri, 22 Sep 2023 11:05:26 GMT
ARG RELEASE
# Fri, 22 Sep 2023 11:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 22 Sep 2023 11:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 22 Sep 2023 11:05:26 GMT
ADD file:0008d56422c09f73afbcd40ace46d311e36ba0d60eef05198ea3665172ba3433 in / 
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:1adfa548dcf4236495853b0c0ac47ba789ff1a5d1cd640c102ab0ff13d8ca08d`  
		Last Modified: Mon, 25 Sep 2023 10:30:49 GMT  
		Size: 26.6 MB (26631526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db38432b797869a26144d7a6c1acc5a40c8396cd9a31c5a65d653cb8c086f53a`  
		Last Modified: Tue, 03 Oct 2023 07:44:51 GMT  
		Size: 32.7 MB (32743737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0152b8eba3c68aed0e419f54709ea81051184de7375eed29840c7fd11c53797`  
		Last Modified: Tue, 03 Oct 2023 07:44:50 GMT  
		Size: 6.1 MB (6056484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15443b380534b33fdff1004a7544022320bda6bf52f87e7a870a43bd4a601be7`  
		Last Modified: Tue, 03 Oct 2023 07:44:49 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2e532dc771f6e69d0c9532d9327f315b6c61f1cdce7eb15e9871f4ebc9081d`  
		Last Modified: Tue, 03 Oct 2023 07:44:51 GMT  
		Size: 20.5 MB (20492830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f058c858619b50f3466f02da8d3a6e5542b0b716d92fb270e88549bc6e4b6a1`  
		Last Modified: Tue, 03 Oct 2023 07:44:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eb05aa9334d7405a6c1391ee5af62a650b0f41b0c8aaccfca049824389ae8d`  
		Last Modified: Tue, 03 Oct 2023 07:44:51 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c0072098b688623ff6809bc4d72c529d825e058f4db9a633230be0b0b1b531`  
		Last Modified: Tue, 03 Oct 2023 07:44:51 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d534c2bcd3dafe0d839f67d5e0f31d9b6c98b23c11977e2d419b14d58bd9fc`  
		Last Modified: Tue, 03 Oct 2023 07:44:52 GMT  
		Size: 835.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:887089950e21b2da1fb3f6e94097b939883d471592cdd3d6b4dd797449495049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2549565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49d40ad9b33fa59fea56f863553a039ebf08c8b4b14b6971ea1e59c5fc3cd9b`

```dockerfile
```

-	Layers:
	-	`sha256:438b2e504c675898a66cec4e63f897ad71f7fa2cb2944a1aa3e7eaba6c2b6925`  
		Last Modified: Tue, 03 Oct 2023 07:44:50 GMT  
		Size: 2.5 MB (2488040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24272bfaee2f218d1afb9ec6c9bf4c030b928ec8592d757a940c1341d749cb1`  
		Last Modified: Tue, 03 Oct 2023 07:44:49 GMT  
		Size: 61.5 KB (61525 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:96647879d816eabea0c4313e790979eca1a78ab8d90d7cfe6d7d1506e42e9a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97239970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c427f2893df62704aed6d44c30e2c2b11bfa8cd1546463a996a76cda91e14f1d`
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
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92e45f5d8cdfd8a809c614b1e5179187bab843d0a815e596e7e0e53befceb33`  
		Last Modified: Wed, 20 Sep 2023 09:18:29 GMT  
		Size: 42.3 MB (42277727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27b7fd9d6be54ef6c327696e289780323c5018a646e211024853f1e29531aad`  
		Last Modified: Wed, 20 Sep 2023 09:18:27 GMT  
		Size: 7.1 MB (7113719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6a5314957b997b3816f49e9bca5e0354e01f9cbb1afecf199117a7b4c5ffc`  
		Last Modified: Wed, 20 Sep 2023 09:18:27 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01d99ba44fdae9a70c441692ae690fcaba78bae21df0a98f9bdd38e3fc56981`  
		Last Modified: Sat, 23 Sep 2023 01:11:07 GMT  
		Size: 20.5 MB (20484959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b52e31db1100a31ff95ff3e20941983550994dbfefd00ba3144df12fc7b40f`  
		Last Modified: Sat, 23 Sep 2023 01:11:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd8d8e65db3a1027da76046a70d945cc05167282ac391353cb5648b9a3b9c1d`  
		Last Modified: Sat, 23 Sep 2023 01:11:06 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29f1e1d896112ea311f1465ded851e594aae94f5da19adeef117fad69cbd3a8`  
		Last Modified: Sat, 23 Sep 2023 01:11:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d823223eb1c0f39367960329af28ed045f24ee7179a19e0b00158dd18fe048b1`  
		Last Modified: Sat, 23 Sep 2023 01:11:07 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:f1d1e398eb423c93ebd3d221f56c7be7382bf1af09167f0ae1361129c7578f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac27ecc42163f27ab3742c69ab7464ce73285a755c73e7d4d06d5b2c261a49b`

```dockerfile
```

-	Layers:
	-	`sha256:e26ca6f47f9b5046a0d04e7a1bdf9dea78be2ec7ae41c0b7872d24bd7295a54d`  
		Last Modified: Sat, 23 Sep 2023 01:11:06 GMT  
		Size: 1.9 MB (1854134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb10bb93c5e368c465dcb286278acace5cc2d1c015d208bb01ac37b27b8e45d3`  
		Last Modified: Sat, 23 Sep 2023 01:11:06 GMT  
		Size: 61.2 KB (61197 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:d0d78d9b1127dd17436d215f0a32a23479220181137915ea813c98ecc862b17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101688242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e095e8e6465acdbbd08e554a3cb61675eab312e46a12d6295fd631bb9b766f`
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
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
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
	-	`sha256:afeee85216adc7f5a68cf64303189f65648bb4ac7778f6daf2cee768d8719ca0`  
		Last Modified: Sat, 23 Sep 2023 00:51:40 GMT  
		Size: 20.5 MB (20512202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3427943d03688d4787d88d7ecdf53cf53c1f261cc19b731c2074d8a802c21`  
		Last Modified: Sat, 23 Sep 2023 00:51:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f8b5d442e0c91cf47cd03c2a26e7aea0e048e2e71f0d7905e8b2f7793cd50`  
		Last Modified: Sat, 23 Sep 2023 00:51:38 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4f0a2489fe822d3ac846bdaab7e51bfab1ccc4b2913373d39521db471fcd8`  
		Last Modified: Sat, 23 Sep 2023 00:51:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbda221c5c79559bffda73074b36adf0aa8a9792d04523822c989a85995cff`  
		Last Modified: Sat, 23 Sep 2023 00:51:40 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:560f7a53488ff7a27e2955db17de3f194c3fa9a7e8c89b80104742c390e56d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1919702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745b6c9a857d800320c5283727b4f508cc9b0c23110c0be116c56b8dc0e1d19c`

```dockerfile
```

-	Layers:
	-	`sha256:7e28e9779c4a3c31a196b80fd5c3520216b48f191fc44951fa0d41327efae4c6`  
		Last Modified: Sat, 23 Sep 2023 00:51:39 GMT  
		Size: 1.9 MB (1858459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af8a86a827f20680469c6389179deb839aa028b386d80dbad8c2b766380bcf9`  
		Last Modified: Sat, 23 Sep 2023 00:51:39 GMT  
		Size: 61.2 KB (61243 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:05a2636b57d9e508cfe2942741fb0830dd2f82e22bfd13e71b51409d17f2d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92497936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a392c649aa7aa79be65efa3891063258b4d592ccb04528b10e9f35ef6f62af7`
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
# Fri, 22 Sep 2023 11:05:26 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Fri, 22 Sep 2023 11:05:26 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_VERSION=3.12.6
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Fri, 22 Sep 2023 11:05:26 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 11:05:26 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
RUN ln -sf /opt/rabbitmq/plugins /plugins # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 22 Sep 2023 11:05:26 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 22 Sep 2023 11:05:26 GMT
ENV LANG=C.UTF-8 LANGUAGE=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 22 Sep 2023 11:05:26 GMT
COPY 10-defaults.conf 20-management_agent.disable_metrics_collector.conf /etc/rabbitmq/conf.d/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Sep 2023 11:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Sep 2023 11:05:26 GMT
EXPOSE map[15691/tcp:{} 15692/tcp:{} 25672/tcp:{} 4369/tcp:{} 5671/tcp:{} 5672/tcp:{}]
# Fri, 22 Sep 2023 11:05:26 GMT
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
	-	`sha256:85a42d49c899b9d39020fd9731a1b367ba7771b1ea8af81c8a06ec77f57f5426`  
		Last Modified: Sat, 23 Sep 2023 00:50:47 GMT  
		Size: 20.5 MB (20543540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c24587f9625025919dddc4637321a2684ed989e02445c8121809e0cd7d0df`  
		Last Modified: Sat, 23 Sep 2023 00:50:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820c09fd4af482c6a7939ad9cafb585557853ed7e5c58f33794f601bec7e4029`  
		Last Modified: Sat, 23 Sep 2023 00:50:46 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f10abba7cf1a7ae05fd5068a299a3507b3262d5f29e67b525f110881856ba5c`  
		Last Modified: Sat, 23 Sep 2023 00:50:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89256ea02b6097f0fbed261d9defdbf45bf6646276cf58f0f8c77929842fac`  
		Last Modified: Sat, 23 Sep 2023 00:50:46 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:6ac5bd0855116d4aece154ff8c9a458e5ce802020fd32a6dad87fefe1a052bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67e6a13d5c65aedc2350627b73e93c495c2a47c0e37c8df88a25e57f51df635`

```dockerfile
```

-	Layers:
	-	`sha256:3816b7f53fdf3303e16ef6a3d8a1bc62b13b6edf71b30a28d1de561f411122cc`  
		Last Modified: Sat, 23 Sep 2023 00:50:46 GMT  
		Size: 1.9 MB (1854766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0312f3ccf844665d92609d298ae52eadaad31b8875331ca9b9dbb3b2bc051a`  
		Last Modified: Sat, 23 Sep 2023 00:50:46 GMT  
		Size: 61.2 KB (61187 bytes)  
		MIME: application/vnd.in-toto+json
