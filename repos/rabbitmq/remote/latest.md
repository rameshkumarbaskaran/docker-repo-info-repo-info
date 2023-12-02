## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:df41e6bbdd77e77c4c0b3f88bc5f58de76ac1b62d0d74054e011648038097a3f
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
$ docker pull rabbitmq@sha256:177b16f28640c04ea0014f70011489d2d485a5ee63138b9bdf04a0146ed97426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102057228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c406f66da2ce375fb591cc1295f36a1dbdcd4e3916f29dcf512356f3111defa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ARG RELEASE
# Wed, 22 Nov 2023 06:55:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 Nov 2023 06:55:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 Nov 2023 06:55:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/bash"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:5e8117c0bd28aecad06f7e76d4d3b64734d59c1a0a44541d18060cd8fba30c50`  
		Last Modified: Fri, 01 Dec 2023 08:21:32 GMT  
		Size: 29.5 MB (29547417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76110771016c78e0353db66b33c17b33c4f136388345908cb110fc17edf85ab1`  
		Last Modified: Sat, 02 Dec 2023 02:20:10 GMT  
		Size: 44.4 MB (44434149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55be5922422868b1bc310292ce6194f4f64ffbd53d1188164c2e6027bcd878aa`  
		Last Modified: Sat, 02 Dec 2023 02:20:09 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76109d95b373a2f36441fd3d9facbe85836884aac1fe96cd90b6297cc3dcafd`  
		Last Modified: Sat, 02 Dec 2023 02:20:10 GMT  
		Size: 7.5 MB (7463495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de86b1669686e788a9116b083517b3505a5978b9bf54dbee881ecef768e25e7`  
		Last Modified: Sat, 02 Dec 2023 02:20:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2df4c6df8d3e3678dc7b45715849c1a644e2dfbb7e36b8cb95c29fb71f1c0e`  
		Last Modified: Sat, 02 Dec 2023 02:20:10 GMT  
		Size: 10.7 KB (10728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ad6d067a495ae82240c4cf85df4fb05b9770451cc2c829cb69fd2f3c5a242`  
		Last Modified: Sat, 02 Dec 2023 02:20:12 GMT  
		Size: 20.6 MB (20598917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c7daf802918fa28016006343547e1d8ca7f3454e423c4c6afb2c5f6ee6e88e`  
		Last Modified: Sat, 02 Dec 2023 02:20:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fae49f5f5ef6b5f789912a1609ce9654dcde25a7493a060dae68f01fd55cca5`  
		Last Modified: Sat, 02 Dec 2023 02:20:11 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb82db8a3d30d14ba09372c879b1be7f0e37a33fd616d6a7420d4ba5e16ca68`  
		Last Modified: Sat, 02 Dec 2023 02:20:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a814b64486494618eb8fdd50c6ae94de2181f362082db021c8f4515fd7ae0a3b`  
		Last Modified: Sat, 02 Dec 2023 02:20:12 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:e6c49c636dd3735db65be657d1f419e521cf8f648f85690e843399f869f84792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15787780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ada9fc0804248ac05492aaece9dd35bb40290869d014d3a683ae5e831c9853`

```dockerfile
```

-	Layers:
	-	`sha256:62f0c68f93320eaf282a8a5c69f214fda7fac7bdcec75bea193d11fdce50d912`  
		Last Modified: Sat, 02 Dec 2023 02:20:09 GMT  
		Size: 2.4 MB (2414181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4497e426f50a903b83f84157f1f5f79291a8fbe1121309c54c26c9dc9b474f`  
		Last Modified: Sat, 02 Dec 2023 02:20:09 GMT  
		Size: 4.4 MB (4434526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05574b1582f54699b8bfe34e8e1569a555281d8527c66deb04300191ae6f7632`  
		Last Modified: Sat, 02 Dec 2023 02:20:09 GMT  
		Size: 4.4 MB (4435426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5242b5afcff8721ec510f8fc4b52d608dcdd68c9b37ab56a9b14ca3cd993e96e`  
		Last Modified: Sat, 02 Dec 2023 02:20:09 GMT  
		Size: 4.4 MB (4434536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7456dbccdb5a4146a0218b385f2495ad53abbca1973efc059676c45d7de053a4`  
		Last Modified: Sat, 02 Dec 2023 02:20:10 GMT  
		Size: 69.1 KB (69111 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:0c3d4939711f69521d1ac39f2a0730947463de9117be1f66a3b748886507239b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85973216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd052ed61671b061fd560f0e4e13b5235fafffefecefffd00fe4f60c34ec1b51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Wed, 22 Nov 2023 06:55:25 GMT
ARG RELEASE
# Wed, 22 Nov 2023 06:55:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 Nov 2023 06:55:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 Nov 2023 06:55:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 22 Nov 2023 06:55:25 GMT
ADD file:852469f16f85d8eff83511eb82d6d4409a4608b882c1634281a43c1c481f70c0 in / 
# Wed, 22 Nov 2023 06:55:25 GMT
CMD ["/bin/bash"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:ea58aa779a072439c842d78cda3d6a8b9c16c8c9acc171db9265b1c82fafecf3`  
		Last Modified: Fri, 01 Dec 2023 08:21:44 GMT  
		Size: 26.6 MB (26635366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4af5b65bb03a4a71a3b7bbc3885c3a0d2d3006d01bc9f9d7041324c1b79309`  
		Last Modified: Sat, 02 Dec 2023 09:37:28 GMT  
		Size: 32.7 MB (32747587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d71a83bcacf357c610557996163daaef4b52e9e27c34b29ef6f6c0da0748b9a`  
		Last Modified: Sat, 02 Dec 2023 09:37:26 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5733389e0dd52282ab0b92145d8ffe337063d0a45afeb8e96d3a8526b894f7`  
		Last Modified: Sat, 02 Dec 2023 09:37:27 GMT  
		Size: 6.1 MB (6060911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b214483fb1e17d6e40b32b284bafe07570a2b467db477ba398e889b66eeb08f6`  
		Last Modified: Sat, 02 Dec 2023 09:37:26 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87b652471a719e1d35a096c14e46364ce787844fe9f6384faa76ef45df22c8a`  
		Last Modified: Sat, 02 Dec 2023 09:37:27 GMT  
		Size: 10.7 KB (10689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256355a597c4f8beda8c2e2bd6b8167dbbfe0802490b355872c32a35a1ee4003`  
		Last Modified: Sat, 02 Dec 2023 09:37:29 GMT  
		Size: 20.5 MB (20516130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebedf65c31e7cfca70f8032304432b8bfd987411eefc1b3461cddf5b1c29ab04`  
		Last Modified: Sat, 02 Dec 2023 09:37:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709e08e135b455d9284a6d59cb1c7125ac3780a0ac13a83e311f9d1c7511d26`  
		Last Modified: Sat, 02 Dec 2023 09:37:29 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10290be04f5811951b1850296e91a6d60c85a3f6b5864b7613f6f009252c3bd7`  
		Last Modified: Sat, 02 Dec 2023 09:37:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad3596da247a7f6f08bfaaa65301ca281d0fe05f8dca47501f2b33ecd4eb935`  
		Last Modified: Sat, 02 Dec 2023 09:37:30 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4d9ee0508f5fdd729a63d3519234e6ebe0ae7dfdff96da9fd0abdf17090c6fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15327963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763d58313066a780640d3d01dddaaf27c876019100b3c2a69e2b078f062cfaa4`

```dockerfile
```

-	Layers:
	-	`sha256:caef4b2b36df1e1b8b630f29576467d0eda400d491b53d7d1be5a10189a0b6d9`  
		Last Modified: Sat, 02 Dec 2023 09:37:27 GMT  
		Size: 2.4 MB (2416555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e988dc90fa69fa8081db74e3278c6a2ed7cd2316f02674e77965f6a29d18df`  
		Last Modified: Sat, 02 Dec 2023 09:37:27 GMT  
		Size: 4.3 MB (4280391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e4083ff8a76367d991fa72a59891637a8891c0d597407371bff8f0bcf77b08`  
		Last Modified: Sat, 02 Dec 2023 09:37:27 GMT  
		Size: 4.3 MB (4281291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cbdd3bd70b638fe035acc55c1aee5d546efc88333d54c787c62e4a179525c7`  
		Last Modified: Sat, 02 Dec 2023 09:37:27 GMT  
		Size: 4.3 MB (4280401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a95de38b0e920a5b5292098c4fcfd230a4fde7c8c0a8aad1e59e828bbe9232f`  
		Last Modified: Sat, 02 Dec 2023 09:37:28 GMT  
		Size: 69.3 KB (69325 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:65873a976b065f88436fd8a5d69ed1cd22a2d83661ed3e80015fd77f7506d76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97277888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a83cdf5bace30fc239fb15288a9be93d8c2fef33fa30095c36b076dc6be412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:bfbe77e41a78ee38147c5761aa8bc896d9f6e1e648b23468f294065ffe03c107`  
		Last Modified: Thu, 05 Oct 2023 07:43:33 GMT  
		Size: 27.4 MB (27351048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba28653fb67585bce79733e4fe20dd1c6b4eef04f1fd2e050d5fac09677dade`  
		Last Modified: Fri, 27 Oct 2023 17:49:37 GMT  
		Size: 42.3 MB (42286767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04931e0b84f1f7fcd48506680656b6f9f5699b69f1405326672b26fdad04d200`  
		Last Modified: Fri, 27 Oct 2023 17:49:34 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89b3cc0afb999a9dc4e9699d660e1dfbc8ceb80f7701c31ce2be933efbbc55d`  
		Last Modified: Fri, 27 Oct 2023 17:49:35 GMT  
		Size: 7.1 MB (7119541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde2259342e5ee7d236a7d7fbb1d3a6875b8f27744166e14ec1b299feb18dab2`  
		Last Modified: Fri, 27 Oct 2023 17:49:34 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3e7138b6221f0b4b599fd844a81458b571dc8cb35a6c3ee15eb318c33e531`  
		Last Modified: Fri, 27 Oct 2023 17:49:35 GMT  
		Size: 10.7 KB (10706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41edcfe355b055bad137983a9d2a87c0ba6bd24fbb3c07b5aed31893276cf`  
		Last Modified: Wed, 29 Nov 2023 06:57:27 GMT  
		Size: 20.5 MB (20507299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da04ab10a5c318b5336a100c384261d1b701661c4b1b401b5380e4dcf90e1a`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064c4a7e35ed30783807ccbe7b1f9ab16c9c5f1b939a9a4b2a9218799360eb85`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c121af4efd097fcbbf7181f7bbdc747ef3f71efdf6a3b1bbb15e7edab448d23`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ff01acd878d65639637d815536503fe9880fdf9d5f4378c0cd9e4db759ad9e`  
		Last Modified: Wed, 29 Nov 2023 06:57:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4e5244036e8a60362058f66c45bdf2c9dec581a8572517ddd0b90e675ef780ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15785527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9358fab889d6a2c4aaeaffcf44a9bdc006a1e4ac66de1751efacbe25c33c01b0`

```dockerfile
```

-	Layers:
	-	`sha256:9afdfd52227aa487fce1df9abb64d9a54d1ca970ea58f065e1c19cd04934d30a`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 2.4 MB (2416251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee7079049f722a7627e1e5974963449d8cd5f336796214ad51462137aa8812b`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 4.4 MB (4433135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a8d63e8b93091e272d012c757d32b336acc0da904fb0701e1a7f62f095cd6b`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 4.4 MB (4434035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7715dfeee8e4f691e71a9ff26ba2533987e0621c51e7007c12237105101abe`  
		Last Modified: Wed, 29 Nov 2023 06:57:26 GMT  
		Size: 4.4 MB (4433145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7de2afa40fe917cf0ba87af623bd419595072ee1157319a626a318294043d0`  
		Last Modified: Wed, 29 Nov 2023 06:57:27 GMT  
		Size: 69.0 KB (68961 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:e756432df5f01828ca1905eae14b4edb3439c59615017b3ec7b962e51babf54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101711782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551422f6d01d36955969f6b36f9b94decf5d518f63512515a8e1a3a2f836062e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:90496cba4a92b0bf6a8307bab5dd30100905ac891d478aa27771408328244c33`  
		Last Modified: Thu, 05 Oct 2023 07:43:45 GMT  
		Size: 34.6 MB (34555968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b853531570b5e27b4e44fd61671df7dc02ff7f8f69c4cbe564abec2783be6`  
		Last Modified: Fri, 27 Oct 2023 17:32:14 GMT  
		Size: 38.8 MB (38768738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc6fc30f4a2d13ede0478b5728e3f2fbb7c6e68aa0279c6a7d36b9f09a758c6`  
		Last Modified: Fri, 27 Oct 2023 17:32:12 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f24f0b38e012085b791f8d11a350a00731c01a0a6ad3c619456d52615e36dc3`  
		Last Modified: Fri, 27 Oct 2023 17:32:13 GMT  
		Size: 7.8 MB (7842385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c68f325716feab6272d1c0f68d70d3801cd0ae4274b41c37c8873f2733e10`  
		Last Modified: Fri, 27 Oct 2023 17:32:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a4362667205863b8c6e96673aa6def5f2f32609a25e4ec0b582075f61a4b8`  
		Last Modified: Fri, 27 Oct 2023 17:32:13 GMT  
		Size: 10.6 KB (10647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110065f9fc3b8b077b97a21ef65b1cfedab62678c1f54a95e9958b1b92268eb0`  
		Last Modified: Wed, 29 Nov 2023 09:04:19 GMT  
		Size: 20.5 MB (20531508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107507dfa489427d3ac72b177ab726c11b1c1e2f006604b2f5ef9e71d4e9733f`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01072f130dbbabdcfb7d3a42d3e40c311b9aab0502e6519c49ab3c43f8844e21`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ebfb2c9ee978c212cafb0665a1011de2a56b6f6460ff11baa9e0536993b39d`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1565b2d7be491f23464821c2039a30f33989bc80fb170780ce017ba3457f7a`  
		Last Modified: Wed, 29 Nov 2023 09:04:19 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:818cbcdd762e19da5c42c8c0600c0f5e14db64776d745e8fe05b9babfc1a1642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15704884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1498671ea7f09ce300779fca95da41a3ea0985f946ca5f18efe04a9abba4495a`

```dockerfile
```

-	Layers:
	-	`sha256:f99ec818cd8becb6779f9ac06a4783462b132c1310162280db2e45b7bde4b269`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 2.4 MB (2420413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c53cebf2eb78c3f92c7211ee2a3e8117e44e259f50c1dc30335d9d75e9b42ec`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 4.4 MB (4404850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0289342708d9a58e168e8cc268ad169d0ead577b42627b60abf1dabd64ba6366`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 4.4 MB (4405750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2fac6410e2013a496d04b0622e132c2a72070c7d22f1abe94053e9b7332f8d`  
		Last Modified: Wed, 29 Nov 2023 09:04:18 GMT  
		Size: 4.4 MB (4404860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c641a09a3b9e73197786ad40c180508511023e326c9f1c94ecf55a3161c8b3b4`  
		Last Modified: Wed, 29 Nov 2023 09:04:20 GMT  
		Size: 69.0 KB (69011 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:66a70bb5ab843d04395162a2d34b6bafcd1bf349d0b3cb1b1eb4b3499364e38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92538605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4978725d8ea694a85f99eb62dd2e3235a097255a106448bc6f5b062bcc811f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Oct 2023 07:29:34 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:29:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:29:36 GMT
ADD file:d165475f8f027ab758a463da57c8c29f5d302f0a87a475ac68fdfae30005c7ac in / 
# Thu, 05 Oct 2023 07:29:36 GMT
CMD ["/bin/bash"]
# Wed, 22 Nov 2023 06:55:25 GMT
ENV ERLANG_INSTALL_PATH_PREFIX=/opt/erlang
# Wed, 22 Nov 2023 06:55:25 GMT
ENV OPENSSL_INSTALL_PATH_PREFIX=/opt/openssl
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/erlang /opt/erlang # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"erlang-sbom","packages":[{"name":"erlang","versionInfo":"25.3.2.7","SPDXID":"SPDXRef-Package--erlang","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/erlang@25.3.2.7?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $ERLANG_INSTALL_PATH_PREFIX/erlang.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
COPY /opt/openssl /opt/openssl # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"openssl-sbom","packages":[{"name":"openssl","versionInfo":"3.1.4","SPDXID":"SPDXRef-Package--openssl","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/openssl@3.1.4?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"Apache-2.0"}]}' > $OPENSSL_INSTALL_PATH_PREFIX/openssl.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_DATA_DIR=/var/lib/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_VERSION=3.12.10
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Wed, 22 Nov 2023 06:55:25 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Wed, 22 Nov 2023 06:55:25 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 06:55:25 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie"; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"rabbitmq-sbom","packages":[{"name":"rabbitmq","versionInfo":"3.12.10","SPDXID":"SPDXRef-Package--rabbitmq","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/rabbitmq@3.12.10?os_name=ubuntu&os_version=22.04"}],"licenseDeclared":"MPL-2.0 AND Apache-2.0"}]}' > $RABBITMQ_HOME/rabbitmq.spdx.json # buildkit
# Wed, 22 Nov 2023 06:55:25 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:0ffe28a7c279dfdb86b23c0d22d37e89442a6d771fbded124aee76b24119c2c1`  
		Last Modified: Thu, 05 Oct 2023 07:43:51 GMT  
		Size: 28.0 MB (28023918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8643c35838ba632b1a5d7085fe53d8f2a2f8385ef376f70ba3cb731946166025`  
		Last Modified: Fri, 27 Oct 2023 19:20:07 GMT  
		Size: 37.4 MB (37420821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9fa9aefda9a265b82db0495b980501d72b41303d8127e43ef5c16b2dc1aca`  
		Last Modified: Fri, 27 Oct 2023 19:20:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4136331ad64a00dc20d9237f6bcbe00a361f49fda8defb1fc3c5a0fa005d30`  
		Last Modified: Fri, 27 Oct 2023 19:20:04 GMT  
		Size: 6.5 MB (6513955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f591b67f1f68792b7e03a5b13ada69beef9fa104b36bc41c6a021573300b8212`  
		Last Modified: Fri, 27 Oct 2023 19:20:04 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a78ef45c4b57da838fa8783026f9dd9c82b27621ba488120922e2ae5dff253`  
		Last Modified: Fri, 27 Oct 2023 19:20:05 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0e602ec11a21ca14a2a7898b19d843ab2a9c96cc424f3ffddd7156f1250c2`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 20.6 MB (20566607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4733c15f06047009a66c00fe61d89bc0e881b5bf5442f8a90f6cd7bf16954715`  
		Last Modified: Wed, 29 Nov 2023 06:32:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2f48399a90a4c07de0dd06783248d0ebb695812c2b8aa4d6c0b1ec9d40318`  
		Last Modified: Wed, 29 Nov 2023 06:32:44 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267e523f82b7a7450fa4a38a2850a1075e31f0c9bb8bf92b1c2b9a1690ace72`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4370725b6de0957b825bb0ba7a8ad413edecd85da305e20e863bc2d2b3a50`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:4d8ed2771c3b2d52fd4ad5155c73c8fa31741c0339128f21f5622968f9cabf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15389991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ad3bb7e28eed8e6dccf899c9ca04e9e0e541e44848cf6ebbb21c577094dcb6`

```dockerfile
```

-	Layers:
	-	`sha256:af91f27152cd148aab7cb2c9d1b9a2017e5551b403bf5df096f89d97a6a7a145`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 2.4 MB (2417733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db92b5122c3e7a8021f4320e5a3a379144813c9d7dd8378375994455f4baf4c`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 4.3 MB (4300799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b259eccca8249995a988cfcf65e6a0bbefecdccab64ad737f6d245f30cb9734`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 4.3 MB (4301699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4524930d7a6fae2b967d9df8743faf7817d1937887117ffd4291de77feb1071b`  
		Last Modified: Wed, 29 Nov 2023 06:32:44 GMT  
		Size: 4.3 MB (4300809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f8376a7bb348469880c674d4057f57e0c5d4ac1ef2310e01fa88a9674daa88`  
		Last Modified: Wed, 29 Nov 2023 06:32:45 GMT  
		Size: 69.0 KB (68951 bytes)  
		MIME: application/vnd.in-toto+json
