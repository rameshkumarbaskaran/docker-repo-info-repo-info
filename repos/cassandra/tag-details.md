<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `cassandra`

-	[`cassandra:3`](#cassandra3)
-	[`cassandra:3.0`](#cassandra30)
-	[`cassandra:3.0.25`](#cassandra3025)
-	[`cassandra:3.11`](#cassandra311)
-	[`cassandra:3.11.11`](#cassandra31111)
-	[`cassandra:4`](#cassandra4)
-	[`cassandra:4.0`](#cassandra40)
-	[`cassandra:4.0.1`](#cassandra401)
-	[`cassandra:latest`](#cassandralatest)

## `cassandra:3`

```console
$ docker pull cassandra@sha256:642a0e62c3d07451f2a380a592e6176f9d8f4b4a5d72df1a68a543d6842a4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3` - linux; amd64

```console
$ docker pull cassandra@sha256:1437973728ab8027aad3a037d232cdb196e0b0ff5328ec571524653c43696940
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138063205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de68729e5a00313b267b57e8c6493b91a91a12455cf95f81a1d0a614702924b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 16:51:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:51:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:51:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:51:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:51:51 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 16:51:51 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 16:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:56:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:56:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:56:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 16:56:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:56:08 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:56:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5670e09cae35e525f2497821afc5c8ab0d7c165fc828f5f68d3b0597eeb66`  
		Last Modified: Wed, 02 Feb 2022 03:02:24 GMT  
		Size: 41.8 MB (41773795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c787c85c7df15d6ae55cb0f3a97270f2aa896caff7d463152f2409c2ced7aceb`  
		Last Modified: Wed, 02 Feb 2022 03:02:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eaa6e4776d194899a38fcdc915b35e96fa2710fd0d1c41fcc3309d6f113170`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013a2453b8e4f657d19da821ec93cfafd86fa1037aa31afc05ba1a31213835a`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 9.3 MB (9301244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b23d2d6dd093a1b33bf6e6f5801a7aee494d8fe935c3cd0c9f068d2574fc7`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.3 MB (1320066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533347f30c75959103573f5b6cc534de95c2b0a9c2bb6c1b3496e0aad7f8e95b`  
		Last Modified: Wed, 02 Feb 2022 16:58:24 GMT  
		Size: 32.3 MB (32286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db3fcf8734a73d2b5a2ae4f8dd5c2e4f0cfc13d26bd6b2b23d0b602fbce114b`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de337715c6cbdc9d5b9c28c8cad352e44ab615cb6e42c92a143e71683811a0`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:88454a25e19974a5697595e3dc8fded78b998d6cb922c8b1dea8ee3afcc6e05a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135099305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa71a4ae2098165b58a917844c3b39117d64a3d0df1588c9642f35d0ca701eda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 10:10:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:11:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:17:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:17:04 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:17:05 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:17:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:17:07 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:17:08 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 10:17:09 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 10:20:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:20:19 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:20:21 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 10:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:20:23 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:20:24 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa60d6ad6ab0b8a49dad3a3c4fb5ed7f511c7af5551f18b190fbb633183e6d9`  
		Last Modified: Wed, 02 Feb 2022 05:06:55 GMT  
		Size: 40.8 MB (40769906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b7c09b7ae03343e3c1e143ec7d68f3a617c7874c33932c0c9335f9f88a1a9f`  
		Last Modified: Wed, 02 Feb 2022 05:06:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8637726ae83909f75c1e5e4ce250bc3a32573181629c7334b1a249402dfd8`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737e0750395a075b0641b27ae05d93cf99a9bc021d6e03294eb7fcc5d799116b`  
		Last Modified: Wed, 02 Feb 2022 10:25:18 GMT  
		Size: 9.3 MB (9333578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a056ad13c688b4546f1a35ba7245bc8d51403aa44b2640fca66563c9f7a1ff`  
		Last Modified: Wed, 02 Feb 2022 10:25:17 GMT  
		Size: 1.0 MB (1014716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926b336b8c4c676f008659612a55460340c6b20f7d7722348ef1c382de146a94`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 32.0 MB (32045533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72197c19142e14cdd5f7afbbd13ab1447fe627b9becbf780c8b658b869f2bd7d`  
		Last Modified: Wed, 02 Feb 2022 10:25:16 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d705f69b962574f53a24179b66af894011e63750d9d1c63cb1ad885e6f12c8`  
		Last Modified: Wed, 02 Feb 2022 10:25:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3` - linux; ppc64le

```console
$ docker pull cassandra@sha256:2b7182a5b78090a9d705b833a81d912be47a9d93a7428453bc33503015bfc4e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144684122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c9e45c9dc966c72ed3ff8d546dfdf0c71076b012a95f1c5d02394644b63c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:49:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:49:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 08:14:43 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:15:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:16:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:16:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:16:43 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:16:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:16:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:16:49 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 08:16:51 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 08:19:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:19:20 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:19:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 08:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:19:32 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:19:34 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b575a12a35b9ef08e2b14d4755693c4abe080a1fd9113db75d7afc8af0a2ea`  
		Last Modified: Wed, 02 Feb 2022 05:57:50 GMT  
		Size: 41.2 MB (41162367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e120f90c634c0ae856cefb05c0fff297a6e3df94751cd737baa714cd5fef8e`  
		Last Modified: Wed, 02 Feb 2022 05:57:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc08c17d6df581a26dd707205561b0881f5667486e551c48e34102730db68ff9`  
		Last Modified: Wed, 02 Feb 2022 08:22:47 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b54344a74021663d8159318acd7e20a07a0f33076557730548d7b7decd4df4`  
		Last Modified: Wed, 02 Feb 2022 08:22:46 GMT  
		Size: 10.1 MB (10062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c592658f2b6ab326cd47e8dcfb5c7ac02f3ae3195e9ee58e0a981d9fc23e9`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 MB (1240606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63a0031583380c3c552ad7428d4ae1b10d736e4e254b6a3a511fdc4111036c`  
		Last Modified: Wed, 02 Feb 2022 08:22:48 GMT  
		Size: 32.3 MB (32287327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbdb181293eda015102f3aa3a1c0d6d9be4a1756337bec84aac21905e189f39`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fb31357dd25b8ad968391c6e81309b6981d1f8c23a2241927be1182aeda50a`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.0`

```console
$ docker pull cassandra@sha256:4798e58bf522328856b4ac8752335435698832c967ad595c2b3db14e96f4ca8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.0` - linux; amd64

```console
$ docker pull cassandra@sha256:48729eeafc56d3e0e6dfe95726e35a9299a3e894737a079adeb6265963fefd89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132982043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f9f8b48e927d2fc9e5219991f9dd6fead9ec077b07016a8865226171658c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 16:51:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:51:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:51:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:51:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:56:22 GMT
ENV CASSANDRA_VERSION=3.0.25
# Wed, 02 Feb 2022 16:56:23 GMT
ENV CASSANDRA_SHA512=a425485a995a8dba998303e368af3cabc322a824f9e42c9e30c4890a0fe186a6bfa19d18b00f2e0336c3c100c6461f191a3e78e201cc91e99f8b80d8df803fdc
# Wed, 02 Feb 2022 16:57:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:57:33 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:57:33 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:57:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 16:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:57:34 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:57:34 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5670e09cae35e525f2497821afc5c8ab0d7c165fc828f5f68d3b0597eeb66`  
		Last Modified: Wed, 02 Feb 2022 03:02:24 GMT  
		Size: 41.8 MB (41773795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c787c85c7df15d6ae55cb0f3a97270f2aa896caff7d463152f2409c2ced7aceb`  
		Last Modified: Wed, 02 Feb 2022 03:02:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eaa6e4776d194899a38fcdc915b35e96fa2710fd0d1c41fcc3309d6f113170`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013a2453b8e4f657d19da821ec93cfafd86fa1037aa31afc05ba1a31213835a`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 9.3 MB (9301244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b23d2d6dd093a1b33bf6e6f5801a7aee494d8fe935c3cd0c9f068d2574fc7`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.3 MB (1320066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbdc4d65b75a2e267a919b2b9bf3898ee6069213be94623238d9e133677c6f7`  
		Last Modified: Wed, 02 Feb 2022 16:58:39 GMT  
		Size: 27.2 MB (27204925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c7db7cb1ce9c3726c88af6d3c4d3c7b86f900fe9db53e473a655e7e469b98`  
		Last Modified: Wed, 02 Feb 2022 16:58:37 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacd117e5dae3dc209a78be02c8dd87a46fd0c229f37c536a7677dcdf10ea2b`  
		Last Modified: Wed, 02 Feb 2022 16:58:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:c14fa23d630c1de11a21e8e6aeb3ab55d4b6d75d50793799997b7786e182155d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130017671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa8c87110d535b1e9f9397271ea1026e00142a2b1283136b2e3ee9e55cedc93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 10:10:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:11:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:17:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:17:04 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:17:05 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:17:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:17:07 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:20:37 GMT
ENV CASSANDRA_VERSION=3.0.25
# Wed, 02 Feb 2022 10:20:38 GMT
ENV CASSANDRA_SHA512=a425485a995a8dba998303e368af3cabc322a824f9e42c9e30c4890a0fe186a6bfa19d18b00f2e0336c3c100c6461f191a3e78e201cc91e99f8b80d8df803fdc
# Wed, 02 Feb 2022 10:24:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:24:17 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:24:19 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:24:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 10:24:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:24:21 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:24:22 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa60d6ad6ab0b8a49dad3a3c4fb5ed7f511c7af5551f18b190fbb633183e6d9`  
		Last Modified: Wed, 02 Feb 2022 05:06:55 GMT  
		Size: 40.8 MB (40769906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b7c09b7ae03343e3c1e143ec7d68f3a617c7874c33932c0c9335f9f88a1a9f`  
		Last Modified: Wed, 02 Feb 2022 05:06:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8637726ae83909f75c1e5e4ce250bc3a32573181629c7334b1a249402dfd8`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737e0750395a075b0641b27ae05d93cf99a9bc021d6e03294eb7fcc5d799116b`  
		Last Modified: Wed, 02 Feb 2022 10:25:18 GMT  
		Size: 9.3 MB (9333578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a056ad13c688b4546f1a35ba7245bc8d51403aa44b2640fca66563c9f7a1ff`  
		Last Modified: Wed, 02 Feb 2022 10:25:17 GMT  
		Size: 1.0 MB (1014716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cee746e1a196a6ebd28af0d2d095ea8fd8307b20baf9254953992f9668a2c`  
		Last Modified: Wed, 02 Feb 2022 10:25:41 GMT  
		Size: 27.0 MB (26963898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db485e3b9926dae6add64ceba0ce4a18a8b47f3e8f5385cb8411dc1ca91dc1f`  
		Last Modified: Wed, 02 Feb 2022 10:25:39 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd26c074b3149ac57dbdb54429022367a306561e31ad1352355d1c30f147cf2`  
		Last Modified: Wed, 02 Feb 2022 10:25:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:5d3200142020c83a86347e06b64b69c4b8723ebec06cbc796d8f5706bd4f89b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139602943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2ab1127c1ec7afe7df3cb7f53452419f44c802272be72aa795e643f42cf48a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:49:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:49:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 08:14:43 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:15:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:16:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:16:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:16:43 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:16:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:16:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:19:49 GMT
ENV CASSANDRA_VERSION=3.0.25
# Wed, 02 Feb 2022 08:19:51 GMT
ENV CASSANDRA_SHA512=a425485a995a8dba998303e368af3cabc322a824f9e42c9e30c4890a0fe186a6bfa19d18b00f2e0336c3c100c6461f191a3e78e201cc91e99f8b80d8df803fdc
# Wed, 02 Feb 2022 08:21:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:21:30 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:21:31 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:21:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 08:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:21:42 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:21:46 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b575a12a35b9ef08e2b14d4755693c4abe080a1fd9113db75d7afc8af0a2ea`  
		Last Modified: Wed, 02 Feb 2022 05:57:50 GMT  
		Size: 41.2 MB (41162367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e120f90c634c0ae856cefb05c0fff297a6e3df94751cd737baa714cd5fef8e`  
		Last Modified: Wed, 02 Feb 2022 05:57:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc08c17d6df581a26dd707205561b0881f5667486e551c48e34102730db68ff9`  
		Last Modified: Wed, 02 Feb 2022 08:22:47 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b54344a74021663d8159318acd7e20a07a0f33076557730548d7b7decd4df4`  
		Last Modified: Wed, 02 Feb 2022 08:22:46 GMT  
		Size: 10.1 MB (10062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c592658f2b6ab326cd47e8dcfb5c7ac02f3ae3195e9ee58e0a981d9fc23e9`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 MB (1240606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d12596598fe1c479b4228183c279a33215b57155177c931172f4244ec850a`  
		Last Modified: Wed, 02 Feb 2022 08:23:06 GMT  
		Size: 27.2 MB (27206146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990deae7a4abddfa1ac8d2c00c7434f524e7560e6060c9faf8511c9c6e7acb94`  
		Last Modified: Wed, 02 Feb 2022 08:23:03 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d4430a88f32adcde936fa5715842ed869ca45f3016b6115f4a88191282bd7a`  
		Last Modified: Wed, 02 Feb 2022 08:23:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.0.25`

```console
$ docker pull cassandra@sha256:4798e58bf522328856b4ac8752335435698832c967ad595c2b3db14e96f4ca8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.0.25` - linux; amd64

```console
$ docker pull cassandra@sha256:48729eeafc56d3e0e6dfe95726e35a9299a3e894737a079adeb6265963fefd89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132982043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f9f8b48e927d2fc9e5219991f9dd6fead9ec077b07016a8865226171658c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 16:51:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:51:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:51:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:51:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:56:22 GMT
ENV CASSANDRA_VERSION=3.0.25
# Wed, 02 Feb 2022 16:56:23 GMT
ENV CASSANDRA_SHA512=a425485a995a8dba998303e368af3cabc322a824f9e42c9e30c4890a0fe186a6bfa19d18b00f2e0336c3c100c6461f191a3e78e201cc91e99f8b80d8df803fdc
# Wed, 02 Feb 2022 16:57:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:57:33 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:57:33 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:57:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 16:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:57:34 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:57:34 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5670e09cae35e525f2497821afc5c8ab0d7c165fc828f5f68d3b0597eeb66`  
		Last Modified: Wed, 02 Feb 2022 03:02:24 GMT  
		Size: 41.8 MB (41773795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c787c85c7df15d6ae55cb0f3a97270f2aa896caff7d463152f2409c2ced7aceb`  
		Last Modified: Wed, 02 Feb 2022 03:02:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eaa6e4776d194899a38fcdc915b35e96fa2710fd0d1c41fcc3309d6f113170`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013a2453b8e4f657d19da821ec93cfafd86fa1037aa31afc05ba1a31213835a`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 9.3 MB (9301244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b23d2d6dd093a1b33bf6e6f5801a7aee494d8fe935c3cd0c9f068d2574fc7`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.3 MB (1320066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbdc4d65b75a2e267a919b2b9bf3898ee6069213be94623238d9e133677c6f7`  
		Last Modified: Wed, 02 Feb 2022 16:58:39 GMT  
		Size: 27.2 MB (27204925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c7db7cb1ce9c3726c88af6d3c4d3c7b86f900fe9db53e473a655e7e469b98`  
		Last Modified: Wed, 02 Feb 2022 16:58:37 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacd117e5dae3dc209a78be02c8dd87a46fd0c229f37c536a7677dcdf10ea2b`  
		Last Modified: Wed, 02 Feb 2022 16:58:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0.25` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:c14fa23d630c1de11a21e8e6aeb3ab55d4b6d75d50793799997b7786e182155d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130017671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa8c87110d535b1e9f9397271ea1026e00142a2b1283136b2e3ee9e55cedc93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 10:10:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:11:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:17:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:17:04 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:17:05 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:17:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:17:07 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:20:37 GMT
ENV CASSANDRA_VERSION=3.0.25
# Wed, 02 Feb 2022 10:20:38 GMT
ENV CASSANDRA_SHA512=a425485a995a8dba998303e368af3cabc322a824f9e42c9e30c4890a0fe186a6bfa19d18b00f2e0336c3c100c6461f191a3e78e201cc91e99f8b80d8df803fdc
# Wed, 02 Feb 2022 10:24:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:24:17 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:24:19 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:24:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 10:24:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:24:21 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:24:22 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa60d6ad6ab0b8a49dad3a3c4fb5ed7f511c7af5551f18b190fbb633183e6d9`  
		Last Modified: Wed, 02 Feb 2022 05:06:55 GMT  
		Size: 40.8 MB (40769906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b7c09b7ae03343e3c1e143ec7d68f3a617c7874c33932c0c9335f9f88a1a9f`  
		Last Modified: Wed, 02 Feb 2022 05:06:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8637726ae83909f75c1e5e4ce250bc3a32573181629c7334b1a249402dfd8`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737e0750395a075b0641b27ae05d93cf99a9bc021d6e03294eb7fcc5d799116b`  
		Last Modified: Wed, 02 Feb 2022 10:25:18 GMT  
		Size: 9.3 MB (9333578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a056ad13c688b4546f1a35ba7245bc8d51403aa44b2640fca66563c9f7a1ff`  
		Last Modified: Wed, 02 Feb 2022 10:25:17 GMT  
		Size: 1.0 MB (1014716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cee746e1a196a6ebd28af0d2d095ea8fd8307b20baf9254953992f9668a2c`  
		Last Modified: Wed, 02 Feb 2022 10:25:41 GMT  
		Size: 27.0 MB (26963898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db485e3b9926dae6add64ceba0ce4a18a8b47f3e8f5385cb8411dc1ca91dc1f`  
		Last Modified: Wed, 02 Feb 2022 10:25:39 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd26c074b3149ac57dbdb54429022367a306561e31ad1352355d1c30f147cf2`  
		Last Modified: Wed, 02 Feb 2022 10:25:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0.25` - linux; ppc64le

```console
$ docker pull cassandra@sha256:5d3200142020c83a86347e06b64b69c4b8723ebec06cbc796d8f5706bd4f89b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139602943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2ab1127c1ec7afe7df3cb7f53452419f44c802272be72aa795e643f42cf48a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:49:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:49:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 08:14:43 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:15:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:16:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:16:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:16:43 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:16:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:16:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:19:49 GMT
ENV CASSANDRA_VERSION=3.0.25
# Wed, 02 Feb 2022 08:19:51 GMT
ENV CASSANDRA_SHA512=a425485a995a8dba998303e368af3cabc322a824f9e42c9e30c4890a0fe186a6bfa19d18b00f2e0336c3c100c6461f191a3e78e201cc91e99f8b80d8df803fdc
# Wed, 02 Feb 2022 08:21:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:21:30 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:21:31 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:21:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 08:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:21:42 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:21:46 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b575a12a35b9ef08e2b14d4755693c4abe080a1fd9113db75d7afc8af0a2ea`  
		Last Modified: Wed, 02 Feb 2022 05:57:50 GMT  
		Size: 41.2 MB (41162367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e120f90c634c0ae856cefb05c0fff297a6e3df94751cd737baa714cd5fef8e`  
		Last Modified: Wed, 02 Feb 2022 05:57:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc08c17d6df581a26dd707205561b0881f5667486e551c48e34102730db68ff9`  
		Last Modified: Wed, 02 Feb 2022 08:22:47 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b54344a74021663d8159318acd7e20a07a0f33076557730548d7b7decd4df4`  
		Last Modified: Wed, 02 Feb 2022 08:22:46 GMT  
		Size: 10.1 MB (10062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c592658f2b6ab326cd47e8dcfb5c7ac02f3ae3195e9ee58e0a981d9fc23e9`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 MB (1240606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d12596598fe1c479b4228183c279a33215b57155177c931172f4244ec850a`  
		Last Modified: Wed, 02 Feb 2022 08:23:06 GMT  
		Size: 27.2 MB (27206146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990deae7a4abddfa1ac8d2c00c7434f524e7560e6060c9faf8511c9c6e7acb94`  
		Last Modified: Wed, 02 Feb 2022 08:23:03 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d4430a88f32adcde936fa5715842ed869ca45f3016b6115f4a88191282bd7a`  
		Last Modified: Wed, 02 Feb 2022 08:23:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.11`

```console
$ docker pull cassandra@sha256:642a0e62c3d07451f2a380a592e6176f9d8f4b4a5d72df1a68a543d6842a4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.11` - linux; amd64

```console
$ docker pull cassandra@sha256:1437973728ab8027aad3a037d232cdb196e0b0ff5328ec571524653c43696940
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138063205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de68729e5a00313b267b57e8c6493b91a91a12455cf95f81a1d0a614702924b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 16:51:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:51:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:51:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:51:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:51:51 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 16:51:51 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 16:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:56:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:56:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:56:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 16:56:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:56:08 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:56:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5670e09cae35e525f2497821afc5c8ab0d7c165fc828f5f68d3b0597eeb66`  
		Last Modified: Wed, 02 Feb 2022 03:02:24 GMT  
		Size: 41.8 MB (41773795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c787c85c7df15d6ae55cb0f3a97270f2aa896caff7d463152f2409c2ced7aceb`  
		Last Modified: Wed, 02 Feb 2022 03:02:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eaa6e4776d194899a38fcdc915b35e96fa2710fd0d1c41fcc3309d6f113170`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013a2453b8e4f657d19da821ec93cfafd86fa1037aa31afc05ba1a31213835a`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 9.3 MB (9301244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b23d2d6dd093a1b33bf6e6f5801a7aee494d8fe935c3cd0c9f068d2574fc7`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.3 MB (1320066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533347f30c75959103573f5b6cc534de95c2b0a9c2bb6c1b3496e0aad7f8e95b`  
		Last Modified: Wed, 02 Feb 2022 16:58:24 GMT  
		Size: 32.3 MB (32286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db3fcf8734a73d2b5a2ae4f8dd5c2e4f0cfc13d26bd6b2b23d0b602fbce114b`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de337715c6cbdc9d5b9c28c8cad352e44ab615cb6e42c92a143e71683811a0`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:88454a25e19974a5697595e3dc8fded78b998d6cb922c8b1dea8ee3afcc6e05a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135099305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa71a4ae2098165b58a917844c3b39117d64a3d0df1588c9642f35d0ca701eda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 10:10:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:11:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:17:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:17:04 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:17:05 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:17:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:17:07 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:17:08 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 10:17:09 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 10:20:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:20:19 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:20:21 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 10:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:20:23 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:20:24 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa60d6ad6ab0b8a49dad3a3c4fb5ed7f511c7af5551f18b190fbb633183e6d9`  
		Last Modified: Wed, 02 Feb 2022 05:06:55 GMT  
		Size: 40.8 MB (40769906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b7c09b7ae03343e3c1e143ec7d68f3a617c7874c33932c0c9335f9f88a1a9f`  
		Last Modified: Wed, 02 Feb 2022 05:06:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8637726ae83909f75c1e5e4ce250bc3a32573181629c7334b1a249402dfd8`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737e0750395a075b0641b27ae05d93cf99a9bc021d6e03294eb7fcc5d799116b`  
		Last Modified: Wed, 02 Feb 2022 10:25:18 GMT  
		Size: 9.3 MB (9333578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a056ad13c688b4546f1a35ba7245bc8d51403aa44b2640fca66563c9f7a1ff`  
		Last Modified: Wed, 02 Feb 2022 10:25:17 GMT  
		Size: 1.0 MB (1014716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926b336b8c4c676f008659612a55460340c6b20f7d7722348ef1c382de146a94`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 32.0 MB (32045533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72197c19142e14cdd5f7afbbd13ab1447fe627b9becbf780c8b658b869f2bd7d`  
		Last Modified: Wed, 02 Feb 2022 10:25:16 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d705f69b962574f53a24179b66af894011e63750d9d1c63cb1ad885e6f12c8`  
		Last Modified: Wed, 02 Feb 2022 10:25:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11` - linux; ppc64le

```console
$ docker pull cassandra@sha256:2b7182a5b78090a9d705b833a81d912be47a9d93a7428453bc33503015bfc4e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144684122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c9e45c9dc966c72ed3ff8d546dfdf0c71076b012a95f1c5d02394644b63c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:49:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:49:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 08:14:43 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:15:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:16:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:16:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:16:43 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:16:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:16:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:16:49 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 08:16:51 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 08:19:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:19:20 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:19:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 08:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:19:32 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:19:34 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b575a12a35b9ef08e2b14d4755693c4abe080a1fd9113db75d7afc8af0a2ea`  
		Last Modified: Wed, 02 Feb 2022 05:57:50 GMT  
		Size: 41.2 MB (41162367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e120f90c634c0ae856cefb05c0fff297a6e3df94751cd737baa714cd5fef8e`  
		Last Modified: Wed, 02 Feb 2022 05:57:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc08c17d6df581a26dd707205561b0881f5667486e551c48e34102730db68ff9`  
		Last Modified: Wed, 02 Feb 2022 08:22:47 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b54344a74021663d8159318acd7e20a07a0f33076557730548d7b7decd4df4`  
		Last Modified: Wed, 02 Feb 2022 08:22:46 GMT  
		Size: 10.1 MB (10062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c592658f2b6ab326cd47e8dcfb5c7ac02f3ae3195e9ee58e0a981d9fc23e9`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 MB (1240606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63a0031583380c3c552ad7428d4ae1b10d736e4e254b6a3a511fdc4111036c`  
		Last Modified: Wed, 02 Feb 2022 08:22:48 GMT  
		Size: 32.3 MB (32287327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbdb181293eda015102f3aa3a1c0d6d9be4a1756337bec84aac21905e189f39`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fb31357dd25b8ad968391c6e81309b6981d1f8c23a2241927be1182aeda50a`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.11.11`

```console
$ docker pull cassandra@sha256:642a0e62c3d07451f2a380a592e6176f9d8f4b4a5d72df1a68a543d6842a4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.11.11` - linux; amd64

```console
$ docker pull cassandra@sha256:1437973728ab8027aad3a037d232cdb196e0b0ff5328ec571524653c43696940
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138063205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de68729e5a00313b267b57e8c6493b91a91a12455cf95f81a1d0a614702924b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 16:51:30 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:51:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:51:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:51:50 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:51:51 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:51:51 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 16:51:51 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 16:56:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:56:07 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:56:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:56:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 16:56:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:56:08 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:56:08 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5670e09cae35e525f2497821afc5c8ab0d7c165fc828f5f68d3b0597eeb66`  
		Last Modified: Wed, 02 Feb 2022 03:02:24 GMT  
		Size: 41.8 MB (41773795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c787c85c7df15d6ae55cb0f3a97270f2aa896caff7d463152f2409c2ced7aceb`  
		Last Modified: Wed, 02 Feb 2022 03:02:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eaa6e4776d194899a38fcdc915b35e96fa2710fd0d1c41fcc3309d6f113170`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013a2453b8e4f657d19da821ec93cfafd86fa1037aa31afc05ba1a31213835a`  
		Last Modified: Wed, 02 Feb 2022 16:58:23 GMT  
		Size: 9.3 MB (9301244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838b23d2d6dd093a1b33bf6e6f5801a7aee494d8fe935c3cd0c9f068d2574fc7`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.3 MB (1320066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533347f30c75959103573f5b6cc534de95c2b0a9c2bb6c1b3496e0aad7f8e95b`  
		Last Modified: Wed, 02 Feb 2022 16:58:24 GMT  
		Size: 32.3 MB (32286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db3fcf8734a73d2b5a2ae4f8dd5c2e4f0cfc13d26bd6b2b23d0b602fbce114b`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de337715c6cbdc9d5b9c28c8cad352e44ab615cb6e42c92a143e71683811a0`  
		Last Modified: Wed, 02 Feb 2022 16:58:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11.11` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:88454a25e19974a5697595e3dc8fded78b998d6cb922c8b1dea8ee3afcc6e05a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135099305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa71a4ae2098165b58a917844c3b39117d64a3d0df1588c9642f35d0ca701eda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 10:10:38 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:11:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:17:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:17:04 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:17:05 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:17:06 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:17:07 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:17:08 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 10:17:09 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 10:20:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:20:19 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:20:21 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 10:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:20:23 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:20:24 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa60d6ad6ab0b8a49dad3a3c4fb5ed7f511c7af5551f18b190fbb633183e6d9`  
		Last Modified: Wed, 02 Feb 2022 05:06:55 GMT  
		Size: 40.8 MB (40769906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b7c09b7ae03343e3c1e143ec7d68f3a617c7874c33932c0c9335f9f88a1a9f`  
		Last Modified: Wed, 02 Feb 2022 05:06:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8637726ae83909f75c1e5e4ce250bc3a32573181629c7334b1a249402dfd8`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737e0750395a075b0641b27ae05d93cf99a9bc021d6e03294eb7fcc5d799116b`  
		Last Modified: Wed, 02 Feb 2022 10:25:18 GMT  
		Size: 9.3 MB (9333578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a056ad13c688b4546f1a35ba7245bc8d51403aa44b2640fca66563c9f7a1ff`  
		Last Modified: Wed, 02 Feb 2022 10:25:17 GMT  
		Size: 1.0 MB (1014716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926b336b8c4c676f008659612a55460340c6b20f7d7722348ef1c382de146a94`  
		Last Modified: Wed, 02 Feb 2022 10:25:19 GMT  
		Size: 32.0 MB (32045533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72197c19142e14cdd5f7afbbd13ab1447fe627b9becbf780c8b658b869f2bd7d`  
		Last Modified: Wed, 02 Feb 2022 10:25:16 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d705f69b962574f53a24179b66af894011e63750d9d1c63cb1ad885e6f12c8`  
		Last Modified: Wed, 02 Feb 2022 10:25:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11.11` - linux; ppc64le

```console
$ docker pull cassandra@sha256:2b7182a5b78090a9d705b833a81d912be47a9d93a7428453bc33503015bfc4e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144684122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c9e45c9dc966c72ed3ff8d546dfdf0c71076b012a95f1c5d02394644b63c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:49:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:49:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 08:14:43 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:15:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:16:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:16:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:16:43 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:16:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:16:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:16:49 GMT
ENV CASSANDRA_VERSION=3.11.11
# Wed, 02 Feb 2022 08:16:51 GMT
ENV CASSANDRA_SHA512=5a7dc4237c9f43526b63cae62f04d73ec60f28e86ee1dd4bd4aaa55d2063d74fe842e015f7f68512db7deadbe52cab37417341183a716c191035463992e42d37
# Wed, 02 Feb 2022 08:19:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:19:20 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:19:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Feb 2022 08:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:19:32 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:19:34 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b575a12a35b9ef08e2b14d4755693c4abe080a1fd9113db75d7afc8af0a2ea`  
		Last Modified: Wed, 02 Feb 2022 05:57:50 GMT  
		Size: 41.2 MB (41162367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e120f90c634c0ae856cefb05c0fff297a6e3df94751cd737baa714cd5fef8e`  
		Last Modified: Wed, 02 Feb 2022 05:57:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc08c17d6df581a26dd707205561b0881f5667486e551c48e34102730db68ff9`  
		Last Modified: Wed, 02 Feb 2022 08:22:47 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b54344a74021663d8159318acd7e20a07a0f33076557730548d7b7decd4df4`  
		Last Modified: Wed, 02 Feb 2022 08:22:46 GMT  
		Size: 10.1 MB (10062580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26c592658f2b6ab326cd47e8dcfb5c7ac02f3ae3195e9ee58e0a981d9fc23e9`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 MB (1240606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63a0031583380c3c552ad7428d4ae1b10d736e4e254b6a3a511fdc4111036c`  
		Last Modified: Wed, 02 Feb 2022 08:22:48 GMT  
		Size: 32.3 MB (32287327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbdb181293eda015102f3aa3a1c0d6d9be4a1756337bec84aac21905e189f39`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fb31357dd25b8ad968391c6e81309b6981d1f8c23a2241927be1182aeda50a`  
		Last Modified: Wed, 02 Feb 2022 08:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:4`

```console
$ docker pull cassandra@sha256:d7afc180e4c22d87b6cb22da834e18d0b6f027271b8600aad64543cdb426785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:4` - linux; amd64

```console
$ docker pull cassandra@sha256:1e7e49947237f085f318ace1a887129452c78478b9e805edd20986b71221b030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149940985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d320f7a08ead778ced2db14f319a6ee13f3a9b0a60ddd64e36cf3097d323414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:59:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:59:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:59:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 16:44:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:44:21 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:44:40 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:44:41 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 16:51:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:51:16 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:51:17 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:51:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:51:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:51:17 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585a8f8fd99d708129717ae5fdac2d9fe803a5fee3291ff479f8dc04db42494`  
		Last Modified: Wed, 02 Feb 2022 03:03:11 GMT  
		Size: 43.2 MB (43230362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f03a4fb8d3d6c8106ee5f1bef091485bf8ae217d5c0a0b0e09f5c0e1a442f`  
		Last Modified: Wed, 02 Feb 2022 03:03:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326346e327fa4e5f6f21fa84ce290ff67d5a96a5abbe69545e23e3794ebd36e0`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8681365c18e7ec32b6c3fa74be141c9d3e037502d30c4c275ffc5ded71c33a5`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 2.2 MB (2160209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d006d3ddcdb9e800b59407661a1b9f6075daa25e786f35c942dd2ba1ca6698`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 1.3 MB (1315265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf35801b2911264b4ad225dfdf08adfcee3a6f9d471b6d28bdb2aa394b47eea`  
		Last Modified: Wed, 02 Feb 2022 16:58:02 GMT  
		Size: 49.9 MB (49853248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2b1ccdbb02b0b617add116ca538bfd44e437609503a9aaa639652247789bc`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:a0bd1396a60ea5458cc694bad6fc5a13a4e72021db87e9aa340d364c104c0b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142048722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1470f92753ee6db83bde063895e8746612189d93be7c7c9b38bd5899e913de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:48:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:48:04 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:49:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:49:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:11:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 05:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 05:12:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 05:12:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:12:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 05:12:34 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 05:12:35 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 05:14:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 05:14:28 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 05:14:29 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 05:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 05:14:30 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 05:14:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca45b223849013a5db7d5850e0832f4aac669b33c69f09d9d74f6d6ae56a91d8`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 23.1 MB (23072061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605123915fece369da5778c9391348661f9ac3f37a8d4e3663c9c282ef486789`  
		Last Modified: Wed, 02 Feb 2022 02:55:57 GMT  
		Size: 41.9 MB (41850725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b512710f7691986f4b2e05d64e27b40ab28ad601c130c9d986ca42d03dcb2`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6686325283874be8268a1d58c6f2cdd07169c9ae2dd498bd863a1f46f4d2e39`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09aa4e0ae0d936e6d97ef85564085e1f0225bcd528b5e007034447cb6aba452`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.9 MB (1936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311e92d9b18c801f8b243c4df37876cf9a80d5550b52276fd3674360969633f7`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.3 MB (1269195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346900b2d9ff04a141f73dc72134e3f7b534f42245a533bebe0089422c9189d`  
		Last Modified: Wed, 02 Feb 2022 05:15:19 GMT  
		Size: 49.9 MB (49854744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8f088b8e4767142541c94cad57124da4600532a71c23b391b81e09a5377057`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:3e6d95c4bea95e2aa2666762b113ea1f645fdaa1abbd49d95172d6853d00a1c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146259958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8203ffe1f6315a574658a9e4cf62400e55f7c9c60a541bdcac6262398d146144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:34 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:03:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:03:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 10:08:26 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:08:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:08:36 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:08:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:08:57 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:08:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:08:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:09:00 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:09:01 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 10:09:02 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 10:10:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:10:21 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:10:23 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:10:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:10:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:10:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6151ca955d4b7fb01dfd3c4470cc07f8484a7de594e6028377da2392b0b9d`  
		Last Modified: Wed, 02 Feb 2022 05:07:49 GMT  
		Size: 41.6 MB (41572184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5b05b981cfd36cda3c95e6c1b623132675dfd8e918bc928fb89bffc419f28`  
		Last Modified: Wed, 02 Feb 2022 05:07:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6f39fa98274f1fecd9e8aa58ab5f79fc37e9a3ab4e9a794c92e07d3473dc3c`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c2c1c85f859360b344bc7c141621d78a13c9e85b0595fab8cf5e1b1f545bf`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 2.1 MB (2129228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5758a9e04b46feeec48da5b86e2183ece68e0580f143c1ac9c99e613b22ae`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 1.0 MB (1010345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e282bb069bfd10203918d28975d264c20f327d5a587da48bc0dd979ccc2a3fd`  
		Last Modified: Wed, 02 Feb 2022 10:25:00 GMT  
		Size: 49.6 MB (49612751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28625866fc351d08f4264f93c6c4b7df54a6471924074cc846d1b894c55aa9f8`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4` - linux; ppc64le

```console
$ docker pull cassandra@sha256:7c6832e02858bc32ec421d7f7908c8cc66c6f6bd20d92beeb861503a1c84e071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152185613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbeb84ea6ea113e9d87fc7b3be1a9e2c216a3d5c8d1a735214ac3c310962ab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:50:12 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:51:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:51:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 08:10:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:10:41 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:11:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:11:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:12:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:12:05 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:12:08 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:12:09 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 08:12:13 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 08:14:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:14:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:14:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:14:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:14:19 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ac27cb36bb8dd24defb16aca611d9a310ff50291b151fb1179fbb18e234e7`  
		Last Modified: Wed, 02 Feb 2022 05:58:45 GMT  
		Size: 38.6 MB (38641073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68febafb066e63efbfcc3c94c15fa0fdf31cc82e9682488ffc94ebe35434214a`  
		Last Modified: Wed, 02 Feb 2022 05:58:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6e3b1cfb67074ab7c5b4d350b0178b8f48d60ead234524bb3ca542217b7d7`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf82212b800515952bf89074aae7b2f5c9ffcfa683e50645deaa10a0b7bdd3b1`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 2.5 MB (2522832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752fad4e0201c301b4b52b929824591a1f22aa3ea2c8dd9112850f3276273f4e`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.2 MB (1236123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d297ef992ea410c0e80d1ddc3b10797a824ecea29c33c903058bd7cd340291`  
		Last Modified: Wed, 02 Feb 2022 08:22:25 GMT  
		Size: 49.9 MB (49854452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a6965d6b28ca7b375926fdd202ecba41292a65c41837e626e08c67f84d223f`  
		Last Modified: Wed, 02 Feb 2022 08:22:20 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:4.0`

```console
$ docker pull cassandra@sha256:d7afc180e4c22d87b6cb22da834e18d0b6f027271b8600aad64543cdb426785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:4.0` - linux; amd64

```console
$ docker pull cassandra@sha256:1e7e49947237f085f318ace1a887129452c78478b9e805edd20986b71221b030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149940985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d320f7a08ead778ced2db14f319a6ee13f3a9b0a60ddd64e36cf3097d323414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:59:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:59:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:59:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 16:44:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:44:21 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:44:40 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:44:41 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 16:51:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:51:16 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:51:17 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:51:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:51:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:51:17 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585a8f8fd99d708129717ae5fdac2d9fe803a5fee3291ff479f8dc04db42494`  
		Last Modified: Wed, 02 Feb 2022 03:03:11 GMT  
		Size: 43.2 MB (43230362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f03a4fb8d3d6c8106ee5f1bef091485bf8ae217d5c0a0b0e09f5c0e1a442f`  
		Last Modified: Wed, 02 Feb 2022 03:03:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326346e327fa4e5f6f21fa84ce290ff67d5a96a5abbe69545e23e3794ebd36e0`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8681365c18e7ec32b6c3fa74be141c9d3e037502d30c4c275ffc5ded71c33a5`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 2.2 MB (2160209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d006d3ddcdb9e800b59407661a1b9f6075daa25e786f35c942dd2ba1ca6698`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 1.3 MB (1315265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf35801b2911264b4ad225dfdf08adfcee3a6f9d471b6d28bdb2aa394b47eea`  
		Last Modified: Wed, 02 Feb 2022 16:58:02 GMT  
		Size: 49.9 MB (49853248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2b1ccdbb02b0b617add116ca538bfd44e437609503a9aaa639652247789bc`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:a0bd1396a60ea5458cc694bad6fc5a13a4e72021db87e9aa340d364c104c0b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142048722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1470f92753ee6db83bde063895e8746612189d93be7c7c9b38bd5899e913de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:48:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:48:04 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:49:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:49:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:11:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 05:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 05:12:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 05:12:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:12:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 05:12:34 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 05:12:35 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 05:14:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 05:14:28 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 05:14:29 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 05:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 05:14:30 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 05:14:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca45b223849013a5db7d5850e0832f4aac669b33c69f09d9d74f6d6ae56a91d8`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 23.1 MB (23072061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605123915fece369da5778c9391348661f9ac3f37a8d4e3663c9c282ef486789`  
		Last Modified: Wed, 02 Feb 2022 02:55:57 GMT  
		Size: 41.9 MB (41850725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b512710f7691986f4b2e05d64e27b40ab28ad601c130c9d986ca42d03dcb2`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6686325283874be8268a1d58c6f2cdd07169c9ae2dd498bd863a1f46f4d2e39`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09aa4e0ae0d936e6d97ef85564085e1f0225bcd528b5e007034447cb6aba452`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.9 MB (1936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311e92d9b18c801f8b243c4df37876cf9a80d5550b52276fd3674360969633f7`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.3 MB (1269195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346900b2d9ff04a141f73dc72134e3f7b534f42245a533bebe0089422c9189d`  
		Last Modified: Wed, 02 Feb 2022 05:15:19 GMT  
		Size: 49.9 MB (49854744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8f088b8e4767142541c94cad57124da4600532a71c23b391b81e09a5377057`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:3e6d95c4bea95e2aa2666762b113ea1f645fdaa1abbd49d95172d6853d00a1c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146259958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8203ffe1f6315a574658a9e4cf62400e55f7c9c60a541bdcac6262398d146144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:34 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:03:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:03:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 10:08:26 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:08:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:08:36 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:08:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:08:57 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:08:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:08:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:09:00 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:09:01 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 10:09:02 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 10:10:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:10:21 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:10:23 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:10:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:10:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:10:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6151ca955d4b7fb01dfd3c4470cc07f8484a7de594e6028377da2392b0b9d`  
		Last Modified: Wed, 02 Feb 2022 05:07:49 GMT  
		Size: 41.6 MB (41572184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5b05b981cfd36cda3c95e6c1b623132675dfd8e918bc928fb89bffc419f28`  
		Last Modified: Wed, 02 Feb 2022 05:07:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6f39fa98274f1fecd9e8aa58ab5f79fc37e9a3ab4e9a794c92e07d3473dc3c`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c2c1c85f859360b344bc7c141621d78a13c9e85b0595fab8cf5e1b1f545bf`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 2.1 MB (2129228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5758a9e04b46feeec48da5b86e2183ece68e0580f143c1ac9c99e613b22ae`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 1.0 MB (1010345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e282bb069bfd10203918d28975d264c20f327d5a587da48bc0dd979ccc2a3fd`  
		Last Modified: Wed, 02 Feb 2022 10:25:00 GMT  
		Size: 49.6 MB (49612751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28625866fc351d08f4264f93c6c4b7df54a6471924074cc846d1b894c55aa9f8`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:7c6832e02858bc32ec421d7f7908c8cc66c6f6bd20d92beeb861503a1c84e071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152185613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbeb84ea6ea113e9d87fc7b3be1a9e2c216a3d5c8d1a735214ac3c310962ab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:50:12 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:51:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:51:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 08:10:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:10:41 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:11:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:11:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:12:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:12:05 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:12:08 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:12:09 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 08:12:13 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 08:14:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:14:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:14:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:14:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:14:19 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ac27cb36bb8dd24defb16aca611d9a310ff50291b151fb1179fbb18e234e7`  
		Last Modified: Wed, 02 Feb 2022 05:58:45 GMT  
		Size: 38.6 MB (38641073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68febafb066e63efbfcc3c94c15fa0fdf31cc82e9682488ffc94ebe35434214a`  
		Last Modified: Wed, 02 Feb 2022 05:58:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6e3b1cfb67074ab7c5b4d350b0178b8f48d60ead234524bb3ca542217b7d7`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf82212b800515952bf89074aae7b2f5c9ffcfa683e50645deaa10a0b7bdd3b1`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 2.5 MB (2522832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752fad4e0201c301b4b52b929824591a1f22aa3ea2c8dd9112850f3276273f4e`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.2 MB (1236123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d297ef992ea410c0e80d1ddc3b10797a824ecea29c33c903058bd7cd340291`  
		Last Modified: Wed, 02 Feb 2022 08:22:25 GMT  
		Size: 49.9 MB (49854452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a6965d6b28ca7b375926fdd202ecba41292a65c41837e626e08c67f84d223f`  
		Last Modified: Wed, 02 Feb 2022 08:22:20 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:4.0.1`

```console
$ docker pull cassandra@sha256:d7afc180e4c22d87b6cb22da834e18d0b6f027271b8600aad64543cdb426785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:4.0.1` - linux; amd64

```console
$ docker pull cassandra@sha256:1e7e49947237f085f318ace1a887129452c78478b9e805edd20986b71221b030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149940985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d320f7a08ead778ced2db14f319a6ee13f3a9b0a60ddd64e36cf3097d323414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:59:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:59:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:59:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 16:44:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:44:21 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:44:40 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:44:41 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 16:51:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:51:16 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:51:17 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:51:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:51:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:51:17 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585a8f8fd99d708129717ae5fdac2d9fe803a5fee3291ff479f8dc04db42494`  
		Last Modified: Wed, 02 Feb 2022 03:03:11 GMT  
		Size: 43.2 MB (43230362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f03a4fb8d3d6c8106ee5f1bef091485bf8ae217d5c0a0b0e09f5c0e1a442f`  
		Last Modified: Wed, 02 Feb 2022 03:03:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326346e327fa4e5f6f21fa84ce290ff67d5a96a5abbe69545e23e3794ebd36e0`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8681365c18e7ec32b6c3fa74be141c9d3e037502d30c4c275ffc5ded71c33a5`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 2.2 MB (2160209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d006d3ddcdb9e800b59407661a1b9f6075daa25e786f35c942dd2ba1ca6698`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 1.3 MB (1315265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf35801b2911264b4ad225dfdf08adfcee3a6f9d471b6d28bdb2aa394b47eea`  
		Last Modified: Wed, 02 Feb 2022 16:58:02 GMT  
		Size: 49.9 MB (49853248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2b1ccdbb02b0b617add116ca538bfd44e437609503a9aaa639652247789bc`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0.1` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:a0bd1396a60ea5458cc694bad6fc5a13a4e72021db87e9aa340d364c104c0b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142048722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1470f92753ee6db83bde063895e8746612189d93be7c7c9b38bd5899e913de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:48:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:48:04 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:49:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:49:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:11:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 05:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 05:12:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 05:12:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:12:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 05:12:34 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 05:12:35 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 05:14:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 05:14:28 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 05:14:29 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 05:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 05:14:30 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 05:14:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca45b223849013a5db7d5850e0832f4aac669b33c69f09d9d74f6d6ae56a91d8`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 23.1 MB (23072061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605123915fece369da5778c9391348661f9ac3f37a8d4e3663c9c282ef486789`  
		Last Modified: Wed, 02 Feb 2022 02:55:57 GMT  
		Size: 41.9 MB (41850725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b512710f7691986f4b2e05d64e27b40ab28ad601c130c9d986ca42d03dcb2`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6686325283874be8268a1d58c6f2cdd07169c9ae2dd498bd863a1f46f4d2e39`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09aa4e0ae0d936e6d97ef85564085e1f0225bcd528b5e007034447cb6aba452`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.9 MB (1936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311e92d9b18c801f8b243c4df37876cf9a80d5550b52276fd3674360969633f7`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.3 MB (1269195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346900b2d9ff04a141f73dc72134e3f7b534f42245a533bebe0089422c9189d`  
		Last Modified: Wed, 02 Feb 2022 05:15:19 GMT  
		Size: 49.9 MB (49854744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8f088b8e4767142541c94cad57124da4600532a71c23b391b81e09a5377057`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0.1` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:3e6d95c4bea95e2aa2666762b113ea1f645fdaa1abbd49d95172d6853d00a1c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146259958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8203ffe1f6315a574658a9e4cf62400e55f7c9c60a541bdcac6262398d146144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:34 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:03:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:03:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 10:08:26 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:08:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:08:36 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:08:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:08:57 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:08:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:08:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:09:00 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:09:01 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 10:09:02 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 10:10:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:10:21 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:10:23 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:10:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:10:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:10:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6151ca955d4b7fb01dfd3c4470cc07f8484a7de594e6028377da2392b0b9d`  
		Last Modified: Wed, 02 Feb 2022 05:07:49 GMT  
		Size: 41.6 MB (41572184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5b05b981cfd36cda3c95e6c1b623132675dfd8e918bc928fb89bffc419f28`  
		Last Modified: Wed, 02 Feb 2022 05:07:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6f39fa98274f1fecd9e8aa58ab5f79fc37e9a3ab4e9a794c92e07d3473dc3c`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c2c1c85f859360b344bc7c141621d78a13c9e85b0595fab8cf5e1b1f545bf`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 2.1 MB (2129228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5758a9e04b46feeec48da5b86e2183ece68e0580f143c1ac9c99e613b22ae`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 1.0 MB (1010345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e282bb069bfd10203918d28975d264c20f327d5a587da48bc0dd979ccc2a3fd`  
		Last Modified: Wed, 02 Feb 2022 10:25:00 GMT  
		Size: 49.6 MB (49612751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28625866fc351d08f4264f93c6c4b7df54a6471924074cc846d1b894c55aa9f8`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0.1` - linux; ppc64le

```console
$ docker pull cassandra@sha256:7c6832e02858bc32ec421d7f7908c8cc66c6f6bd20d92beeb861503a1c84e071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152185613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbeb84ea6ea113e9d87fc7b3be1a9e2c216a3d5c8d1a735214ac3c310962ab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:50:12 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:51:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:51:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 08:10:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:10:41 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:11:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:11:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:12:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:12:05 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:12:08 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:12:09 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 08:12:13 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 08:14:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:14:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:14:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:14:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:14:19 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ac27cb36bb8dd24defb16aca611d9a310ff50291b151fb1179fbb18e234e7`  
		Last Modified: Wed, 02 Feb 2022 05:58:45 GMT  
		Size: 38.6 MB (38641073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68febafb066e63efbfcc3c94c15fa0fdf31cc82e9682488ffc94ebe35434214a`  
		Last Modified: Wed, 02 Feb 2022 05:58:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6e3b1cfb67074ab7c5b4d350b0178b8f48d60ead234524bb3ca542217b7d7`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf82212b800515952bf89074aae7b2f5c9ffcfa683e50645deaa10a0b7bdd3b1`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 2.5 MB (2522832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752fad4e0201c301b4b52b929824591a1f22aa3ea2c8dd9112850f3276273f4e`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.2 MB (1236123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d297ef992ea410c0e80d1ddc3b10797a824ecea29c33c903058bd7cd340291`  
		Last Modified: Wed, 02 Feb 2022 08:22:25 GMT  
		Size: 49.9 MB (49854452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a6965d6b28ca7b375926fdd202ecba41292a65c41837e626e08c67f84d223f`  
		Last Modified: Wed, 02 Feb 2022 08:22:20 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:latest`

```console
$ docker pull cassandra@sha256:d7afc180e4c22d87b6cb22da834e18d0b6f027271b8600aad64543cdb426785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:latest` - linux; amd64

```console
$ docker pull cassandra@sha256:1e7e49947237f085f318ace1a887129452c78478b9e805edd20986b71221b030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149940985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d320f7a08ead778ced2db14f319a6ee13f3a9b0a60ddd64e36cf3097d323414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:52 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:59:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:59:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:59:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 16:44:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 16:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 16:44:21 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 16:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 16:44:40 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 16:44:41 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 16:44:41 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 16:44:41 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 16:51:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 16:51:16 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 16:51:17 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 16:51:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 16:51:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 16:51:17 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585a8f8fd99d708129717ae5fdac2d9fe803a5fee3291ff479f8dc04db42494`  
		Last Modified: Wed, 02 Feb 2022 03:03:11 GMT  
		Size: 43.2 MB (43230362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f03a4fb8d3d6c8106ee5f1bef091485bf8ae217d5c0a0b0e09f5c0e1a442f`  
		Last Modified: Wed, 02 Feb 2022 03:03:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326346e327fa4e5f6f21fa84ce290ff67d5a96a5abbe69545e23e3794ebd36e0`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8681365c18e7ec32b6c3fa74be141c9d3e037502d30c4c275ffc5ded71c33a5`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 2.2 MB (2160209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d006d3ddcdb9e800b59407661a1b9f6075daa25e786f35c942dd2ba1ca6698`  
		Last Modified: Wed, 02 Feb 2022 16:57:59 GMT  
		Size: 1.3 MB (1315265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf35801b2911264b4ad225dfdf08adfcee3a6f9d471b6d28bdb2aa394b47eea`  
		Last Modified: Wed, 02 Feb 2022 16:58:02 GMT  
		Size: 49.9 MB (49853248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2b1ccdbb02b0b617add116ca538bfd44e437609503a9aaa639652247789bc`  
		Last Modified: Wed, 02 Feb 2022 16:57:58 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:a0bd1396a60ea5458cc694bad6fc5a13a4e72021db87e9aa340d364c104c0b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142048722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1470f92753ee6db83bde063895e8746612189d93be7c7c9b38bd5899e913de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:48:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:48:04 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 02:49:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:49:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 05:11:40 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 05:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 05:12:03 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 05:12:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 05:12:33 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:12:34 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 05:12:34 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 05:12:35 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 05:14:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 05:14:28 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 05:14:29 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 05:14:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 05:14:30 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 05:14:30 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca45b223849013a5db7d5850e0832f4aac669b33c69f09d9d74f6d6ae56a91d8`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 23.1 MB (23072061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605123915fece369da5778c9391348661f9ac3f37a8d4e3663c9c282ef486789`  
		Last Modified: Wed, 02 Feb 2022 02:55:57 GMT  
		Size: 41.9 MB (41850725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b512710f7691986f4b2e05d64e27b40ab28ad601c130c9d986ca42d03dcb2`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6686325283874be8268a1d58c6f2cdd07169c9ae2dd498bd863a1f46f4d2e39`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09aa4e0ae0d936e6d97ef85564085e1f0225bcd528b5e007034447cb6aba452`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.9 MB (1936119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311e92d9b18c801f8b243c4df37876cf9a80d5550b52276fd3674360969633f7`  
		Last Modified: Wed, 02 Feb 2022 05:15:04 GMT  
		Size: 1.3 MB (1269195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346900b2d9ff04a141f73dc72134e3f7b534f42245a533bebe0089422c9189d`  
		Last Modified: Wed, 02 Feb 2022 05:15:19 GMT  
		Size: 49.9 MB (49854744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8f088b8e4767142541c94cad57124da4600532a71c23b391b81e09a5377057`  
		Last Modified: Wed, 02 Feb 2022 05:15:03 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:3e6d95c4bea95e2aa2666762b113ea1f645fdaa1abbd49d95172d6853d00a1c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146259958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8203ffe1f6315a574658a9e4cf62400e55f7c9c60a541bdcac6262398d146144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:02:34 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:03:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:03:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 10:08:26 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 10:08:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 10:08:36 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 10:08:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 10:08:57 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 10:08:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 10:08:59 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 10:09:00 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 10:09:01 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 10:09:02 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 10:10:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 10:10:21 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 10:10:23 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 10:10:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 10:10:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 10:10:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6151ca955d4b7fb01dfd3c4470cc07f8484a7de594e6028377da2392b0b9d`  
		Last Modified: Wed, 02 Feb 2022 05:07:49 GMT  
		Size: 41.6 MB (41572184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d5b05b981cfd36cda3c95e6c1b623132675dfd8e918bc928fb89bffc419f28`  
		Last Modified: Wed, 02 Feb 2022 05:07:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6f39fa98274f1fecd9e8aa58ab5f79fc37e9a3ab4e9a794c92e07d3473dc3c`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c2c1c85f859360b344bc7c141621d78a13c9e85b0595fab8cf5e1b1f545bf`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 2.1 MB (2129228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5758a9e04b46feeec48da5b86e2183ece68e0580f143c1ac9c99e613b22ae`  
		Last Modified: Wed, 02 Feb 2022 10:24:56 GMT  
		Size: 1.0 MB (1010345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e282bb069bfd10203918d28975d264c20f327d5a587da48bc0dd979ccc2a3fd`  
		Last Modified: Wed, 02 Feb 2022 10:25:00 GMT  
		Size: 49.6 MB (49612751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28625866fc351d08f4264f93c6c4b7df54a6471924074cc846d1b894c55aa9f8`  
		Last Modified: Wed, 02 Feb 2022 10:24:55 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:7c6832e02858bc32ec421d7f7908c8cc66c6f6bd20d92beeb861503a1c84e071
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152185613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbeb84ea6ea113e9d87fc7b3be1a9e2c216a3d5c8d1a735214ac3c310962ab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:50:12 GMT
ENV JAVA_VERSION=jdk-11.0.14+9
# Wed, 02 Feb 2022 05:51:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f20bcf8c29057b7275876b1d9e68c13dca03789750ddfabdb213a69f3aa3fcf5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14_9.tar.gz';          ;;        armhf|arm)          ESUM='675fb486e99060e097d194178f6bd387585c06647eeac27109145a0f03ec3b92';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.14_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='fc94df3676ebae655a4a1c07767535f12d72b3d913d5111f5f21ac9e1a009572';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d2a631aa367d9ef37082e0b1f5d21d18cffddbe24045f4b2fb318d4ba841c3fd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f9c0b0c5f379f57424a1cb9fb304003aeb827817d8b12164388792e145011480';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.14_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:51:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 02 Feb 2022 08:10:02 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 02 Feb 2022 08:10:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 02 Feb 2022 08:10:41 GMT
ENV GOSU_VERSION=1.12
# Wed, 02 Feb 2022 08:11:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 08:11:58 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 02 Feb 2022 08:12:01 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 02 Feb 2022 08:12:05 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 08:12:08 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 02 Feb 2022 08:12:09 GMT
ENV CASSANDRA_VERSION=4.0.1
# Wed, 02 Feb 2022 08:12:13 GMT
ENV CASSANDRA_SHA512=2890c054666afa93fe2978c46da5db15ed7d11d60f4890574dc642bd81f7b3af40b41d3e5b8245e6c1453a165eddebeb28bcf3fef1a2b2fc6fb3b82058d7ceb0
# Wed, 02 Feb 2022 08:14:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 02 Feb 2022 08:14:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 02 Feb 2022 08:14:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 02 Feb 2022 08:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 08:14:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 02 Feb 2022 08:14:19 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ac27cb36bb8dd24defb16aca611d9a310ff50291b151fb1179fbb18e234e7`  
		Last Modified: Wed, 02 Feb 2022 05:58:45 GMT  
		Size: 38.6 MB (38641073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68febafb066e63efbfcc3c94c15fa0fdf31cc82e9682488ffc94ebe35434214a`  
		Last Modified: Wed, 02 Feb 2022 05:58:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6e3b1cfb67074ab7c5b4d350b0178b8f48d60ead234524bb3ca542217b7d7`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf82212b800515952bf89074aae7b2f5c9ffcfa683e50645deaa10a0b7bdd3b1`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 2.5 MB (2522832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752fad4e0201c301b4b52b929824591a1f22aa3ea2c8dd9112850f3276273f4e`  
		Last Modified: Wed, 02 Feb 2022 08:22:21 GMT  
		Size: 1.2 MB (1236123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d297ef992ea410c0e80d1ddc3b10797a824ecea29c33c903058bd7cd340291`  
		Last Modified: Wed, 02 Feb 2022 08:22:25 GMT  
		Size: 49.9 MB (49854452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a6965d6b28ca7b375926fdd202ecba41292a65c41837e626e08c67f84d223f`  
		Last Modified: Wed, 02 Feb 2022 08:22:20 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
