## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:d96c58d1e2e55a32a03fa9ba01d00c6383d1aca26fb2790f14ac411fd6e45152
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
$ docker pull rabbitmq@sha256:999a1621cf23664d7b5b978f732031a4e3ab9dca74142fd9106b9c2ac13b86ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102022560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898222cdea43e486fef5731a88985152ce2e8dc7b3eaf0d0709821f69ceeffb6`
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5c9bc07c0d95663204735babb6678ae6df0e7a32e3e74a2bdc549c473f9016`  
		Last Modified: Fri, 22 Sep 2023 01:00:07 GMT  
		Size: 44.4 MB (44441916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717f393744c2070e11d2de4ff2f82dc293dc22f42238b75b9b4602e6f9e7374e`  
		Last Modified: Fri, 22 Sep 2023 01:00:05 GMT  
		Size: 7.5 MB (7456656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43efe57804eba03d76b69e9318b14555db4f5c2e643f6c873866ad54e3fe6bb4`  
		Last Modified: Fri, 22 Sep 2023 01:00:05 GMT  
		Size: 10.7 KB (10738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5534f2695725a8f4df32c81d25d1843dab7490d196839dec2229c5b2bd53d`  
		Last Modified: Fri, 22 Sep 2023 01:00:07 GMT  
		Size: 20.6 MB (20573785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d45e925fba0204c8998eb965b827d2e42e5068573eb38bcf9824f768b6f4dfe`  
		Last Modified: Fri, 22 Sep 2023 01:00:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451ce99df83f930b138ec512a968429bbf88c53b608a962d8122a4c4cf147126`  
		Last Modified: Fri, 22 Sep 2023 01:00:07 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc59d12e7ab9c673277b3875ef14e9b15aa817f4327b536e0f81f20bc01466df`  
		Last Modified: Fri, 22 Sep 2023 01:00:08 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a944fa9f45b13486581dd64ca6fee128e40722abab256bcec22b95ed9e58291`  
		Last Modified: Fri, 22 Sep 2023 01:00:08 GMT  
		Size: 834.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:cd22ef5ae757db6d7a5069563f43702d7ae6ade8ab3cbdc26f8503dc5b8024ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da165cdaf81d6dbae7eb774c35a5834275a23dd9a1291e8be35bea8705ae64cb`

```dockerfile
```

-	Layers:
	-	`sha256:2dfda3b50673ab531a8b3473555451500ba6bcd3b5be690778a30fbc0a0c096e`  
		Last Modified: Fri, 22 Sep 2023 01:00:05 GMT  
		Size: 1.9 MB (1853767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3bd867582df65f21d05545cdaaee21c5e5d0e8ed18b211c2e9709c12173c80c`  
		Last Modified: Fri, 22 Sep 2023 01:00:05 GMT  
		Size: 61.3 KB (61348 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm variant v7

```console
$ docker pull rabbitmq@sha256:35b68856e90f4574fb94d13f8f2d2721435ed5f9e9227189202be8bbce163825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85445751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd5c55b2d7b4d0b59075b301d201e7e8225af0922bfad16954ec8962846c5b4`
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:d79cf5fbd02b4f64ddfb1ba3ae0178a904f012bc2ff0e5603ffdb4668a8f529c`  
		Last Modified: Wed, 16 Aug 2023 06:32:59 GMT  
		Size: 26.1 MB (26142545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6f7bfc2a3d1f78a82c379e653b9c82a7f95f6f7bac6b4a2364a09116d570f`  
		Last Modified: Wed, 20 Sep 2023 04:54:07 GMT  
		Size: 32.7 MB (32743780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a021b429c8bb2a2d7a596ea82b5906f46de88451d8a6de43794637792f7198`  
		Last Modified: Wed, 20 Sep 2023 04:54:06 GMT  
		Size: 6.1 MB (6056428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76840ae68a893b33d07d8103df3ede84ce967200e6a923475b31cbf06e41a6f0`  
		Last Modified: Wed, 20 Sep 2023 04:54:05 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73116be27fdf0df786692c0ab159d69414e46e67d831a17141933bc650fd7b18`  
		Last Modified: Fri, 22 Sep 2023 01:04:02 GMT  
		Size: 20.5 MB (20490525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15f15e2dbc4923ec9e595829141ff32e158e273447e00874ef2dbd2448853d3`  
		Last Modified: Fri, 22 Sep 2023 01:04:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9254f2e62e2d4d2468e3e2373ae08e6c9f92f97a362743a3ec9deb6819a557`  
		Last Modified: Fri, 22 Sep 2023 01:04:00 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206d77d234e482152347d128bb544ff4decf4101d50bcfe56fdbd2a5af3897b7`  
		Last Modified: Fri, 22 Sep 2023 01:04:00 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d9c9b7f9a18c981592ac79bbd6f632d64abc79fd43869b237c71591053077b`  
		Last Modified: Fri, 22 Sep 2023 01:04:01 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:b6a7e42f345dff5f62e872e4855a615228c99beb2f5a0fb1b67cfab9fb7f01bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1917144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ccd10447b3addc5d8558af4f04dc389811eef2e02c53ae3075efb769a14f1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd55ea93d659dba200cf888d2b1515b57775bb9a360879444a1c33ba9c4d722b`  
		Last Modified: Fri, 22 Sep 2023 01:04:01 GMT  
		Size: 1.9 MB (1855770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2873ed0d432ef9665c656c33b930f1aa16f1ae559c0707e0db9a038ca4a0a7f4`  
		Last Modified: Fri, 22 Sep 2023 01:04:00 GMT  
		Size: 61.4 KB (61374 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; arm64 variant v8

```console
$ docker pull rabbitmq@sha256:e00e8d2e4fece6569353c3630293b92bbb162c8fa3bf03dbc0e07c20a2798c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97238119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d43fd975468a7f6d9441301d49696f1ed170d49a4331737d6596a9d54a779e`
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:1bbce84bd2e78f3a0dc02fdf5f00ad586526e25fc0f91e3c56b3fec053f31b32`  
		Last Modified: Fri, 22 Sep 2023 02:30:26 GMT  
		Size: 20.5 MB (20483109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a3298067665499c0f49435a9e1a80a7e39de0b9df3c228fad4bcefab395c6a`  
		Last Modified: Fri, 22 Sep 2023 02:30:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1492fcad4cd3384df96fd4573ff942fb7eb73dab6028fa8c629a3a3cab72e394`  
		Last Modified: Fri, 22 Sep 2023 02:30:25 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe547c12b81dbb50269694410f24156482511b9922417b1a87b6f648712fcbc4`  
		Last Modified: Fri, 22 Sep 2023 02:30:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c10451ee789541730f09b612b7e36edc8f2aa50a3d1f13820d65a88279e4f`  
		Last Modified: Fri, 22 Sep 2023 02:30:26 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:83c40c14522ab9db91d646c54deba2f4b5f5431fcbc30b7f30ecd17f6cbb7ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8296ef2474dca1e081a09e677303935fd292d6c7314ba3d655a5e5bb3f46c`

```dockerfile
```

-	Layers:
	-	`sha256:64d07d7b60f07a54e93cc763baccebec28499e81c707701b13ae51c12df977ca`  
		Last Modified: Fri, 22 Sep 2023 02:30:25 GMT  
		Size: 1.9 MB (1854134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b1a9f2dfd482dd228795b8b97c7f7de4314889d9973d9000050635b0180fb1`  
		Last Modified: Fri, 22 Sep 2023 02:30:25 GMT  
		Size: 61.2 KB (61197 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; ppc64le

```console
$ docker pull rabbitmq@sha256:385a95ebabdf768125fe29b4724f24dff2c5ff31db39974680fc153b38590a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101683890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb0009328e5a8d1bf7e18fbd36aba58d1c4349af8ac0eb29cd22c59071d9999`
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:533a69876385757c30bc9f0a306e39828f2fc8f2a3cf6157edf05ce035c9884c`  
		Last Modified: Fri, 22 Sep 2023 02:13:16 GMT  
		Size: 20.5 MB (20507850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c788ccfb99446faa997c15a87e7342bba0dfd7ded508ac7390c7678bffbba9bd`  
		Last Modified: Fri, 22 Sep 2023 02:13:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb094608951c68bbbe5c82cbe278a9fddef9d1a5827d551cb8d50c6a9494d1`  
		Last Modified: Fri, 22 Sep 2023 02:13:15 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57b30c998667919dc05d2cf6661bd1225c462bd8108923c366b9c37afb313b`  
		Last Modified: Fri, 22 Sep 2023 02:13:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de830e115c61a5190fa846011f2a8f3d65465700bb1f0731cc147f2e9592bfa7`  
		Last Modified: Fri, 22 Sep 2023 02:13:16 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:2e58cf73a3e2adbab74ab723b55ed1d284b00341639ee8f8ce483fb8fc04ad8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1919702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761beb931dde5c9ba33c2a487ccb93ef7210ae607aca446cd82da8fdae788f4d`

```dockerfile
```

-	Layers:
	-	`sha256:7f2c68dc51b8bdd836872707e97d33cd4373348ec3a585adc7bc18ef33a395c8`  
		Last Modified: Fri, 22 Sep 2023 02:13:15 GMT  
		Size: 1.9 MB (1858459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff112a4150298437454f3e98ceb79c8c4505eab6994fa0621f6dbf73f1c45482`  
		Last Modified: Fri, 22 Sep 2023 02:13:14 GMT  
		Size: 61.2 KB (61243 bytes)  
		MIME: application/vnd.in-toto+json

### `rabbitmq:latest` - linux; s390x

```console
$ docker pull rabbitmq@sha256:f1e67985be3f9e6726a7ec31439c9086285d01e8073e39966b15764ad7ffd447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92496366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874490ea24c0dbb1843d703c031e6fc739ed37f310dfa38e9a52e756ce8e1e67`
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
RUN set -eux; 	ln -vsf /etc/ssl/certs /etc/ssl/private "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl"; 		ldconfig; 	sed -i.ORIG -e "/\.include.*fips/ s!.*!.include $OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf!" 		-e '/# fips =/s/.*/fips = fips_sect/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/openssl.cnf"; 	sed -i.ORIG -e '/^activate/s/^/#/' "$OPENSSL_INSTALL_PATH_PREFIX/etc/ssl/fipsmodule.cnf"; 	[ "$(command -v openssl)" = "$OPENSSL_INSTALL_PATH_PREFIX/bin/openssl" ]; 	openssl version; 	openssl version -d; 		erl -noshell -eval 'ok = crypto:start(), ok = io:format("~p~n~n~p~n~n", [crypto:supports(), ssl:versions()]), init:stop().'; 		groupadd --gid 999 --system rabbitmq; 	useradd --uid 999 --system --home-dir "$RABBITMQ_DATA_DIR" --gid rabbitmq rabbitmq; 	mkdir -p "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chown -fR rabbitmq:rabbitmq "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	chmod 1777 "$RABBITMQ_DATA_DIR" /etc/rabbitmq /etc/rabbitmq/conf.d /tmp/rabbitmq-ssl /var/log/rabbitmq; 	ln -sf "$RABBITMQ_DATA_DIR/.erlang.cookie" /root/.erlang.cookie # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_VERSION=3.12.5
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_PGP_KEY_ID=0x0A9AF2115F4687BD29803A206B73A36E6026DFCA
# Thu, 21 Sep 2023 11:05:32 GMT
ENV RABBITMQ_HOME=/opt/rabbitmq
# Thu, 21 Sep 2023 11:05:32 GMT
ENV PATH=/opt/rabbitmq/sbin:/opt/erlang/bin:/opt/openssl/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 11:05:32 GMT
RUN set -eux; 	export DEBIAN_FRONTEND=noninteractive; 	apt-get update; 	apt-get install --yes --no-install-recommends 		ca-certificates 		gosu 		tzdata 	; 	gosu nobody true; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --yes --no-install-recommends 		gnupg 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		RABBITMQ_SOURCE_URL="https://github.com/rabbitmq/rabbitmq-server/releases/download/v$RABBITMQ_VERSION/rabbitmq-server-generic-unix-latest-toolchain-$RABBITMQ_VERSION.tar.xz"; 	RABBITMQ_PATH="/usr/local/src/rabbitmq-$RABBITMQ_VERSION"; 		wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_SOURCE_URL.asc"; 	wget --progress dot:giga --output-document "$RABBITMQ_PATH.tar.xz" "$RABBITMQ_SOURCE_URL"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$RABBITMQ_PGP_KEY_ID"; 	gpg --batch --verify "$RABBITMQ_PATH.tar.xz.asc" "$RABBITMQ_PATH.tar.xz"; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$RABBITMQ_HOME"; 	tar --extract --file "$RABBITMQ_PATH.tar.xz" --directory "$RABBITMQ_HOME" --strip-components 1; 	rm -rf "$RABBITMQ_PATH"*; 	grep -qE '^SYS_PREFIX=\$\{RABBITMQ_HOME\}$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	sed -i 's/^SYS_PREFIX=.*$/SYS_PREFIX=/' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	grep -qE '^SYS_PREFIX=$' "$RABBITMQ_HOME/sbin/rabbitmq-defaults"; 	chown -R rabbitmq:rabbitmq "$RABBITMQ_HOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		[ ! -e "$RABBITMQ_DATA_DIR/.erlang.cookie" ]; 	gosu rabbitmq rabbitmqctl help; 	gosu rabbitmq rabbitmqctl list_ciphers; 	gosu rabbitmq rabbitmq-plugins list; 	rm "$RABBITMQ_DATA_DIR/.erlang.cookie" # buildkit
# Thu, 21 Sep 2023 11:05:32 GMT
RUN gosu rabbitmq rabbitmq-plugins enable --offline rabbitmq_prometheus # buildkit
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
	-	`sha256:c903fa79c4e94569ad19a659590214e84b466d0d4bdc3c421b10840ea5e59cdf`  
		Last Modified: Fri, 22 Sep 2023 01:34:24 GMT  
		Size: 20.5 MB (20541968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504ef7f1a983585525f57fee9661954947ec4647881471589ae743c0354a0db`  
		Last Modified: Fri, 22 Sep 2023 01:34:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9faae671d155d7edd8e5acfcecd1a197f2a7832aba253d54ea6ff37692a1697`  
		Last Modified: Fri, 22 Sep 2023 01:34:23 GMT  
		Size: 109.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c345e04db3ae4692a15f86340b17305fc4d2360cd1ca9c38e521cb0d8da20bc`  
		Last Modified: Fri, 22 Sep 2023 01:34:23 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcdf55894ec1af593cfb192452fdb368f53b9f7f3b35ba9148beb0d549597f`  
		Last Modified: Fri, 22 Sep 2023 01:34:24 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rabbitmq:latest` - unknown; unknown

```console
$ docker pull rabbitmq@sha256:d709d84f80f19c1c0eb1e52e90c0b66a956979b79ae79c1997d39bced85d3ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1915953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859eeef7c25eabbccd524a7ccadf9fa70e0b2a72197be3fc808a4fb33b11409e`

```dockerfile
```

-	Layers:
	-	`sha256:349b418ecd565d938d7a55db7f613406c697635f6e956a473b07430e697bb25c`  
		Last Modified: Fri, 22 Sep 2023 01:34:23 GMT  
		Size: 1.9 MB (1854766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8b9635fffcae3311e545b3ef6144106a89058a52dcce701c29f209814a1060`  
		Last Modified: Fri, 22 Sep 2023 01:34:22 GMT  
		Size: 61.2 KB (61187 bytes)  
		MIME: application/vnd.in-toto+json
