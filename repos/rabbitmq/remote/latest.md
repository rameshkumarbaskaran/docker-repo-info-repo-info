## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:d548e59469ae8f20c801be59e1a9e40bddeec2f496f3d1c37b15c7728700ccc4
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
$ docker pull rabbitmq@sha256:31e1c1b3209e9040fc72523c827072de42f1ada37db7f2cdbb09ee4b604a8e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102046843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe33dce462d4b76cd0195ef79d035f6f932a6659657dced1c64eb8050185804b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
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
	-	`sha256:aece8493d3972efa43bfd4ee3cdba659c0f787f8f59c82fb3e48c87cbb22a12e`  
		Last Modified: Thu, 05 Oct 2023 07:43:26 GMT  
		Size: 29.5 MB (29537387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f003867676f41b9c714fb7a0bac1ba9f81e0254308e5f86022da400d7d0432`  
		Last Modified: Wed, 29 Nov 2023 17:40:20 GMT  
		Size: 44.4 MB (44434047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c734c1efdc5722626a49e1bfd72295253bd3ee97c4b7fc7ab66d013fd6926ab7`  
		Last Modified: Wed, 29 Nov 2023 17:40:14 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6f89a4f091433cc70c8fb9dbb542aa2a424a47a96f0980d64ac2c1f1f0d1ce`  
		Last Modified: Wed, 29 Nov 2023 17:40:19 GMT  
		Size: 7.5 MB (7463466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af262e3f8097a0e1b0cc4560dc36f532b77fbf9f79377b009dce55387e238ef9`  
		Last Modified: Wed, 29 Nov 2023 17:40:14 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5766147ec927d5b0f8a1621ab1a511bab1f4c26de6725577631e01913e952c8b`  
		Last Modified: Wed, 29 Nov 2023 17:40:19 GMT  
		Size: 10.7 KB (10697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ad004b2741061c8cc64ca750bc93e9c439a277da0f72a950130666d79438b6`  
		Last Modified: Wed, 29 Nov 2023 17:40:20 GMT  
		Size: 20.6 MB (20598719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665ea42f5c30c74de702f68c88374830cda7afa6e65b9c65951228890ee77225`  
		Last Modified: Wed, 29 Nov 2023 17:40:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fa2ad4f25fd2d2c0a67ae71a4228c7facb3fd91659ef9a19e17f75cab06d46`  
		Last Modified: Wed, 29 Nov 2023 17:40:21 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449af749460c6ea6b885d63807acc1eaa42cd95e6bd65a58d4362c49d6703b27`  
		Last Modified: Wed, 29 Nov 2023 17:40:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76744dd6a6d0c904935f26493a88d076e54acf420238a67ff767a928ff6b6c34`  
		Last Modified: Wed, 29 Nov 2023 17:40:22 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:8d67208bed4ce3c186a57d9c9aaa648ccf6e60a748c83624f162514ce8a12655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15794717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664d43220dd8e8af006fa93c5aeefe10d3bc47df04f60c1170eb996e70f2ac77`

```dockerfile
```

-	Layers:
	-	`sha256:b8d7a99acc6fcfebbc36a897aab19c77a1af0485d7333f2d77ac32ac534f9f6e`  
		Last Modified: Wed, 29 Nov 2023 17:40:19 GMT  
		Size: 2.4 MB (2415918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84d42ae24a5a57709feb5d431ce29e4309c3f0d486144e32278df1f47ec04aa`  
		Last Modified: Wed, 29 Nov 2023 17:40:19 GMT  
		Size: 4.4 MB (4436259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea5c7bb48704452797d9e67ab9086c7e669cb6e5e2abe121f26f84bf578aea5`  
		Last Modified: Wed, 29 Nov 2023 17:40:19 GMT  
		Size: 4.4 MB (4437159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6ea08e3b83c3bdb871c874927f795e90a578c9def004e4e2d3c20916d01455`  
		Last Modified: Wed, 29 Nov 2023 17:40:19 GMT  
		Size: 4.4 MB (4436269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63b44cbe542c0e29fb5725c220221857483f5f5c30ebb74d79ee9a01c17416c`  
		Last Modified: Wed, 29 Nov 2023 17:40:20 GMT  
		Size: 69.1 KB (69112 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:5077c9d9640d6924e1597ed5db9347cb5b061812a2cc2a79c860e26157648b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85966843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc2e91476c3cf3d0fb9c081b09eacffa79fa50913b9aae0fc6fc7127dc42839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
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
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6723c70a949b7c2f19800daa7c0facd5d95527c5bd40a2e8599a8c8062ceb6`  
		Last Modified: Fri, 27 Oct 2023 17:47:20 GMT  
		Size: 32.7 MB (32747508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6eebe3ba29e2c2c6ce17850ccbe73c7ee638081f891ec3c67274d39d6a02bf`  
		Last Modified: Fri, 27 Oct 2023 17:47:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4265268db1d7989bb8e226fc9a267da2c9f6bdceae40eacd9fd84b62b5c7a231`  
		Last Modified: Fri, 27 Oct 2023 17:47:18 GMT  
		Size: 6.1 MB (6060927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdfee9b05f2bfa6a2e025c26dfa1e3271cb3234468386e05dbd394791780c56`  
		Last Modified: Fri, 27 Oct 2023 17:47:17 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa1c7a29928327e068f0349983349c2433896cb4a939cd7ab68c9e2e16f878`  
		Last Modified: Fri, 27 Oct 2023 17:47:19 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75e6697696013abff033d615f8b079a7aa9d0ae4c9fe2f9e7164d30eb879bb3`  
		Last Modified: Wed, 29 Nov 2023 11:24:03 GMT  
		Size: 20.5 MB (20515556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f624db09f3dbfcab95f50e89e0c93f7daa8d48b5b5f7b55f167a078d1e940`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fc93eb1560d3f2342e65bd9d40fe52f8e361479a8647927a5be4e76bbc3def`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7031a3d2e72c6de6e793671707c1d8e1c0d9b0d0934c5d620174d875baa82be6`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b53c3b8aee1bd49b461fef40c71b67116a7f30a3ffee4aa5eb6c01df2c788`  
		Last Modified: Wed, 29 Nov 2023 11:24:03 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:afc6d6c2f86f228bb67b6844c80ee94bfc0ff96b78acbbad8ad57d87b3fcc270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb57b649268ec6275902367fee68adedf8765175e40d8a791f41c2ee7f20dd8`

```dockerfile
```

-	Layers:
	-	`sha256:0724534ce71783ee77a21c437daa13a4b80001bedaabd7bc2057fed0a997861f`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 2.4 MB (2418292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b152f485ffb295033f84cdf65922079b7b79b283aef1a5bb64b534a1af2b2f2f`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 4.3 MB (4282124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f9e6815b4d67c7c35569a76869f07ab59f6baecc86cab14da6eb9b753f2b6a`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 4.3 MB (4283024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a5c551c0894a159ebe9ba2f307d2d7e16f756d3c2c92faaa9984bc95eda6de4`  
		Last Modified: Wed, 29 Nov 2023 11:24:02 GMT  
		Size: 4.3 MB (4282134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef2175d045a620e67adb914aefb9cc5a1e82f710f22a4b3e2c85a5817ec9b6a`  
		Last Modified: Wed, 29 Nov 2023 11:24:04 GMT  
		Size: 69.2 KB (69164 bytes)  
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
