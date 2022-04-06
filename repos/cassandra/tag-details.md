<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `cassandra`

-	[`cassandra:3`](#cassandra3)
-	[`cassandra:3.0`](#cassandra30)
-	[`cassandra:3.0.26`](#cassandra3026)
-	[`cassandra:3.11`](#cassandra311)
-	[`cassandra:3.11.12`](#cassandra31112)
-	[`cassandra:4`](#cassandra4)
-	[`cassandra:4.0`](#cassandra40)
-	[`cassandra:4.0.3`](#cassandra403)
-	[`cassandra:latest`](#cassandralatest)

## `cassandra:3`

```console
$ docker pull cassandra@sha256:9dd8201f254d94380612cb918eb47b1dbe6ace6cf417f5fe890e3c15a85533fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3` - linux; amd64

```console
$ docker pull cassandra@sha256:8517e4fc9df510d13f25d81d487996bef4b66b76e758c186602e327ebfcd0c94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129688337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d8a3f21648f7ac853ed77abb65135fce16062d8db6bd2c40b4054ae2725478`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:03 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 04:54:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:54:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:54:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:54:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:54:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 04:54:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:54:39 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:54:39 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:54:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 04:54:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:54:40 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:54:40 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe65b7bd97ef856e2eb027fca02eb3a03fc15438b7e7e6c17efa9e0bad759d`  
		Last Modified: Tue, 05 Apr 2022 23:10:07 GMT  
		Size: 41.8 MB (41773798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff312975bbf79abccf177e6ba71ed66447d75914a3be6c4d0be50e20f7bd8f4`  
		Last Modified: Tue, 05 Apr 2022 23:10:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a1c8b05f0710e2ac3f734e3f3e16f7c9df946429b2fdf4c6266f717f739d`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88bdc12d10cbcbad16404e873cb5b3fe133b3f20f14abdd4716e075dce0271a`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 9.5 MB (9520751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0361372f3f252fc66be242838f3e8bedbb3ed58d550e95d8b795b7892b82bb2b`  
		Last Modified: Wed, 06 Apr 2022 04:55:39 GMT  
		Size: 1.3 MB (1316176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51e78dbddf47fe06318e20b44bd5371012835bf4654dd2471ca0562d8df6bea`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 32.5 MB (32477989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eecbba06788d9180f126d94d98fbe197cf52ef756473081dff0af26e079587`  
		Last Modified: Wed, 06 Apr 2022 04:55:38 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac32352b35a576b800e324c512dda93a4d7a1a5457e4e16ce9687db2bb9355`  
		Last Modified: Wed, 06 Apr 2022 04:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:8def3259f3a7703d99f64b79d843509d78f06f0738581de9992b238c81ac9a15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121133482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dfff6e4bcf756ecd8cd193f6eb940a77b6e6d3f43c9687635b91d0cce35bff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:03:58 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:04:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:04:57 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 05:51:56 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:52:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:52:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:52:35 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:52:36 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:52:37 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 05:52:37 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 05:53:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:53:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:53:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 05:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:53:09 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:53:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571d75f300668becfcd40e9fafe6bbce8567722d68f30aeb98dc329d4823191`  
		Last Modified: Wed, 06 Apr 2022 04:13:25 GMT  
		Size: 39.5 MB (39507446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ed2119a1c0ba32f14c24749a783945a7e212b84bcdbd71e3c4aacd2065f03`  
		Last Modified: Wed, 06 Apr 2022 04:13:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b2c8d215497665a3eb09f4b09bb53efd3081bd5979ba37242ee76ff6302bf`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f64d254a9003912150f2111698eee0d8da69a7fe06250925b26fac3fb3c7c`  
		Last Modified: Wed, 06 Apr 2022 05:55:41 GMT  
		Size: 8.9 MB (8899426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7eca9d937559fb9bb552674ca6349d6e953d8098f0c5d1943b1863f46d3871`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.3 MB (1269816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab372b29b82bc7548c528b8a9eded479f5a2fcbb1c189077501db50ac4c44e`  
		Last Modified: Wed, 06 Apr 2022 05:55:44 GMT  
		Size: 32.5 MB (32479207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1dcda68a9752bd330cb5619db062c45992f67a0b1591d193aecfb77857e078`  
		Last Modified: Wed, 06 Apr 2022 05:55:33 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478bb0878182f0d25a266ed9dbae1a04c5e1bc13ad16b7491ac7b2b46452db`  
		Last Modified: Wed, 06 Apr 2022 05:55:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:18e1e5406e4cd6413571f972690553c8a4e2272c648a35030281d377aed7a802
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126635893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43262b9173ec9cac093bac08c9da1c0fb01b46f8c72c039695c6108b328c2ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:19:57 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:20:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:20:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:20:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 03:39:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:39:42 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:39:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:39:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:39:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:39:57 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:39:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:39:59 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 03:40:00 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 03:40:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:40:20 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:40:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 03:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:40:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:40:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f9c4e86dbe952096d342e88426076fa51dbdbebdb4eaf88241bb2620f3c54`  
		Last Modified: Tue, 05 Apr 2022 23:25:38 GMT  
		Size: 40.8 MB (40769839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9297f966344d79f5c43f91cc3302de9ef04e5470abc1aef22b69662f5bc3cb2`  
		Last Modified: Tue, 05 Apr 2022 23:25:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353fbc349257275f1fc07f7c5890a73f5203208eacbba5562d02784b273b1249`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326611242d9919dd1e5dfa4f47d9a8d440e21538b6784606d680f09c51dff5f2`  
		Last Modified: Wed, 06 Apr 2022 03:41:51 GMT  
		Size: 9.6 MB (9550721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc745ff3919ae3c0ae1548bea5212b0b30f5847cc8d8317d397d3538719f491`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 1.0 MB (1010703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365a4074b25f41b67c6f607a83edcb7df6da6ebd5e09cb392ddccf900478fa71`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 32.2 MB (32236540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d079081fa12e1fdce42815d042d064a44d46544e55d83140626e9a042694122`  
		Last Modified: Wed, 06 Apr 2022 03:41:49 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49585b4cf01f23d02ee4ce0cf015c753a00df3db23f4f3b9dbf7e5b06d727fda`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3` - linux; ppc64le

```console
$ docker pull cassandra@sha256:ddd6173938668416bebdc5e9f739b403d6c992377034350382c6a9996d96159d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135689235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1efe397aef8317ac23ebc26aac38c98ef09df88d92bfc06c30f9e5610589a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:10:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 20:11:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:11:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:11:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 20:11:45 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:12:35 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:13:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:13:43 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:13:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:13:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:13:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:13:51 GMT
ENV CASSANDRA_VERSION=3.11.12
# Sun, 20 Mar 2022 20:13:55 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Sun, 20 Mar 2022 20:18:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:18:35 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:18:36 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:18:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sun, 20 Mar 2022 20:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:18:47 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:18:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e79e12f00cc2f2ad6a2f2a94bceb7063937e945931ff8fbda9c055408e37da4`  
		Last Modified: Sat, 19 Mar 2022 20:18:49 GMT  
		Size: 41.2 MB (41162315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bd6b17f427e5b43109e77cde332787886f2d266caff26f56cb4deba881c2ac`  
		Last Modified: Sat, 19 Mar 2022 20:18:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f14abe92e4b95af2a51ba629bfffc99fdfba0929ae52c84969b4fe1e61108c`  
		Last Modified: Sun, 20 Mar 2022 20:23:17 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03e24fcf564356db942d48cfd8afdc008542f4655939fe8b19bb54237a43d0`  
		Last Modified: Sun, 20 Mar 2022 20:23:16 GMT  
		Size: 10.3 MB (10310109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58212613733fbf81b88cb6b5ac12c8f630f376f26191b877627b9b94268551bc`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 MB (1236822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04d34853a015067ef161ced6432ae8df93bbb14085e3cfcdef0f237d093fcbc`  
		Last Modified: Sun, 20 Mar 2022 20:23:18 GMT  
		Size: 32.5 MB (32479031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd07b810aa6883fe4dfcf7aee43b9ab584fb210e1ce62f0c1da7cc8a52d02ed`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f086e4aaecd8115cd259af3a39483262ba84e698ba72e4881ca65509c66b9b`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.0`

```console
$ docker pull cassandra@sha256:091f6918d345bf97def9b1e663135696edc46e2c8430615a2dc164af85e1575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.0` - linux; amd64

```console
$ docker pull cassandra@sha256:c86f1dcf762a9f04dd7626839b88c7b09e34603b5f657873b28a7cadc86adc15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124386894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71f71ef2335d4e0147950a3a1c27339c2bce8c5eb4d9fce830d89f6ee7d62a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:03 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 04:54:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:54:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:54:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:54:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:54:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:54:45 GMT
ENV CASSANDRA_VERSION=3.0.26
# Wed, 06 Apr 2022 04:54:45 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Wed, 06 Apr 2022 04:55:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:55:02 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:55:02 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 04:55:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:55:03 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:55:03 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe65b7bd97ef856e2eb027fca02eb3a03fc15438b7e7e6c17efa9e0bad759d`  
		Last Modified: Tue, 05 Apr 2022 23:10:07 GMT  
		Size: 41.8 MB (41773798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff312975bbf79abccf177e6ba71ed66447d75914a3be6c4d0be50e20f7bd8f4`  
		Last Modified: Tue, 05 Apr 2022 23:10:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a1c8b05f0710e2ac3f734e3f3e16f7c9df946429b2fdf4c6266f717f739d`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88bdc12d10cbcbad16404e873cb5b3fe133b3f20f14abdd4716e075dce0271a`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 9.5 MB (9520751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0361372f3f252fc66be242838f3e8bedbb3ed58d550e95d8b795b7892b82bb2b`  
		Last Modified: Wed, 06 Apr 2022 04:55:39 GMT  
		Size: 1.3 MB (1316176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae1e63fe68fd142a1a4f0bce2334c9a31aff8ab412c2f8fa8f9ff78d615bfa`  
		Last Modified: Wed, 06 Apr 2022 04:55:55 GMT  
		Size: 27.2 MB (27176547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065c158f6f814fcddb3f71f3703dd7161a6c3a6089ab9baed7e744caef9cd87`  
		Last Modified: Wed, 06 Apr 2022 04:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc33f72604d923c5aefe1334bf55949d279a2e234dda8d113467425b28d77f`  
		Last Modified: Wed, 06 Apr 2022 04:55:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:676d85a2706725c0b252f3f1f3135005fbcb37721686fe1b9293effda23c1916
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115832199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8167a2e6988cdef77df99e59acd51b2a45af0fee1e3751f6ab308da5933b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:03:58 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:04:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:04:57 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 05:51:56 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:52:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:52:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:52:35 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:52:36 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:53:28 GMT
ENV CASSANDRA_VERSION=3.0.26
# Wed, 06 Apr 2022 05:53:28 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Wed, 06 Apr 2022 05:53:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:54:00 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:54:00 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:54:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 05:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:02 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:54:03 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571d75f300668becfcd40e9fafe6bbce8567722d68f30aeb98dc329d4823191`  
		Last Modified: Wed, 06 Apr 2022 04:13:25 GMT  
		Size: 39.5 MB (39507446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ed2119a1c0ba32f14c24749a783945a7e212b84bcdbd71e3c4aacd2065f03`  
		Last Modified: Wed, 06 Apr 2022 04:13:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b2c8d215497665a3eb09f4b09bb53efd3081bd5979ba37242ee76ff6302bf`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f64d254a9003912150f2111698eee0d8da69a7fe06250925b26fac3fb3c7c`  
		Last Modified: Wed, 06 Apr 2022 05:55:41 GMT  
		Size: 8.9 MB (8899426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7eca9d937559fb9bb552674ca6349d6e953d8098f0c5d1943b1863f46d3871`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.3 MB (1269816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06f421e49d5709130adfdedcaca23bf357f847737b6123407e0bfd1ba1deb6`  
		Last Modified: Wed, 06 Apr 2022 05:56:09 GMT  
		Size: 27.2 MB (27177927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a6884876f61a7e9b803c872004d16c716532f5b52791065b24caa8cdec962f`  
		Last Modified: Wed, 06 Apr 2022 05:56:00 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07da8b72eda7595f3e96bec18e4128adc6263c971a4c12b91114beecee33a4b2`  
		Last Modified: Wed, 06 Apr 2022 05:56:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:9f171da93df9e1afa0f678ea729f220f52277d5921033fdccf9e08e492b91337
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0d569215603d37b4551622afe3c1ef30ca191ccca40f58ab55c5fa9007077f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:19:57 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:20:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:20:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:20:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 03:39:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:39:42 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:39:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:39:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:39:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:39:57 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:39:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:40:31 GMT
ENV CASSANDRA_VERSION=3.0.26
# Wed, 06 Apr 2022 03:40:32 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Wed, 06 Apr 2022 03:40:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:40:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:40:57 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:40:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 03:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:40:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:41:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f9c4e86dbe952096d342e88426076fa51dbdbebdb4eaf88241bb2620f3c54`  
		Last Modified: Tue, 05 Apr 2022 23:25:38 GMT  
		Size: 40.8 MB (40769839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9297f966344d79f5c43f91cc3302de9ef04e5470abc1aef22b69662f5bc3cb2`  
		Last Modified: Tue, 05 Apr 2022 23:25:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353fbc349257275f1fc07f7c5890a73f5203208eacbba5562d02784b273b1249`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326611242d9919dd1e5dfa4f47d9a8d440e21538b6784606d680f09c51dff5f2`  
		Last Modified: Wed, 06 Apr 2022 03:41:51 GMT  
		Size: 9.6 MB (9550721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc745ff3919ae3c0ae1548bea5212b0b30f5847cc8d8317d397d3538719f491`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 1.0 MB (1010703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b673817f10cf6b4310189f390982fcac85d5c1a67c876e6fd5606097ade0f26d`  
		Last Modified: Wed, 06 Apr 2022 03:42:11 GMT  
		Size: 26.9 MB (26935200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d667f6e332cf89d054decba7b6a69cbd47ed934511814e0e6740e52258ecf`  
		Last Modified: Wed, 06 Apr 2022 03:42:07 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fa37e7fd969aaa4ca22f52965bdecb3b7641456fed21fedac50ba07049f848`  
		Last Modified: Wed, 06 Apr 2022 03:42:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:4cc6d38b848a492bc79250e3623063b930e4a59ed7a171d4be7006320b8f0cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130387703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c0b1c5cba454ece41961676d0dc28d4e8f86a1e116f276b009be0a41c8112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:10:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 20:11:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:11:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:11:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 20:11:45 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:12:35 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:13:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:13:43 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:13:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:13:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:13:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:19:03 GMT
ENV CASSANDRA_VERSION=3.0.26
# Sun, 20 Mar 2022 20:19:06 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Sun, 20 Mar 2022 20:22:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:22:05 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:22:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:22:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sun, 20 Mar 2022 20:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:22:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:22:19 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e79e12f00cc2f2ad6a2f2a94bceb7063937e945931ff8fbda9c055408e37da4`  
		Last Modified: Sat, 19 Mar 2022 20:18:49 GMT  
		Size: 41.2 MB (41162315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bd6b17f427e5b43109e77cde332787886f2d266caff26f56cb4deba881c2ac`  
		Last Modified: Sat, 19 Mar 2022 20:18:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f14abe92e4b95af2a51ba629bfffc99fdfba0929ae52c84969b4fe1e61108c`  
		Last Modified: Sun, 20 Mar 2022 20:23:17 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03e24fcf564356db942d48cfd8afdc008542f4655939fe8b19bb54237a43d0`  
		Last Modified: Sun, 20 Mar 2022 20:23:16 GMT  
		Size: 10.3 MB (10310109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58212613733fbf81b88cb6b5ac12c8f630f376f26191b877627b9b94268551bc`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 MB (1236822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d890a559a1e8804b652b3564830b81050d0e3af859949a758a3d1636517f2ccc`  
		Last Modified: Sun, 20 Mar 2022 20:23:37 GMT  
		Size: 27.2 MB (27177498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25b5143a053409a637df6f37d5ed53875e5197950d923471adf8578ac39f1cc`  
		Last Modified: Sun, 20 Mar 2022 20:23:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc71d9f5b08933dfcb89a15b4a2e76baa7b636dff31d7470b67a78d2dd03f2c6`  
		Last Modified: Sun, 20 Mar 2022 20:23:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.0.26`

```console
$ docker pull cassandra@sha256:091f6918d345bf97def9b1e663135696edc46e2c8430615a2dc164af85e1575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.0.26` - linux; amd64

```console
$ docker pull cassandra@sha256:c86f1dcf762a9f04dd7626839b88c7b09e34603b5f657873b28a7cadc86adc15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124386894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71f71ef2335d4e0147950a3a1c27339c2bce8c5eb4d9fce830d89f6ee7d62a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:03 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 04:54:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:54:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:54:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:54:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:54:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:54:45 GMT
ENV CASSANDRA_VERSION=3.0.26
# Wed, 06 Apr 2022 04:54:45 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Wed, 06 Apr 2022 04:55:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:55:02 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:55:02 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:55:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 04:55:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:55:03 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:55:03 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe65b7bd97ef856e2eb027fca02eb3a03fc15438b7e7e6c17efa9e0bad759d`  
		Last Modified: Tue, 05 Apr 2022 23:10:07 GMT  
		Size: 41.8 MB (41773798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff312975bbf79abccf177e6ba71ed66447d75914a3be6c4d0be50e20f7bd8f4`  
		Last Modified: Tue, 05 Apr 2022 23:10:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a1c8b05f0710e2ac3f734e3f3e16f7c9df946429b2fdf4c6266f717f739d`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88bdc12d10cbcbad16404e873cb5b3fe133b3f20f14abdd4716e075dce0271a`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 9.5 MB (9520751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0361372f3f252fc66be242838f3e8bedbb3ed58d550e95d8b795b7892b82bb2b`  
		Last Modified: Wed, 06 Apr 2022 04:55:39 GMT  
		Size: 1.3 MB (1316176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ae1e63fe68fd142a1a4f0bce2334c9a31aff8ab412c2f8fa8f9ff78d615bfa`  
		Last Modified: Wed, 06 Apr 2022 04:55:55 GMT  
		Size: 27.2 MB (27176547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065c158f6f814fcddb3f71f3703dd7161a6c3a6089ab9baed7e744caef9cd87`  
		Last Modified: Wed, 06 Apr 2022 04:55:53 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc33f72604d923c5aefe1334bf55949d279a2e234dda8d113467425b28d77f`  
		Last Modified: Wed, 06 Apr 2022 04:55:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0.26` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:676d85a2706725c0b252f3f1f3135005fbcb37721686fe1b9293effda23c1916
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115832199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8167a2e6988cdef77df99e59acd51b2a45af0fee1e3751f6ab308da5933b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:03:58 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:04:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:04:57 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 05:51:56 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:52:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:52:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:52:35 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:52:36 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:53:28 GMT
ENV CASSANDRA_VERSION=3.0.26
# Wed, 06 Apr 2022 05:53:28 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Wed, 06 Apr 2022 05:53:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:54:00 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:54:00 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:54:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 05:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:54:02 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:54:03 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571d75f300668becfcd40e9fafe6bbce8567722d68f30aeb98dc329d4823191`  
		Last Modified: Wed, 06 Apr 2022 04:13:25 GMT  
		Size: 39.5 MB (39507446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ed2119a1c0ba32f14c24749a783945a7e212b84bcdbd71e3c4aacd2065f03`  
		Last Modified: Wed, 06 Apr 2022 04:13:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b2c8d215497665a3eb09f4b09bb53efd3081bd5979ba37242ee76ff6302bf`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f64d254a9003912150f2111698eee0d8da69a7fe06250925b26fac3fb3c7c`  
		Last Modified: Wed, 06 Apr 2022 05:55:41 GMT  
		Size: 8.9 MB (8899426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7eca9d937559fb9bb552674ca6349d6e953d8098f0c5d1943b1863f46d3871`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.3 MB (1269816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a06f421e49d5709130adfdedcaca23bf357f847737b6123407e0bfd1ba1deb6`  
		Last Modified: Wed, 06 Apr 2022 05:56:09 GMT  
		Size: 27.2 MB (27177927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a6884876f61a7e9b803c872004d16c716532f5b52791065b24caa8cdec962f`  
		Last Modified: Wed, 06 Apr 2022 05:56:00 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07da8b72eda7595f3e96bec18e4128adc6263c971a4c12b91114beecee33a4b2`  
		Last Modified: Wed, 06 Apr 2022 05:56:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0.26` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:9f171da93df9e1afa0f678ea729f220f52277d5921033fdccf9e08e492b91337
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0d569215603d37b4551622afe3c1ef30ca191ccca40f58ab55c5fa9007077f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:19:57 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:20:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:20:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:20:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 03:39:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:39:42 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:39:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:39:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:39:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:39:57 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:39:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:40:31 GMT
ENV CASSANDRA_VERSION=3.0.26
# Wed, 06 Apr 2022 03:40:32 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Wed, 06 Apr 2022 03:40:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:40:55 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:40:57 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:40:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 03:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:40:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:41:00 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f9c4e86dbe952096d342e88426076fa51dbdbebdb4eaf88241bb2620f3c54`  
		Last Modified: Tue, 05 Apr 2022 23:25:38 GMT  
		Size: 40.8 MB (40769839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9297f966344d79f5c43f91cc3302de9ef04e5470abc1aef22b69662f5bc3cb2`  
		Last Modified: Tue, 05 Apr 2022 23:25:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353fbc349257275f1fc07f7c5890a73f5203208eacbba5562d02784b273b1249`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326611242d9919dd1e5dfa4f47d9a8d440e21538b6784606d680f09c51dff5f2`  
		Last Modified: Wed, 06 Apr 2022 03:41:51 GMT  
		Size: 9.6 MB (9550721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc745ff3919ae3c0ae1548bea5212b0b30f5847cc8d8317d397d3538719f491`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 1.0 MB (1010703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b673817f10cf6b4310189f390982fcac85d5c1a67c876e6fd5606097ade0f26d`  
		Last Modified: Wed, 06 Apr 2022 03:42:11 GMT  
		Size: 26.9 MB (26935200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82d667f6e332cf89d054decba7b6a69cbd47ed934511814e0e6740e52258ecf`  
		Last Modified: Wed, 06 Apr 2022 03:42:07 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fa37e7fd969aaa4ca22f52965bdecb3b7641456fed21fedac50ba07049f848`  
		Last Modified: Wed, 06 Apr 2022 03:42:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.0.26` - linux; ppc64le

```console
$ docker pull cassandra@sha256:4cc6d38b848a492bc79250e3623063b930e4a59ed7a171d4be7006320b8f0cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130387703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c0b1c5cba454ece41961676d0dc28d4e8f86a1e116f276b009be0a41c8112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:10:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 20:11:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:11:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:11:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 20:11:45 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:12:35 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:13:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:13:43 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:13:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:13:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:13:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:19:03 GMT
ENV CASSANDRA_VERSION=3.0.26
# Sun, 20 Mar 2022 20:19:06 GMT
ENV CASSANDRA_SHA512=1f18094d0191d722371942d6046dcd0b70342c995800c277c822d81a2584c3b8d3f38d47f831b19d3ccf17b079a24540672998ba1b546d67594ff62618323c54
# Sun, 20 Mar 2022 20:22:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:22:05 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:22:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:22:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sun, 20 Mar 2022 20:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:22:17 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:22:19 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e79e12f00cc2f2ad6a2f2a94bceb7063937e945931ff8fbda9c055408e37da4`  
		Last Modified: Sat, 19 Mar 2022 20:18:49 GMT  
		Size: 41.2 MB (41162315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bd6b17f427e5b43109e77cde332787886f2d266caff26f56cb4deba881c2ac`  
		Last Modified: Sat, 19 Mar 2022 20:18:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f14abe92e4b95af2a51ba629bfffc99fdfba0929ae52c84969b4fe1e61108c`  
		Last Modified: Sun, 20 Mar 2022 20:23:17 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03e24fcf564356db942d48cfd8afdc008542f4655939fe8b19bb54237a43d0`  
		Last Modified: Sun, 20 Mar 2022 20:23:16 GMT  
		Size: 10.3 MB (10310109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58212613733fbf81b88cb6b5ac12c8f630f376f26191b877627b9b94268551bc`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 MB (1236822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d890a559a1e8804b652b3564830b81050d0e3af859949a758a3d1636517f2ccc`  
		Last Modified: Sun, 20 Mar 2022 20:23:37 GMT  
		Size: 27.2 MB (27177498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25b5143a053409a637df6f37d5ed53875e5197950d923471adf8578ac39f1cc`  
		Last Modified: Sun, 20 Mar 2022 20:23:34 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc71d9f5b08933dfcb89a15b4a2e76baa7b636dff31d7470b67a78d2dd03f2c6`  
		Last Modified: Sun, 20 Mar 2022 20:23:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.11`

```console
$ docker pull cassandra@sha256:9dd8201f254d94380612cb918eb47b1dbe6ace6cf417f5fe890e3c15a85533fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.11` - linux; amd64

```console
$ docker pull cassandra@sha256:8517e4fc9df510d13f25d81d487996bef4b66b76e758c186602e327ebfcd0c94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129688337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d8a3f21648f7ac853ed77abb65135fce16062d8db6bd2c40b4054ae2725478`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:03 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 04:54:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:54:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:54:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:54:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:54:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 04:54:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:54:39 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:54:39 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:54:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 04:54:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:54:40 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:54:40 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe65b7bd97ef856e2eb027fca02eb3a03fc15438b7e7e6c17efa9e0bad759d`  
		Last Modified: Tue, 05 Apr 2022 23:10:07 GMT  
		Size: 41.8 MB (41773798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff312975bbf79abccf177e6ba71ed66447d75914a3be6c4d0be50e20f7bd8f4`  
		Last Modified: Tue, 05 Apr 2022 23:10:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a1c8b05f0710e2ac3f734e3f3e16f7c9df946429b2fdf4c6266f717f739d`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88bdc12d10cbcbad16404e873cb5b3fe133b3f20f14abdd4716e075dce0271a`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 9.5 MB (9520751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0361372f3f252fc66be242838f3e8bedbb3ed58d550e95d8b795b7892b82bb2b`  
		Last Modified: Wed, 06 Apr 2022 04:55:39 GMT  
		Size: 1.3 MB (1316176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51e78dbddf47fe06318e20b44bd5371012835bf4654dd2471ca0562d8df6bea`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 32.5 MB (32477989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eecbba06788d9180f126d94d98fbe197cf52ef756473081dff0af26e079587`  
		Last Modified: Wed, 06 Apr 2022 04:55:38 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac32352b35a576b800e324c512dda93a4d7a1a5457e4e16ce9687db2bb9355`  
		Last Modified: Wed, 06 Apr 2022 04:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:8def3259f3a7703d99f64b79d843509d78f06f0738581de9992b238c81ac9a15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121133482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dfff6e4bcf756ecd8cd193f6eb940a77b6e6d3f43c9687635b91d0cce35bff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:03:58 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:04:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:04:57 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 05:51:56 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:52:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:52:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:52:35 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:52:36 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:52:37 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 05:52:37 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 05:53:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:53:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:53:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 05:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:53:09 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:53:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571d75f300668becfcd40e9fafe6bbce8567722d68f30aeb98dc329d4823191`  
		Last Modified: Wed, 06 Apr 2022 04:13:25 GMT  
		Size: 39.5 MB (39507446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ed2119a1c0ba32f14c24749a783945a7e212b84bcdbd71e3c4aacd2065f03`  
		Last Modified: Wed, 06 Apr 2022 04:13:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b2c8d215497665a3eb09f4b09bb53efd3081bd5979ba37242ee76ff6302bf`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f64d254a9003912150f2111698eee0d8da69a7fe06250925b26fac3fb3c7c`  
		Last Modified: Wed, 06 Apr 2022 05:55:41 GMT  
		Size: 8.9 MB (8899426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7eca9d937559fb9bb552674ca6349d6e953d8098f0c5d1943b1863f46d3871`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.3 MB (1269816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab372b29b82bc7548c528b8a9eded479f5a2fcbb1c189077501db50ac4c44e`  
		Last Modified: Wed, 06 Apr 2022 05:55:44 GMT  
		Size: 32.5 MB (32479207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1dcda68a9752bd330cb5619db062c45992f67a0b1591d193aecfb77857e078`  
		Last Modified: Wed, 06 Apr 2022 05:55:33 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478bb0878182f0d25a266ed9dbae1a04c5e1bc13ad16b7491ac7b2b46452db`  
		Last Modified: Wed, 06 Apr 2022 05:55:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:18e1e5406e4cd6413571f972690553c8a4e2272c648a35030281d377aed7a802
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126635893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43262b9173ec9cac093bac08c9da1c0fb01b46f8c72c039695c6108b328c2ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:19:57 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:20:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:20:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:20:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 03:39:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:39:42 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:39:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:39:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:39:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:39:57 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:39:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:39:59 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 03:40:00 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 03:40:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:40:20 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:40:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 03:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:40:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:40:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f9c4e86dbe952096d342e88426076fa51dbdbebdb4eaf88241bb2620f3c54`  
		Last Modified: Tue, 05 Apr 2022 23:25:38 GMT  
		Size: 40.8 MB (40769839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9297f966344d79f5c43f91cc3302de9ef04e5470abc1aef22b69662f5bc3cb2`  
		Last Modified: Tue, 05 Apr 2022 23:25:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353fbc349257275f1fc07f7c5890a73f5203208eacbba5562d02784b273b1249`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326611242d9919dd1e5dfa4f47d9a8d440e21538b6784606d680f09c51dff5f2`  
		Last Modified: Wed, 06 Apr 2022 03:41:51 GMT  
		Size: 9.6 MB (9550721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc745ff3919ae3c0ae1548bea5212b0b30f5847cc8d8317d397d3538719f491`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 1.0 MB (1010703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365a4074b25f41b67c6f607a83edcb7df6da6ebd5e09cb392ddccf900478fa71`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 32.2 MB (32236540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d079081fa12e1fdce42815d042d064a44d46544e55d83140626e9a042694122`  
		Last Modified: Wed, 06 Apr 2022 03:41:49 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49585b4cf01f23d02ee4ce0cf015c753a00df3db23f4f3b9dbf7e5b06d727fda`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11` - linux; ppc64le

```console
$ docker pull cassandra@sha256:ddd6173938668416bebdc5e9f739b403d6c992377034350382c6a9996d96159d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135689235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1efe397aef8317ac23ebc26aac38c98ef09df88d92bfc06c30f9e5610589a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:10:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 20:11:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:11:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:11:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 20:11:45 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:12:35 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:13:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:13:43 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:13:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:13:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:13:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:13:51 GMT
ENV CASSANDRA_VERSION=3.11.12
# Sun, 20 Mar 2022 20:13:55 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Sun, 20 Mar 2022 20:18:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:18:35 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:18:36 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:18:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sun, 20 Mar 2022 20:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:18:47 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:18:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e79e12f00cc2f2ad6a2f2a94bceb7063937e945931ff8fbda9c055408e37da4`  
		Last Modified: Sat, 19 Mar 2022 20:18:49 GMT  
		Size: 41.2 MB (41162315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bd6b17f427e5b43109e77cde332787886f2d266caff26f56cb4deba881c2ac`  
		Last Modified: Sat, 19 Mar 2022 20:18:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f14abe92e4b95af2a51ba629bfffc99fdfba0929ae52c84969b4fe1e61108c`  
		Last Modified: Sun, 20 Mar 2022 20:23:17 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03e24fcf564356db942d48cfd8afdc008542f4655939fe8b19bb54237a43d0`  
		Last Modified: Sun, 20 Mar 2022 20:23:16 GMT  
		Size: 10.3 MB (10310109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58212613733fbf81b88cb6b5ac12c8f630f376f26191b877627b9b94268551bc`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 MB (1236822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04d34853a015067ef161ced6432ae8df93bbb14085e3cfcdef0f237d093fcbc`  
		Last Modified: Sun, 20 Mar 2022 20:23:18 GMT  
		Size: 32.5 MB (32479031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd07b810aa6883fe4dfcf7aee43b9ab584fb210e1ce62f0c1da7cc8a52d02ed`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f086e4aaecd8115cd259af3a39483262ba84e698ba72e4881ca65509c66b9b`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:3.11.12`

```console
$ docker pull cassandra@sha256:9dd8201f254d94380612cb918eb47b1dbe6ace6cf417f5fe890e3c15a85533fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:3.11.12` - linux; amd64

```console
$ docker pull cassandra@sha256:8517e4fc9df510d13f25d81d487996bef4b66b76e758c186602e327ebfcd0c94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129688337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d8a3f21648f7ac853ed77abb65135fce16062d8db6bd2c40b4054ae2725478`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:03 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 04:54:05 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:54:14 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:54:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:54:22 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:54:23 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:54:23 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 04:54:23 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 04:54:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:54:39 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:54:39 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:54:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 04:54:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:54:40 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:54:40 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fe65b7bd97ef856e2eb027fca02eb3a03fc15438b7e7e6c17efa9e0bad759d`  
		Last Modified: Tue, 05 Apr 2022 23:10:07 GMT  
		Size: 41.8 MB (41773798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff312975bbf79abccf177e6ba71ed66447d75914a3be6c4d0be50e20f7bd8f4`  
		Last Modified: Tue, 05 Apr 2022 23:10:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a1c8b05f0710e2ac3f734e3f3e16f7c9df946429b2fdf4c6266f717f739d`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88bdc12d10cbcbad16404e873cb5b3fe133b3f20f14abdd4716e075dce0271a`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 9.5 MB (9520751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0361372f3f252fc66be242838f3e8bedbb3ed58d550e95d8b795b7892b82bb2b`  
		Last Modified: Wed, 06 Apr 2022 04:55:39 GMT  
		Size: 1.3 MB (1316176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51e78dbddf47fe06318e20b44bd5371012835bf4654dd2471ca0562d8df6bea`  
		Last Modified: Wed, 06 Apr 2022 04:55:41 GMT  
		Size: 32.5 MB (32477989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eecbba06788d9180f126d94d98fbe197cf52ef756473081dff0af26e079587`  
		Last Modified: Wed, 06 Apr 2022 04:55:38 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ac32352b35a576b800e324c512dda93a4d7a1a5457e4e16ce9687db2bb9355`  
		Last Modified: Wed, 06 Apr 2022 04:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11.12` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:8def3259f3a7703d99f64b79d843509d78f06f0738581de9992b238c81ac9a15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121133482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dfff6e4bcf756ecd8cd193f6eb940a77b6e6d3f43c9687635b91d0cce35bff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:03:58 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:04:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:04:57 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 05:51:56 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:52:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:52:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:52:35 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:52:36 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:52:36 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:52:37 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 05:52:37 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 05:53:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:53:06 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:53:07 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 05:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:53:09 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:53:10 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571d75f300668becfcd40e9fafe6bbce8567722d68f30aeb98dc329d4823191`  
		Last Modified: Wed, 06 Apr 2022 04:13:25 GMT  
		Size: 39.5 MB (39507446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ed2119a1c0ba32f14c24749a783945a7e212b84bcdbd71e3c4aacd2065f03`  
		Last Modified: Wed, 06 Apr 2022 04:13:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b2c8d215497665a3eb09f4b09bb53efd3081bd5979ba37242ee76ff6302bf`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94f64d254a9003912150f2111698eee0d8da69a7fe06250925b26fac3fb3c7c`  
		Last Modified: Wed, 06 Apr 2022 05:55:41 GMT  
		Size: 8.9 MB (8899426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7eca9d937559fb9bb552674ca6349d6e953d8098f0c5d1943b1863f46d3871`  
		Last Modified: Wed, 06 Apr 2022 05:55:35 GMT  
		Size: 1.3 MB (1269816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab372b29b82bc7548c528b8a9eded479f5a2fcbb1c189077501db50ac4c44e`  
		Last Modified: Wed, 06 Apr 2022 05:55:44 GMT  
		Size: 32.5 MB (32479207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1dcda68a9752bd330cb5619db062c45992f67a0b1591d193aecfb77857e078`  
		Last Modified: Wed, 06 Apr 2022 05:55:33 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9478bb0878182f0d25a266ed9dbae1a04c5e1bc13ad16b7491ac7b2b46452db`  
		Last Modified: Wed, 06 Apr 2022 05:55:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11.12` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:18e1e5406e4cd6413571f972690553c8a4e2272c648a35030281d377aed7a802
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126635893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43262b9173ec9cac093bac08c9da1c0fb01b46f8c72c039695c6108b328c2ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:19:57 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 23:20:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:20:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:20:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 03:39:29 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:39:42 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:39:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:39:55 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:39:56 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:39:57 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:39:58 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:39:59 GMT
ENV CASSANDRA_VERSION=3.11.12
# Wed, 06 Apr 2022 03:40:00 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Wed, 06 Apr 2022 03:40:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:40:20 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:40:22 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 06 Apr 2022 03:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:40:24 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:40:25 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f9c4e86dbe952096d342e88426076fa51dbdbebdb4eaf88241bb2620f3c54`  
		Last Modified: Tue, 05 Apr 2022 23:25:38 GMT  
		Size: 40.8 MB (40769839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9297f966344d79f5c43f91cc3302de9ef04e5470abc1aef22b69662f5bc3cb2`  
		Last Modified: Tue, 05 Apr 2022 23:25:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353fbc349257275f1fc07f7c5890a73f5203208eacbba5562d02784b273b1249`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326611242d9919dd1e5dfa4f47d9a8d440e21538b6784606d680f09c51dff5f2`  
		Last Modified: Wed, 06 Apr 2022 03:41:51 GMT  
		Size: 9.6 MB (9550721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc745ff3919ae3c0ae1548bea5212b0b30f5847cc8d8317d397d3538719f491`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 1.0 MB (1010703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365a4074b25f41b67c6f607a83edcb7df6da6ebd5e09cb392ddccf900478fa71`  
		Last Modified: Wed, 06 Apr 2022 03:41:52 GMT  
		Size: 32.2 MB (32236540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d079081fa12e1fdce42815d042d064a44d46544e55d83140626e9a042694122`  
		Last Modified: Wed, 06 Apr 2022 03:41:49 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49585b4cf01f23d02ee4ce0cf015c753a00df3db23f4f3b9dbf7e5b06d727fda`  
		Last Modified: Wed, 06 Apr 2022 03:41:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:3.11.12` - linux; ppc64le

```console
$ docker pull cassandra@sha256:ddd6173938668416bebdc5e9f739b403d6c992377034350382c6a9996d96159d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135689235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1efe397aef8317ac23ebc26aac38c98ef09df88d92bfc06c30f9e5610589a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:10:33 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 19 Mar 2022 20:11:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:11:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:11:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sun, 20 Mar 2022 20:11:45 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:12:35 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:13:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:13:43 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:13:45 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:13:46 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:13:48 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:13:51 GMT
ENV CASSANDRA_VERSION=3.11.12
# Sun, 20 Mar 2022 20:13:55 GMT
ENV CASSANDRA_SHA512=788446e281353bd1bebab983702643a4a8a5ac39ae69d6e17c257793de7a9105884c2cd35a40873ad5a091b36cd916934ef2d51d1e347b729d5068fc54a54f01
# Sun, 20 Mar 2022 20:18:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:18:35 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:18:36 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:18:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sun, 20 Mar 2022 20:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:18:47 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:18:49 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e79e12f00cc2f2ad6a2f2a94bceb7063937e945931ff8fbda9c055408e37da4`  
		Last Modified: Sat, 19 Mar 2022 20:18:49 GMT  
		Size: 41.2 MB (41162315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bd6b17f427e5b43109e77cde332787886f2d266caff26f56cb4deba881c2ac`  
		Last Modified: Sat, 19 Mar 2022 20:18:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f14abe92e4b95af2a51ba629bfffc99fdfba0929ae52c84969b4fe1e61108c`  
		Last Modified: Sun, 20 Mar 2022 20:23:17 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03e24fcf564356db942d48cfd8afdc008542f4655939fe8b19bb54237a43d0`  
		Last Modified: Sun, 20 Mar 2022 20:23:16 GMT  
		Size: 10.3 MB (10310109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58212613733fbf81b88cb6b5ac12c8f630f376f26191b877627b9b94268551bc`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 MB (1236822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04d34853a015067ef161ced6432ae8df93bbb14085e3cfcdef0f237d093fcbc`  
		Last Modified: Sun, 20 Mar 2022 20:23:18 GMT  
		Size: 32.5 MB (32479031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd07b810aa6883fe4dfcf7aee43b9ab584fb210e1ce62f0c1da7cc8a52d02ed`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f086e4aaecd8115cd259af3a39483262ba84e698ba72e4881ca65509c66b9b`  
		Last Modified: Sun, 20 Mar 2022 20:23:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:4`

```console
$ docker pull cassandra@sha256:433e582e3587e5f7894132fdadfbdaccd6332375de78a0631fea364abb3a79b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:4` - linux; amd64

```console
$ docker pull cassandra@sha256:3538d1ce86b9b7a6c9189fbfd51b90194c6552b7c4d0932ef33f871f24a108fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150122675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737365077efac5bfff97d9a2a97bf506bb38bb65a6d4eff28613be909f780a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:32 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:06:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 04:53:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:53:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:53:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:53:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 04:53:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:53:58 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:53:58 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:53:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:53:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb433471b76621f1e03ea608408222b52c5a8d7a017eb7a00e50ed4ba1172fd9`  
		Last Modified: Tue, 05 Apr 2022 23:10:52 GMT  
		Size: 43.2 MB (43230159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b163eb312d7a79b3faf8f10447eaf91a745084448ba43b182e7eb5fe46add8`  
		Last Modified: Tue, 05 Apr 2022 23:10:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e8710ad06db7d0764b3684e1814528d9e1921a775c84cf0310114dc6d9b84a`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bd15491b211ac949fcb1173ad196eb70c3d2b3d0b2406b2fb5a5ac2d631da9`  
		Last Modified: Wed, 06 Apr 2022 04:55:22 GMT  
		Size: 10.9 MB (10945247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9fbee1f0b099389b29886dd35e61ce2ef1b9f0ae987d2c9ef4ef0c74789868`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.3 MB (1314635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc1bcea94afb8cae77dfa419e14b70badf7b14a490f4e093b974af8cf83a38`  
		Last Modified: Wed, 06 Apr 2022 04:55:23 GMT  
		Size: 50.0 MB (50033131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4ffa39fc1da7f0a44ccd95ff51a1b9ab9b1fdce1ee90fb7321bdea4418ba5`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:b06144d13a6f9d0fcd5d7d9bc383b4159e0d5ea280f7d4aa3f75cb4ceea97022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142238668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b72aa32a8f7ef16cf0d482680ecc82eb986cabac6581ab3ee722f5372a0cd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:05:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Wed, 06 Apr 2022 04:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:06:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 05:50:22 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:50:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:50:43 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:51:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:51:04 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:51:04 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 05:51:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:51:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:51:38 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:51:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:51:39 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:51:39 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa85bc24dc516a1e4fbc573adbf5cbc173fc45553d4c3d8e220ca62ed46d898`  
		Last Modified: Wed, 06 Apr 2022 04:15:28 GMT  
		Size: 41.9 MB (41850617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691e727fa9da7b8d4cbf21e9207ef94b77a88fb30e4a879d7bb8773cfaad330`  
		Last Modified: Wed, 06 Apr 2022 04:15:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ff957cbdf9f3a3723934106e75663d50c003068c775f42137783dadc42a84`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9432824afb209452317339923cb8f02258ec106c02afd0cfaa8fc1f50ae64`  
		Last Modified: Wed, 06 Apr 2022 05:55:06 GMT  
		Size: 10.1 MB (10108558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2594c50d6d39afb69628952f8cc3b85e5836fb27f09e8afa4c4e26352d66f08`  
		Last Modified: Wed, 06 Apr 2022 05:54:59 GMT  
		Size: 1.3 MB (1267901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54aa0058b91f095c05b166af4b41972663ff8406e3b69ac740a435581300287`  
		Last Modified: Wed, 06 Apr 2022 05:55:14 GMT  
		Size: 50.0 MB (50034128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d338abc0c3aa05bbf46e28e5fd073c23a0678b0fffed95fba7fd5b73028e0`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:d7cc4bc4d710bc8a70939dd766750243d1d429414d2b11bb4f57d2ea43acca28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146447897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3079f77c0f579094cf7f71948acc5b59f9d4c7ef14984bba123523ceb3b4a316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:20:35 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:21:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:21:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:21:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 03:38:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:38:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:38:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:38:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:38:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:38:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:38:43 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:38:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:38:45 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 03:38:46 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 03:39:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:39:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:39:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:39:13 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:39:14 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa473dc99209a595af291ad95e292bdbd6bc4b2856e3a87c9e1e49c414fa5622`  
		Last Modified: Tue, 05 Apr 2022 23:26:33 GMT  
		Size: 41.6 MB (41572359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64027b263996dab387273d47aade148c254a5f92db1dd6d146780c343a4928`  
		Last Modified: Tue, 05 Apr 2022 23:26:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934b62f82b38e0d42c3157041d811344dcb806c5a4ca05626d890467d518d65`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d3e4f2dd0854d38e5033bf3057e18417b054d501d54509de0b15941e976be`  
		Last Modified: Wed, 06 Apr 2022 03:41:29 GMT  
		Size: 11.0 MB (11006583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6caaef001bc247840c92f302c32f1a4efcb4e32157a73b45cddd62d04fb13d`  
		Last Modified: Wed, 06 Apr 2022 03:41:28 GMT  
		Size: 1.0 MB (1009186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc8eb95b6d4e013b8d744abe989e4d5640a1f997de559597c3eec3d1da72b84`  
		Last Modified: Wed, 06 Apr 2022 03:41:32 GMT  
		Size: 49.8 MB (49791803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a273c9bef20dcc45c85a58273986452b2db0bda1974e407cc71ba8eaf054e8e`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4` - linux; ppc64le

```console
$ docker pull cassandra@sha256:598fe3892c284e6c9a3a5b8a2a4fb326476533a610555950488376fb62bb2063
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152367585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5687a84e943caa97373dbb0b06e6cd84770068b3c9fdff0c4eef9513b477dba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:11:44 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 19 Mar 2022 20:12:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:12:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sun, 20 Mar 2022 20:02:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:03:34 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:04:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:04:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:05:03 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:05:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:05:08 GMT
ENV CASSANDRA_VERSION=4.0.3
# Sun, 20 Mar 2022 20:05:10 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Sun, 20 Mar 2022 20:11:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:11:11 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:11:13 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:11:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:11:19 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:11:23 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4f8fa3b047811e9cdc3fc57007bd4b9113a7e5b6a8ee60fa3a9885af124e25`  
		Last Modified: Sat, 19 Mar 2022 20:19:52 GMT  
		Size: 38.6 MB (38640599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9533343ab28df64b8a531e60101e2820a8c262c4fb28c0cad11425bb93f4ae`  
		Last Modified: Sat, 19 Mar 2022 20:19:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5dfa7032f074c1ac138074374f54682d53dec03e960ec5a38a723a1764622a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58de168219f06c57c03bbb24b244cb3799bd98ee22ed43b1d6fc896c6e5691bb`  
		Last Modified: Sun, 20 Mar 2022 20:22:51 GMT  
		Size: 12.0 MB (11956742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2759a6a0586fd71d0d975a5c144f2e4132bbb031ee11c3cb30a50074dac91a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 MB (1235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c9489b899ab00bdf3ffe9cefa25a8f1123dd7c4d3f6c7a89d2b7621feb8bcd`  
		Last Modified: Sun, 20 Mar 2022 20:22:54 GMT  
		Size: 50.0 MB (50034254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1205451e67f300e84e6d1b50ef325a9e9737e03e85556981f078386ed58b46`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:4.0`

```console
$ docker pull cassandra@sha256:433e582e3587e5f7894132fdadfbdaccd6332375de78a0631fea364abb3a79b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:4.0` - linux; amd64

```console
$ docker pull cassandra@sha256:3538d1ce86b9b7a6c9189fbfd51b90194c6552b7c4d0932ef33f871f24a108fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150122675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737365077efac5bfff97d9a2a97bf506bb38bb65a6d4eff28613be909f780a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:32 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:06:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 04:53:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:53:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:53:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:53:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 04:53:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:53:58 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:53:58 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:53:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:53:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb433471b76621f1e03ea608408222b52c5a8d7a017eb7a00e50ed4ba1172fd9`  
		Last Modified: Tue, 05 Apr 2022 23:10:52 GMT  
		Size: 43.2 MB (43230159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b163eb312d7a79b3faf8f10447eaf91a745084448ba43b182e7eb5fe46add8`  
		Last Modified: Tue, 05 Apr 2022 23:10:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e8710ad06db7d0764b3684e1814528d9e1921a775c84cf0310114dc6d9b84a`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bd15491b211ac949fcb1173ad196eb70c3d2b3d0b2406b2fb5a5ac2d631da9`  
		Last Modified: Wed, 06 Apr 2022 04:55:22 GMT  
		Size: 10.9 MB (10945247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9fbee1f0b099389b29886dd35e61ce2ef1b9f0ae987d2c9ef4ef0c74789868`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.3 MB (1314635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc1bcea94afb8cae77dfa419e14b70badf7b14a490f4e093b974af8cf83a38`  
		Last Modified: Wed, 06 Apr 2022 04:55:23 GMT  
		Size: 50.0 MB (50033131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4ffa39fc1da7f0a44ccd95ff51a1b9ab9b1fdce1ee90fb7321bdea4418ba5`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:b06144d13a6f9d0fcd5d7d9bc383b4159e0d5ea280f7d4aa3f75cb4ceea97022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142238668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b72aa32a8f7ef16cf0d482680ecc82eb986cabac6581ab3ee722f5372a0cd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:05:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Wed, 06 Apr 2022 04:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:06:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 05:50:22 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:50:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:50:43 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:51:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:51:04 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:51:04 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 05:51:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:51:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:51:38 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:51:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:51:39 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:51:39 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa85bc24dc516a1e4fbc573adbf5cbc173fc45553d4c3d8e220ca62ed46d898`  
		Last Modified: Wed, 06 Apr 2022 04:15:28 GMT  
		Size: 41.9 MB (41850617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691e727fa9da7b8d4cbf21e9207ef94b77a88fb30e4a879d7bb8773cfaad330`  
		Last Modified: Wed, 06 Apr 2022 04:15:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ff957cbdf9f3a3723934106e75663d50c003068c775f42137783dadc42a84`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9432824afb209452317339923cb8f02258ec106c02afd0cfaa8fc1f50ae64`  
		Last Modified: Wed, 06 Apr 2022 05:55:06 GMT  
		Size: 10.1 MB (10108558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2594c50d6d39afb69628952f8cc3b85e5836fb27f09e8afa4c4e26352d66f08`  
		Last Modified: Wed, 06 Apr 2022 05:54:59 GMT  
		Size: 1.3 MB (1267901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54aa0058b91f095c05b166af4b41972663ff8406e3b69ac740a435581300287`  
		Last Modified: Wed, 06 Apr 2022 05:55:14 GMT  
		Size: 50.0 MB (50034128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d338abc0c3aa05bbf46e28e5fd073c23a0678b0fffed95fba7fd5b73028e0`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:d7cc4bc4d710bc8a70939dd766750243d1d429414d2b11bb4f57d2ea43acca28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146447897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3079f77c0f579094cf7f71948acc5b59f9d4c7ef14984bba123523ceb3b4a316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:20:35 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:21:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:21:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:21:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 03:38:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:38:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:38:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:38:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:38:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:38:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:38:43 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:38:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:38:45 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 03:38:46 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 03:39:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:39:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:39:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:39:13 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:39:14 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa473dc99209a595af291ad95e292bdbd6bc4b2856e3a87c9e1e49c414fa5622`  
		Last Modified: Tue, 05 Apr 2022 23:26:33 GMT  
		Size: 41.6 MB (41572359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64027b263996dab387273d47aade148c254a5f92db1dd6d146780c343a4928`  
		Last Modified: Tue, 05 Apr 2022 23:26:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934b62f82b38e0d42c3157041d811344dcb806c5a4ca05626d890467d518d65`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d3e4f2dd0854d38e5033bf3057e18417b054d501d54509de0b15941e976be`  
		Last Modified: Wed, 06 Apr 2022 03:41:29 GMT  
		Size: 11.0 MB (11006583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6caaef001bc247840c92f302c32f1a4efcb4e32157a73b45cddd62d04fb13d`  
		Last Modified: Wed, 06 Apr 2022 03:41:28 GMT  
		Size: 1.0 MB (1009186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc8eb95b6d4e013b8d744abe989e4d5640a1f997de559597c3eec3d1da72b84`  
		Last Modified: Wed, 06 Apr 2022 03:41:32 GMT  
		Size: 49.8 MB (49791803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a273c9bef20dcc45c85a58273986452b2db0bda1974e407cc71ba8eaf054e8e`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0` - linux; ppc64le

```console
$ docker pull cassandra@sha256:598fe3892c284e6c9a3a5b8a2a4fb326476533a610555950488376fb62bb2063
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152367585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5687a84e943caa97373dbb0b06e6cd84770068b3c9fdff0c4eef9513b477dba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:11:44 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 19 Mar 2022 20:12:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:12:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sun, 20 Mar 2022 20:02:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:03:34 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:04:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:04:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:05:03 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:05:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:05:08 GMT
ENV CASSANDRA_VERSION=4.0.3
# Sun, 20 Mar 2022 20:05:10 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Sun, 20 Mar 2022 20:11:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:11:11 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:11:13 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:11:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:11:19 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:11:23 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4f8fa3b047811e9cdc3fc57007bd4b9113a7e5b6a8ee60fa3a9885af124e25`  
		Last Modified: Sat, 19 Mar 2022 20:19:52 GMT  
		Size: 38.6 MB (38640599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9533343ab28df64b8a531e60101e2820a8c262c4fb28c0cad11425bb93f4ae`  
		Last Modified: Sat, 19 Mar 2022 20:19:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5dfa7032f074c1ac138074374f54682d53dec03e960ec5a38a723a1764622a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58de168219f06c57c03bbb24b244cb3799bd98ee22ed43b1d6fc896c6e5691bb`  
		Last Modified: Sun, 20 Mar 2022 20:22:51 GMT  
		Size: 12.0 MB (11956742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2759a6a0586fd71d0d975a5c144f2e4132bbb031ee11c3cb30a50074dac91a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 MB (1235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c9489b899ab00bdf3ffe9cefa25a8f1123dd7c4d3f6c7a89d2b7621feb8bcd`  
		Last Modified: Sun, 20 Mar 2022 20:22:54 GMT  
		Size: 50.0 MB (50034254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1205451e67f300e84e6d1b50ef325a9e9737e03e85556981f078386ed58b46`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:4.0.3`

```console
$ docker pull cassandra@sha256:433e582e3587e5f7894132fdadfbdaccd6332375de78a0631fea364abb3a79b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:4.0.3` - linux; amd64

```console
$ docker pull cassandra@sha256:3538d1ce86b9b7a6c9189fbfd51b90194c6552b7c4d0932ef33f871f24a108fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150122675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737365077efac5bfff97d9a2a97bf506bb38bb65a6d4eff28613be909f780a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:32 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:06:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 04:53:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:53:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:53:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:53:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 04:53:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:53:58 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:53:58 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:53:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:53:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb433471b76621f1e03ea608408222b52c5a8d7a017eb7a00e50ed4ba1172fd9`  
		Last Modified: Tue, 05 Apr 2022 23:10:52 GMT  
		Size: 43.2 MB (43230159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b163eb312d7a79b3faf8f10447eaf91a745084448ba43b182e7eb5fe46add8`  
		Last Modified: Tue, 05 Apr 2022 23:10:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e8710ad06db7d0764b3684e1814528d9e1921a775c84cf0310114dc6d9b84a`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bd15491b211ac949fcb1173ad196eb70c3d2b3d0b2406b2fb5a5ac2d631da9`  
		Last Modified: Wed, 06 Apr 2022 04:55:22 GMT  
		Size: 10.9 MB (10945247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9fbee1f0b099389b29886dd35e61ce2ef1b9f0ae987d2c9ef4ef0c74789868`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.3 MB (1314635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc1bcea94afb8cae77dfa419e14b70badf7b14a490f4e093b974af8cf83a38`  
		Last Modified: Wed, 06 Apr 2022 04:55:23 GMT  
		Size: 50.0 MB (50033131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4ffa39fc1da7f0a44ccd95ff51a1b9ab9b1fdce1ee90fb7321bdea4418ba5`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0.3` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:b06144d13a6f9d0fcd5d7d9bc383b4159e0d5ea280f7d4aa3f75cb4ceea97022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142238668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b72aa32a8f7ef16cf0d482680ecc82eb986cabac6581ab3ee722f5372a0cd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:05:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Wed, 06 Apr 2022 04:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:06:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 05:50:22 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:50:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:50:43 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:51:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:51:04 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:51:04 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 05:51:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:51:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:51:38 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:51:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:51:39 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:51:39 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa85bc24dc516a1e4fbc573adbf5cbc173fc45553d4c3d8e220ca62ed46d898`  
		Last Modified: Wed, 06 Apr 2022 04:15:28 GMT  
		Size: 41.9 MB (41850617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691e727fa9da7b8d4cbf21e9207ef94b77a88fb30e4a879d7bb8773cfaad330`  
		Last Modified: Wed, 06 Apr 2022 04:15:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ff957cbdf9f3a3723934106e75663d50c003068c775f42137783dadc42a84`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9432824afb209452317339923cb8f02258ec106c02afd0cfaa8fc1f50ae64`  
		Last Modified: Wed, 06 Apr 2022 05:55:06 GMT  
		Size: 10.1 MB (10108558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2594c50d6d39afb69628952f8cc3b85e5836fb27f09e8afa4c4e26352d66f08`  
		Last Modified: Wed, 06 Apr 2022 05:54:59 GMT  
		Size: 1.3 MB (1267901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54aa0058b91f095c05b166af4b41972663ff8406e3b69ac740a435581300287`  
		Last Modified: Wed, 06 Apr 2022 05:55:14 GMT  
		Size: 50.0 MB (50034128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d338abc0c3aa05bbf46e28e5fd073c23a0678b0fffed95fba7fd5b73028e0`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0.3` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:d7cc4bc4d710bc8a70939dd766750243d1d429414d2b11bb4f57d2ea43acca28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146447897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3079f77c0f579094cf7f71948acc5b59f9d4c7ef14984bba123523ceb3b4a316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:20:35 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:21:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:21:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:21:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 03:38:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:38:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:38:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:38:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:38:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:38:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:38:43 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:38:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:38:45 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 03:38:46 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 03:39:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:39:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:39:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:39:13 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:39:14 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa473dc99209a595af291ad95e292bdbd6bc4b2856e3a87c9e1e49c414fa5622`  
		Last Modified: Tue, 05 Apr 2022 23:26:33 GMT  
		Size: 41.6 MB (41572359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64027b263996dab387273d47aade148c254a5f92db1dd6d146780c343a4928`  
		Last Modified: Tue, 05 Apr 2022 23:26:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934b62f82b38e0d42c3157041d811344dcb806c5a4ca05626d890467d518d65`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d3e4f2dd0854d38e5033bf3057e18417b054d501d54509de0b15941e976be`  
		Last Modified: Wed, 06 Apr 2022 03:41:29 GMT  
		Size: 11.0 MB (11006583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6caaef001bc247840c92f302c32f1a4efcb4e32157a73b45cddd62d04fb13d`  
		Last Modified: Wed, 06 Apr 2022 03:41:28 GMT  
		Size: 1.0 MB (1009186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc8eb95b6d4e013b8d744abe989e4d5640a1f997de559597c3eec3d1da72b84`  
		Last Modified: Wed, 06 Apr 2022 03:41:32 GMT  
		Size: 49.8 MB (49791803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a273c9bef20dcc45c85a58273986452b2db0bda1974e407cc71ba8eaf054e8e`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:4.0.3` - linux; ppc64le

```console
$ docker pull cassandra@sha256:598fe3892c284e6c9a3a5b8a2a4fb326476533a610555950488376fb62bb2063
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152367585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5687a84e943caa97373dbb0b06e6cd84770068b3c9fdff0c4eef9513b477dba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:11:44 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 19 Mar 2022 20:12:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:12:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sun, 20 Mar 2022 20:02:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:03:34 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:04:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:04:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:05:03 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:05:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:05:08 GMT
ENV CASSANDRA_VERSION=4.0.3
# Sun, 20 Mar 2022 20:05:10 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Sun, 20 Mar 2022 20:11:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:11:11 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:11:13 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:11:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:11:19 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:11:23 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4f8fa3b047811e9cdc3fc57007bd4b9113a7e5b6a8ee60fa3a9885af124e25`  
		Last Modified: Sat, 19 Mar 2022 20:19:52 GMT  
		Size: 38.6 MB (38640599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9533343ab28df64b8a531e60101e2820a8c262c4fb28c0cad11425bb93f4ae`  
		Last Modified: Sat, 19 Mar 2022 20:19:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5dfa7032f074c1ac138074374f54682d53dec03e960ec5a38a723a1764622a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58de168219f06c57c03bbb24b244cb3799bd98ee22ed43b1d6fc896c6e5691bb`  
		Last Modified: Sun, 20 Mar 2022 20:22:51 GMT  
		Size: 12.0 MB (11956742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2759a6a0586fd71d0d975a5c144f2e4132bbb031ee11c3cb30a50074dac91a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 MB (1235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c9489b899ab00bdf3ffe9cefa25a8f1123dd7c4d3f6c7a89d2b7621feb8bcd`  
		Last Modified: Sun, 20 Mar 2022 20:22:54 GMT  
		Size: 50.0 MB (50034254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1205451e67f300e84e6d1b50ef325a9e9737e03e85556981f078386ed58b46`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cassandra:latest`

```console
$ docker pull cassandra@sha256:433e582e3587e5f7894132fdadfbdaccd6332375de78a0631fea364abb3a79b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cassandra:latest` - linux; amd64

```console
$ docker pull cassandra@sha256:3538d1ce86b9b7a6c9189fbfd51b90194c6552b7c4d0932ef33f871f24a108fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150122675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737365077efac5bfff97d9a2a97bf506bb38bb65a6d4eff28613be909f780a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:06:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:06:32 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:06:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:06:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 04:53:07 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 04:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 04:53:26 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:53:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 04:53:37 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:53:37 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 04:53:38 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 04:53:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 04:53:58 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 04:53:58 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 04:53:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:53:59 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 04:53:59 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd2bc15eb1778663f55f9d16d0759ddc862631f9cf765680eb4f9dcd5894ea`  
		Last Modified: Tue, 05 Apr 2022 23:09:42 GMT  
		Size: 16.0 MB (16030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb433471b76621f1e03ea608408222b52c5a8d7a017eb7a00e50ed4ba1172fd9`  
		Last Modified: Tue, 05 Apr 2022 23:10:52 GMT  
		Size: 43.2 MB (43230159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b163eb312d7a79b3faf8f10447eaf91a745084448ba43b182e7eb5fe46add8`  
		Last Modified: Tue, 05 Apr 2022 23:10:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e8710ad06db7d0764b3684e1814528d9e1921a775c84cf0310114dc6d9b84a`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bd15491b211ac949fcb1173ad196eb70c3d2b3d0b2406b2fb5a5ac2d631da9`  
		Last Modified: Wed, 06 Apr 2022 04:55:22 GMT  
		Size: 10.9 MB (10945247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9fbee1f0b099389b29886dd35e61ce2ef1b9f0ae987d2c9ef4ef0c74789868`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.3 MB (1314635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc1bcea94afb8cae77dfa419e14b70badf7b14a490f4e093b974af8cf83a38`  
		Last Modified: Wed, 06 Apr 2022 04:55:23 GMT  
		Size: 50.0 MB (50033131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4ffa39fc1da7f0a44ccd95ff51a1b9ab9b1fdce1ee90fb7321bdea4418ba5`  
		Last Modified: Wed, 06 Apr 2022 04:55:20 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; arm variant v7

```console
$ docker pull cassandra@sha256:b06144d13a6f9d0fcd5d7d9bc383b4159e0d5ea280f7d4aa3f75cb4ceea97022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142238668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b72aa32a8f7ef16cf0d482680ecc82eb986cabac6581ab3ee722f5372a0cd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:05:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Wed, 06 Apr 2022 04:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:06:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 05:50:22 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 05:50:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 05:50:43 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 05:51:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 05:51:03 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 05:51:04 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:51:04 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 05:51:05 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 05:51:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 05:51:38 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 05:51:38 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 05:51:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 05:51:39 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 05:51:39 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa85bc24dc516a1e4fbc573adbf5cbc173fc45553d4c3d8e220ca62ed46d898`  
		Last Modified: Wed, 06 Apr 2022 04:15:28 GMT  
		Size: 41.9 MB (41850617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691e727fa9da7b8d4cbf21e9207ef94b77a88fb30e4a879d7bb8773cfaad330`  
		Last Modified: Wed, 06 Apr 2022 04:15:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2ff957cbdf9f3a3723934106e75663d50c003068c775f42137783dadc42a84`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9432824afb209452317339923cb8f02258ec106c02afd0cfaa8fc1f50ae64`  
		Last Modified: Wed, 06 Apr 2022 05:55:06 GMT  
		Size: 10.1 MB (10108558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2594c50d6d39afb69628952f8cc3b85e5836fb27f09e8afa4c4e26352d66f08`  
		Last Modified: Wed, 06 Apr 2022 05:54:59 GMT  
		Size: 1.3 MB (1267901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54aa0058b91f095c05b166af4b41972663ff8406e3b69ac740a435581300287`  
		Last Modified: Wed, 06 Apr 2022 05:55:14 GMT  
		Size: 50.0 MB (50034128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811d338abc0c3aa05bbf46e28e5fd073c23a0678b0fffed95fba7fd5b73028e0`  
		Last Modified: Wed, 06 Apr 2022 05:54:58 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; arm64 variant v8

```console
$ docker pull cassandra@sha256:d7cc4bc4d710bc8a70939dd766750243d1d429414d2b11bb4f57d2ea43acca28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146447897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3079f77c0f579094cf7f71948acc5b59f9d4c7ef14984bba123523ceb3b4a316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:20:35 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 23:21:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 23:21:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 23:21:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 03:38:17 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Wed, 06 Apr 2022 03:38:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Wed, 06 Apr 2022 03:38:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 03:38:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 03:38:41 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Wed, 06 Apr 2022 03:38:42 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Wed, 06 Apr 2022 03:38:43 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 03:38:44 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Wed, 06 Apr 2022 03:38:45 GMT
ENV CASSANDRA_VERSION=4.0.3
# Wed, 06 Apr 2022 03:38:46 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Wed, 06 Apr 2022 03:39:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Wed, 06 Apr 2022 03:39:10 GMT
VOLUME [/var/lib/cassandra]
# Wed, 06 Apr 2022 03:39:12 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Wed, 06 Apr 2022 03:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Apr 2022 03:39:13 GMT
EXPOSE 7000 7001 7199 9042 9160
# Wed, 06 Apr 2022 03:39:14 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa473dc99209a595af291ad95e292bdbd6bc4b2856e3a87c9e1e49c414fa5622`  
		Last Modified: Tue, 05 Apr 2022 23:26:33 GMT  
		Size: 41.6 MB (41572359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64027b263996dab387273d47aade148c254a5f92db1dd6d146780c343a4928`  
		Last Modified: Tue, 05 Apr 2022 23:26:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934b62f82b38e0d42c3157041d811344dcb806c5a4ca05626d890467d518d65`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d3e4f2dd0854d38e5033bf3057e18417b054d501d54509de0b15941e976be`  
		Last Modified: Wed, 06 Apr 2022 03:41:29 GMT  
		Size: 11.0 MB (11006583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6caaef001bc247840c92f302c32f1a4efcb4e32157a73b45cddd62d04fb13d`  
		Last Modified: Wed, 06 Apr 2022 03:41:28 GMT  
		Size: 1.0 MB (1009186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc8eb95b6d4e013b8d744abe989e4d5640a1f997de559597c3eec3d1da72b84`  
		Last Modified: Wed, 06 Apr 2022 03:41:32 GMT  
		Size: 49.8 MB (49791803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a273c9bef20dcc45c85a58273986452b2db0bda1974e407cc71ba8eaf054e8e`  
		Last Modified: Wed, 06 Apr 2022 03:41:27 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cassandra:latest` - linux; ppc64le

```console
$ docker pull cassandra@sha256:598fe3892c284e6c9a3a5b8a2a4fb326476533a610555950488376fb62bb2063
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152367585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5687a84e943caa97373dbb0b06e6cd84770068b3c9fdff0c4eef9513b477dba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["cassandra","-f"]`

```dockerfile
# Fri, 18 Mar 2022 00:48:28 GMT
ADD file:4f85f0964cc66c6d7dd6a29e535eb2235ff8847d3c3aa3342c74cc53710ae499 in / 
# Fri, 18 Mar 2022 00:48:34 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:09:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 20:10:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:11:44 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Sat, 19 Mar 2022 20:12:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 20:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 20:12:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sun, 20 Mar 2022 20:02:19 GMT
RUN set -eux; 	groupadd -r cassandra --gid=999; 	useradd -r -g cassandra --uid=999 cassandra
# Sun, 20 Mar 2022 20:03:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libjemalloc2 		procps 		python3 		iproute2 		numactl 	; 	rm -rf /var/lib/apt/lists/*; 	libjemalloc="$(readlink -e /usr/lib/*/libjemalloc.so.2)"; 	ln -sT "$libjemalloc" /usr/local/lib/libjemalloc.so; 	ldconfig
# Sun, 20 Mar 2022 20:03:34 GMT
ENV GOSU_VERSION=1.12
# Sun, 20 Mar 2022 20:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sun, 20 Mar 2022 20:04:52 GMT
ENV CASSANDRA_HOME=/opt/cassandra
# Sun, 20 Mar 2022 20:04:58 GMT
ENV CASSANDRA_CONF=/etc/cassandra
# Sun, 20 Mar 2022 20:05:03 GMT
ENV PATH=/opt/cassandra/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 20:05:06 GMT
ENV GPG_KEYS=CEC86BB4A0BA9D0F90397CAEF8358FA2F2833C93 	C4965EE9E3015D192CCCF2B6F758CE318D77295D 	5AED1BF378E9A19DADE1BCB34BD736A82B5C1B00 	514A2AD631A57A16DD0047EC749D6EEC0353B12C 	A26E528B271F19B9E5D8E19EA278B781FE4B2BDA 	A4C465FEA0C552561A392A61E91335D77E3E87CB 	9E66CEC6106D578D0B1EB9BFF1000962B7F6840C 	C4009872C59B49561310D966D0062876AF30F054 	B7842CDAF36E6A3214FAE35D5E85B9AE0B84C041 	3E9C876907A560ACA00964F363E9BAD215BBF5F0 	F8B7FD00E05C932991A2CD6150EE103D162C5A55
# Sun, 20 Mar 2022 20:05:08 GMT
ENV CASSANDRA_VERSION=4.0.3
# Sun, 20 Mar 2022 20:05:10 GMT
ENV CASSANDRA_SHA512=b328a6bed9bf2d92f1e44a540bf1d800e26163257ca8e69d6f43ca792aeefe5bacf61b6e5bf2cf7233e34a168ab19de96a52fb3fe82304b7749fde2d7baa81d9
# Sun, 20 Mar 2022 20:11:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget --progress=dot:giga -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'cassandra-bin.tgz' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz"; 	echo "$CASSANDRA_SHA512 *cassandra-bin.tgz" | sha512sum --check --strict -; 		ddist 'cassandra-bin.tgz.asc' "cassandra/$CASSANDRA_VERSION/apache-cassandra-$CASSANDRA_VERSION-bin.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify cassandra-bin.tgz.asc cassandra-bin.tgz; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		mkdir -p "$CASSANDRA_HOME"; 	tar --extract --file cassandra-bin.tgz --directory "$CASSANDRA_HOME" --strip-components 1; 	rm cassandra-bin.tgz*; 		[ ! -e "$CASSANDRA_CONF" ]; 	mv "$CASSANDRA_HOME/conf" "$CASSANDRA_CONF"; 	ln -sT "$CASSANDRA_CONF" "$CASSANDRA_HOME/conf"; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		ppc64el) 			if grep -q -- '^-Xss' "$CASSANDRA_CONF/jvm.options"; then 				grep -- '^-Xss256k$' "$CASSANDRA_CONF/jvm.options"; 				sed -ri 's/^-Xss256k$/-Xss512k/' "$CASSANDRA_CONF/jvm.options"; 				grep -- '^-Xss512k$' "$CASSANDRA_CONF/jvm.options"; 			elif grep -q -- '-Xss256k' "$CASSANDRA_CONF/cassandra-env.sh"; then 				sed -ri 's/-Xss256k/-Xss512k/g' "$CASSANDRA_CONF/cassandra-env.sh"; 				grep -- '-Xss512k' "$CASSANDRA_CONF/cassandra-env.sh"; 			fi; 			;; 	esac; 		mkdir -p "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chown -R cassandra:cassandra "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod 777 "$CASSANDRA_CONF" /var/lib/cassandra /var/log/cassandra; 	chmod -R a+rwX "$CASSANDRA_CONF"; 	ln -sT /var/lib/cassandra "$CASSANDRA_HOME/data"; 	ln -sT /var/log/cassandra "$CASSANDRA_HOME/logs"; 		cassandra -v
# Sun, 20 Mar 2022 20:11:11 GMT
VOLUME [/var/lib/cassandra]
# Sun, 20 Mar 2022 20:11:13 GMT
COPY file:a8d4fc10252d8783a105c235b3eef2315dbe3b0b1be0f1e4650f19fa5a56ab29 in /usr/local/bin/ 
# Sun, 20 Mar 2022 20:11:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 20 Mar 2022 20:11:19 GMT
EXPOSE 7000 7001 7199 9042 9160
# Sun, 20 Mar 2022 20:11:23 GMT
CMD ["cassandra" "-f"]
```

-	Layers:
	-	`sha256:cf1115d7b3bb72f50de3eb695005fb2c88fb88d73f535f164b306c4ab972c570`  
		Last Modified: Fri, 18 Mar 2022 00:51:19 GMT  
		Size: 33.3 MB (33292416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c83f5d2456f061b5e8436215d94c771940ee113ed327dd33b701564ffa58e`  
		Last Modified: Sat, 19 Mar 2022 20:18:16 GMT  
		Size: 17.2 MB (17205279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4f8fa3b047811e9cdc3fc57007bd4b9113a7e5b6a8ee60fa3a9885af124e25`  
		Last Modified: Sat, 19 Mar 2022 20:19:52 GMT  
		Size: 38.6 MB (38640599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9533343ab28df64b8a531e60101e2820a8c262c4fb28c0cad11425bb93f4ae`  
		Last Modified: Sat, 19 Mar 2022 20:19:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5dfa7032f074c1ac138074374f54682d53dec03e960ec5a38a723a1764622a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58de168219f06c57c03bbb24b244cb3799bd98ee22ed43b1d6fc896c6e5691bb`  
		Last Modified: Sun, 20 Mar 2022 20:22:51 GMT  
		Size: 12.0 MB (11956742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2759a6a0586fd71d0d975a5c144f2e4132bbb031ee11c3cb30a50074dac91a`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 MB (1235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c9489b899ab00bdf3ffe9cefa25a8f1123dd7c4d3f6c7a89d2b7621feb8bcd`  
		Last Modified: Sun, 20 Mar 2022 20:22:54 GMT  
		Size: 50.0 MB (50034254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1205451e67f300e84e6d1b50ef325a9e9737e03e85556981f078386ed58b46`  
		Last Modified: Sun, 20 Mar 2022 20:22:49 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
