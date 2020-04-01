<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jetty`

-	[`jetty:9`](#jetty9)
-	[`jetty:9.2.29-jre8`](#jetty9229-jre8)
-	[`jetty:9.2-jre8`](#jetty92-jre8)
-	[`jetty:9.3.28-jre8`](#jetty9328-jre8)
-	[`jetty:9.3-jre8`](#jetty93-jre8)
-	[`jetty:9.4`](#jetty94)
-	[`jetty:9.4.27`](#jetty9427)
-	[`jetty:9.4.27-jdk13`](#jetty9427-jdk13)
-	[`jetty:9.4.27-jdk13-slim`](#jetty9427-jdk13-slim)
-	[`jetty:9.4.27-jre11`](#jetty9427-jre11)
-	[`jetty:9.4.27-jre11-slim`](#jetty9427-jre11-slim)
-	[`jetty:9.4.27-jre8`](#jetty9427-jre8)
-	[`jetty:9.4-jdk13`](#jetty94-jdk13)
-	[`jetty:9.4-jdk13-slim`](#jetty94-jdk13-slim)
-	[`jetty:9.4-jre11`](#jetty94-jre11)
-	[`jetty:9.4-jre11-slim`](#jetty94-jre11-slim)
-	[`jetty:9.4-jre8`](#jetty94-jre8)
-	[`jetty:9-jdk13`](#jetty9-jdk13)
-	[`jetty:9-jdk13-slim`](#jetty9-jdk13-slim)
-	[`jetty:9-jre11`](#jetty9-jre11)
-	[`jetty:9-jre11-slim`](#jetty9-jre11-slim)
-	[`jetty:9-jre8`](#jetty9-jre8)
-	[`jetty:jdk13`](#jettyjdk13)
-	[`jetty:latest`](#jettylatest)

## `jetty:9`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.2.29-jre8`

```console
$ docker pull jetty@sha256:db00fd122ecb1e005219a8f9b6a2cde17a4ad02e7b6ec67319a1143abd7b932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.2.29-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:939cc3f0d307202ddb54dc21fb7f17a41340a1f48df06f807263174564a8283b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127755988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4236814d8b7b2ab9b6c4d8ba9cf4b0510960a6b8b8046dd3da561db79fde5129`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:23:00 GMT
ENV JETTY_VERSION=9.2.29.v20191105
# Wed, 01 Apr 2020 07:23:00 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:23:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:23:00 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:23:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:23:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.29.v20191105/jetty-distribution-9.2.29.v20191105.tar.gz
# Wed, 01 Apr 2020 07:23:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:23:04 GMT
RUN set -xe 	&& mkdir /jetty-keys         && export GNUPGHOME=/jetty-keys;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done 	&& mkdir -p "$JETTY_HOME" 	&& cd $JETTY_HOME 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr jetty.tar.gz* 	&& mkdir -p "$JETTY_BASE" 	&& cd $JETTY_BASE 	&& modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& mkdir -p "$TMPDIR" 	&& groupadd -r jetty && useradd -r -g jetty jetty 	&& chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 01 Apr 2020 07:23:04 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:23:04 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:23:04 GMT
USER jetty
# Wed, 01 Apr 2020 07:23:04 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:23:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:23:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af94a50825e8c3093290f4f30e15eafb5fcade94997f592b1101595ba0836034`  
		Last Modified: Wed, 01 Apr 2020 07:23:38 GMT  
		Size: 13.8 MB (13846883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a15a0d53eeba9f8ed1dd1646ff32e8a3fc897e326962ba3fec8c1d8c0c33510`  
		Last Modified: Wed, 01 Apr 2020 07:23:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.2-jre8`

```console
$ docker pull jetty@sha256:db00fd122ecb1e005219a8f9b6a2cde17a4ad02e7b6ec67319a1143abd7b932c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.2-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:939cc3f0d307202ddb54dc21fb7f17a41340a1f48df06f807263174564a8283b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127755988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4236814d8b7b2ab9b6c4d8ba9cf4b0510960a6b8b8046dd3da561db79fde5129`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:23:00 GMT
ENV JETTY_VERSION=9.2.29.v20191105
# Wed, 01 Apr 2020 07:23:00 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:23:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:23:00 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:23:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:23:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.29.v20191105/jetty-distribution-9.2.29.v20191105.tar.gz
# Wed, 01 Apr 2020 07:23:01 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:23:04 GMT
RUN set -xe 	&& mkdir /jetty-keys         && export GNUPGHOME=/jetty-keys;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done 	&& mkdir -p "$JETTY_HOME" 	&& cd $JETTY_HOME 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr jetty.tar.gz* 	&& mkdir -p "$JETTY_BASE" 	&& cd $JETTY_BASE 	&& modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& mkdir -p "$TMPDIR" 	&& groupadd -r jetty && useradd -r -g jetty jetty 	&& chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 01 Apr 2020 07:23:04 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:23:04 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:23:04 GMT
USER jetty
# Wed, 01 Apr 2020 07:23:04 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:23:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:23:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af94a50825e8c3093290f4f30e15eafb5fcade94997f592b1101595ba0836034`  
		Last Modified: Wed, 01 Apr 2020 07:23:38 GMT  
		Size: 13.8 MB (13846883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a15a0d53eeba9f8ed1dd1646ff32e8a3fc897e326962ba3fec8c1d8c0c33510`  
		Last Modified: Wed, 01 Apr 2020 07:23:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.3.28-jre8`

```console
$ docker pull jetty@sha256:13888c9c9b22b83fc7eee780b40a26e968c103dccc5ceaa353a80bb989379f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.3.28-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:e07fbcb2b38d2791f00fa9e7e0fc81bbe22700adf531404d9e862deced1384f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131650836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869c3f78855e43dd680cb90b746007ae2d6e652ddf56a143e9b47bb18fa69498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:22:51 GMT
ENV JETTY_VERSION=9.3.28.v20191105
# Wed, 01 Apr 2020 07:22:51 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.28.v20191105/jetty-distribution-9.3.28.v20191105.tar.gz
# Wed, 01 Apr 2020 07:22:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:55 GMT
RUN set -xe 	&& mkdir /jetty-keys         && export GNUPGHOME=/jetty-keys;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done 	&& mkdir -p "$JETTY_HOME" 	&& cd $JETTY_HOME 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr jetty.tar.gz* 	&& mkdir -p "$JETTY_BASE" 	&& cd $JETTY_BASE 	&& modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& mkdir -p "$TMPDIR" 	&& groupadd -r jetty && useradd -r -g jetty jetty 	&& chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 01 Apr 2020 07:22:55 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:56 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:56 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:56 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:56 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82ccacb39948a417b81b302059b516b8e3e3729861707b10601dafe1ccc0d24`  
		Last Modified: Wed, 01 Apr 2020 07:23:33 GMT  
		Size: 17.7 MB (17741734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e373bc07d47de1b330595538051f28b6c978e404777b75e82c355d5da34fa7d2`  
		Last Modified: Wed, 01 Apr 2020 07:23:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.3-jre8`

```console
$ docker pull jetty@sha256:13888c9c9b22b83fc7eee780b40a26e968c103dccc5ceaa353a80bb989379f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.3-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:e07fbcb2b38d2791f00fa9e7e0fc81bbe22700adf531404d9e862deced1384f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131650836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869c3f78855e43dd680cb90b746007ae2d6e652ddf56a143e9b47bb18fa69498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:22:51 GMT
ENV JETTY_VERSION=9.3.28.v20191105
# Wed, 01 Apr 2020 07:22:51 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.28.v20191105/jetty-distribution-9.3.28.v20191105.tar.gz
# Wed, 01 Apr 2020 07:22:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:55 GMT
RUN set -xe 	&& mkdir /jetty-keys         && export GNUPGHOME=/jetty-keys;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done 	&& mkdir -p "$JETTY_HOME" 	&& cd $JETTY_HOME 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr jetty.tar.gz* 	&& mkdir -p "$JETTY_BASE" 	&& cd $JETTY_BASE 	&& modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& mkdir -p "$TMPDIR" 	&& groupadd -r jetty && useradd -r -g jetty jetty 	&& chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 01 Apr 2020 07:22:55 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:56 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:56 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:56 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:56 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82ccacb39948a417b81b302059b516b8e3e3729861707b10601dafe1ccc0d24`  
		Last Modified: Wed, 01 Apr 2020 07:23:33 GMT  
		Size: 17.7 MB (17741734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e373bc07d47de1b330595538051f28b6c978e404777b75e82c355d5da34fa7d2`  
		Last Modified: Wed, 01 Apr 2020 07:23:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.27`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4.27` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.27-jdk13`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4.27-jdk13` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.27-jdk13-slim`

```console
$ docker pull jetty@sha256:1173c0983b165e57669b6881c75619642dfe3baf150fa73e2619fdc386bf474e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4.27-jdk13-slim` - linux; amd64

```console
$ docker pull jetty@sha256:36ae70cf819fce461383a33d06e8afbcb2884793fdb085eb5baf4ea215eb8758
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236975018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbc63ee63b891f126ec24c56bec48445094be161afed3e3526464a893d01b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:19:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Wed, 26 Feb 2020 20:19:24 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:19:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_VERSION=13.0.2
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Wed, 26 Feb 2020 20:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:19:47 GMT
CMD ["jshell"]
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 28 Feb 2020 22:28:32 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 28 Feb 2020 22:28:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2020 22:28:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Fri, 28 Feb 2020 22:28:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Fri, 28 Feb 2020 22:28:46 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 28 Feb 2020 22:28:46 GMT
WORKDIR /var/lib/jetty
# Fri, 28 Feb 2020 22:28:47 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Fri, 28 Feb 2020 22:28:47 GMT
USER jetty
# Fri, 28 Feb 2020 22:28:47 GMT
EXPOSE 8080
# Fri, 28 Feb 2020 22:28:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2020 22:28:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4874c5772968dcab87c114bee2baf2c7e9a06dda36e63bdfeab71bd4d6f02890`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 3.2 MB (3249096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a0f4652d3adec4d455dd21ebcb5a6a4fa159dd2fb0350a661db90355ef66f7`  
		Last Modified: Wed, 26 Feb 2020 20:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fff129ced58518df785f81c0a069ce3089f82742923c6b75c5332b51592510`  
		Last Modified: Wed, 26 Feb 2020 20:26:09 GMT  
		Size: 196.7 MB (196675216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca51a886b8455ec5d55e08df270cb6ce33383fbffd5d756e9dacd60d52841d37`  
		Last Modified: Fri, 28 Feb 2020 22:29:33 GMT  
		Size: 10.0 MB (9957260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc46c9cf35624036939a30e192784c7a5ac5389d3e5f75c5cf5950d3226a8fd6`  
		Last Modified: Fri, 28 Feb 2020 22:29:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.27-jre11`

```console
$ docker pull jetty@sha256:bae51bd52f6ba18a349f9779cd35c68a88973286b99e5221b49b1adc4cf0b934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9.4.27-jre11` - linux; amd64

```console
$ docker pull jetty@sha256:81d868c694ff7a361b71ba619b0c61b12bbe209f3f8addf4bde1f3beb09b2a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125295268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e2fc3f355754885c033d0f9df1360ff3fc22aea778241f8594be2c59d5d94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:29 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:29 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:30 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:30 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:30 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acb3faf5fa85df74c5057abb2e439e46ad84d5ad3f0f5c32029c676253004c9`  
		Last Modified: Wed, 01 Apr 2020 07:23:22 GMT  
		Size: 9.7 MB (9679415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6e70711740a045f787e3b45b110a5c064b81a90e5c502ec8e2a1c247d8946`  
		Last Modified: Wed, 01 Apr 2020 07:23:21 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4.27-jre11` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6ba9d226aa804b78d975b2857972f283378e176d0776081cc18339924cc055be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123017415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bc1d4876d8c1acdc7ab54ac08ad0321dc7dec88171563d750993e196c08d78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:07 GMT
ADD file:d0df7ac13226f8d35c078941a20d8a465b09a4e226c5ca37709fa23599cd56dc in / 
# Tue, 31 Mar 2020 02:05:09 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:33:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:33:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 20:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:40:17 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 20:40:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 20:40:18 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:40:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 20:40:22 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 20:40:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 20:40:23 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 20:40:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Tue, 31 Mar 2020 20:54:34 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 31 Mar 2020 20:54:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Mar 2020 20:54:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Mar 2020 20:54:36 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Mar 2020 20:54:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:54:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 31 Mar 2020 20:54:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 31 Mar 2020 20:54:44 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Mar 2020 20:54:45 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Mar 2020 20:54:46 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 31 Mar 2020 20:54:46 GMT
USER jetty
# Tue, 31 Mar 2020 20:54:47 GMT
EXPOSE 8080
# Tue, 31 Mar 2020 20:54:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Mar 2020 20:54:48 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5767fbcc7692f25971758138978eed9bd3add831a79561cd58bf281e60a5159f`  
		Last Modified: Tue, 31 Mar 2020 02:11:54 GMT  
		Size: 49.2 MB (49169998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b632de0573ae234fd668631d1aba00e13ea3a66cdd1732e58533b119480e4e9`  
		Last Modified: Tue, 31 Mar 2020 04:46:42 GMT  
		Size: 7.7 MB (7681336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f852028d4482a56b904b98dfe16c9781cb55380b9a7f6b6cf59622e3ef0de0`  
		Last Modified: Tue, 31 Mar 2020 04:46:38 GMT  
		Size: 10.0 MB (9983948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63afb8f982cf457f13a6f2c5ceea33ffa8315f0e7efa0960e0d46af9f0d8b5`  
		Last Modified: Tue, 31 Mar 2020 20:41:58 GMT  
		Size: 5.5 MB (5504367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ac299e82e885c22fdc6324775b8b3b119d15c21538f03b6c2c97f7cbb55c5`  
		Last Modified: Tue, 31 Mar 2020 20:41:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821205250f444eec5b66fd0a6a724149775aa19c4f7c4a5d7bb890a45746717`  
		Last Modified: Tue, 31 Mar 2020 20:42:08 GMT  
		Size: 41.0 MB (40996651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe20f7391117a10902bbf562107cf5460f218a7e33bcb9bd97b31f0573e66d`  
		Last Modified: Tue, 31 Mar 2020 20:55:13 GMT  
		Size: 9.7 MB (9679486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54af02305088c4d508c3cf312f12229b4088e36246bf020f5b030610d537828b`  
		Last Modified: Tue, 31 Mar 2020 20:55:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.27-jre11-slim`

```console
$ docker pull jetty@sha256:984d138cadf8471babeb4d5bb3b12b4be76df0b26c395cebb9442dcb61533d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9.4.27-jre11-slim` - linux; amd64

```console
$ docker pull jetty@sha256:089d27d019e43327441e56ca2d32d30f56d6d76c220176544408d0b9146cdc1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82473905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e4bb657ff7e7bd25ed90e58342f77441fae9c3f6ccd150423dab01417c3cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:31:09 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 01:33:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 01:33:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 01:33:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 01:33:15 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 01:33:46 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 01:33:46 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 01:33:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 07:22:03 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:19 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:19 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:19 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:19 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:20 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e36ba391601ebce2c22f34982f56ce9236ca9cfdef13b2bc60457881d84e8`  
		Last Modified: Tue, 31 Mar 2020 01:35:26 GMT  
		Size: 3.2 MB (3249089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f5150f7beb631588d1fd1dc420e1529f2db039f6c330d8cad4d7fc17fe51e5`  
		Last Modified: Tue, 31 Mar 2020 01:36:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be7a8683667eb197d08e2e4bb4989fa299e1cdcc681a771902483bfbd724f0f`  
		Last Modified: Tue, 31 Mar 2020 01:37:13 GMT  
		Size: 42.2 MB (42172502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f957f41afae6be1154dc432db6a75a02efb8649d4631a6d9c47d3da5e584d8`  
		Last Modified: Wed, 01 Apr 2020 07:23:17 GMT  
		Size: 10.0 MB (9958824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b40c05e88a1a96ab80d070af8955d4a24533c355cfe830c004eb130185c9cdd`  
		Last Modified: Wed, 01 Apr 2020 07:23:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4.27-jre11-slim` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2f792774dfb48c32f5efba874919ac61d7887902363095fb60ee848492404f9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80185165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4758f10250aa1034ee74a23d1ba99531da961a420a4d54453e4d792b613fcb25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:47:39 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 03:47:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 03:47:41 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 03:47:44 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 03:47:45 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 03:48:47 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 03:48:47 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 03:49:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Tue, 31 Mar 2020 20:53:10 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 31 Mar 2020 20:53:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Mar 2020 20:53:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Mar 2020 20:53:20 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Mar 2020 20:53:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:53:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 31 Mar 2020 20:53:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 31 Mar 2020 20:54:14 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Mar 2020 20:54:15 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Mar 2020 20:54:16 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 31 Mar 2020 20:54:16 GMT
USER jetty
# Tue, 31 Mar 2020 20:54:17 GMT
EXPOSE 8080
# Tue, 31 Mar 2020 20:54:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Mar 2020 20:54:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94531fd03e27a9de9cc97ba8ac3e4779fd0396c9d115a52f7fe459b8bff1eb9`  
		Last Modified: Tue, 31 Mar 2020 03:49:42 GMT  
		Size: 3.1 MB (3101189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f099899933d1e166be4ac82b1101a984d575ad5b8fe8660d5175e53ea0efa`  
		Last Modified: Tue, 31 Mar 2020 03:49:41 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447e5e868c8eaef5b9009e7c422a374738ae27359026467367755b01fae2f01`  
		Last Modified: Tue, 31 Mar 2020 03:50:46 GMT  
		Size: 41.3 MB (41271733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68444a20d9c20b143ac4134b43673b098d8ef76f05b7778ff67abada21edfbb1`  
		Last Modified: Tue, 31 Mar 2020 20:54:59 GMT  
		Size: 10.0 MB (9958971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcd9cd42c852b579f80f092e0ec3cd705881341828f297aac078999526e9a31`  
		Last Modified: Tue, 31 Mar 2020 20:54:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.27-jre8`

```console
$ docker pull jetty@sha256:9df77303ee185d2aa621cc704f9adb02359ccd8b43775feff99c1d79cf0a6e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4.27-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:f4a1a5337546c8eb8e97450b2174994d8f55b2a6b865d8bb308d26c77765cd50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123588515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8814a4f48b4e32ed4aaae57ee6d2774905e69ed569991db26ef06ce110ee423`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:22:34 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:39 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:40 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:40 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:40 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:40 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:41 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0242f3c63707290544d3b147fee941350befb14e8eb23158dfa0ff4e384cab9`  
		Last Modified: Wed, 01 Apr 2020 07:23:26 GMT  
		Size: 9.7 MB (9679410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7701495cfb58aab26d6631294dce8d7794e433db5390149d34e01447dcc8dfa1`  
		Last Modified: Wed, 01 Apr 2020 07:23:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4-jdk13`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4-jdk13` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4-jdk13-slim`

```console
$ docker pull jetty@sha256:1173c0983b165e57669b6881c75619642dfe3baf150fa73e2619fdc386bf474e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4-jdk13-slim` - linux; amd64

```console
$ docker pull jetty@sha256:36ae70cf819fce461383a33d06e8afbcb2884793fdb085eb5baf4ea215eb8758
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236975018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbc63ee63b891f126ec24c56bec48445094be161afed3e3526464a893d01b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:19:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Wed, 26 Feb 2020 20:19:24 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:19:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_VERSION=13.0.2
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Wed, 26 Feb 2020 20:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:19:47 GMT
CMD ["jshell"]
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 28 Feb 2020 22:28:32 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 28 Feb 2020 22:28:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2020 22:28:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Fri, 28 Feb 2020 22:28:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Fri, 28 Feb 2020 22:28:46 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 28 Feb 2020 22:28:46 GMT
WORKDIR /var/lib/jetty
# Fri, 28 Feb 2020 22:28:47 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Fri, 28 Feb 2020 22:28:47 GMT
USER jetty
# Fri, 28 Feb 2020 22:28:47 GMT
EXPOSE 8080
# Fri, 28 Feb 2020 22:28:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2020 22:28:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4874c5772968dcab87c114bee2baf2c7e9a06dda36e63bdfeab71bd4d6f02890`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 3.2 MB (3249096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a0f4652d3adec4d455dd21ebcb5a6a4fa159dd2fb0350a661db90355ef66f7`  
		Last Modified: Wed, 26 Feb 2020 20:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fff129ced58518df785f81c0a069ce3089f82742923c6b75c5332b51592510`  
		Last Modified: Wed, 26 Feb 2020 20:26:09 GMT  
		Size: 196.7 MB (196675216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca51a886b8455ec5d55e08df270cb6ce33383fbffd5d756e9dacd60d52841d37`  
		Last Modified: Fri, 28 Feb 2020 22:29:33 GMT  
		Size: 10.0 MB (9957260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc46c9cf35624036939a30e192784c7a5ac5389d3e5f75c5cf5950d3226a8fd6`  
		Last Modified: Fri, 28 Feb 2020 22:29:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4-jre11`

```console
$ docker pull jetty@sha256:bae51bd52f6ba18a349f9779cd35c68a88973286b99e5221b49b1adc4cf0b934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9.4-jre11` - linux; amd64

```console
$ docker pull jetty@sha256:81d868c694ff7a361b71ba619b0c61b12bbe209f3f8addf4bde1f3beb09b2a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125295268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e2fc3f355754885c033d0f9df1360ff3fc22aea778241f8594be2c59d5d94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:29 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:29 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:30 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:30 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:30 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acb3faf5fa85df74c5057abb2e439e46ad84d5ad3f0f5c32029c676253004c9`  
		Last Modified: Wed, 01 Apr 2020 07:23:22 GMT  
		Size: 9.7 MB (9679415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6e70711740a045f787e3b45b110a5c064b81a90e5c502ec8e2a1c247d8946`  
		Last Modified: Wed, 01 Apr 2020 07:23:21 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6ba9d226aa804b78d975b2857972f283378e176d0776081cc18339924cc055be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123017415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bc1d4876d8c1acdc7ab54ac08ad0321dc7dec88171563d750993e196c08d78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:07 GMT
ADD file:d0df7ac13226f8d35c078941a20d8a465b09a4e226c5ca37709fa23599cd56dc in / 
# Tue, 31 Mar 2020 02:05:09 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:33:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:33:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 20:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:40:17 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 20:40:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 20:40:18 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:40:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 20:40:22 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 20:40:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 20:40:23 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 20:40:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Tue, 31 Mar 2020 20:54:34 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 31 Mar 2020 20:54:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Mar 2020 20:54:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Mar 2020 20:54:36 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Mar 2020 20:54:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:54:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 31 Mar 2020 20:54:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 31 Mar 2020 20:54:44 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Mar 2020 20:54:45 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Mar 2020 20:54:46 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 31 Mar 2020 20:54:46 GMT
USER jetty
# Tue, 31 Mar 2020 20:54:47 GMT
EXPOSE 8080
# Tue, 31 Mar 2020 20:54:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Mar 2020 20:54:48 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5767fbcc7692f25971758138978eed9bd3add831a79561cd58bf281e60a5159f`  
		Last Modified: Tue, 31 Mar 2020 02:11:54 GMT  
		Size: 49.2 MB (49169998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b632de0573ae234fd668631d1aba00e13ea3a66cdd1732e58533b119480e4e9`  
		Last Modified: Tue, 31 Mar 2020 04:46:42 GMT  
		Size: 7.7 MB (7681336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f852028d4482a56b904b98dfe16c9781cb55380b9a7f6b6cf59622e3ef0de0`  
		Last Modified: Tue, 31 Mar 2020 04:46:38 GMT  
		Size: 10.0 MB (9983948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63afb8f982cf457f13a6f2c5ceea33ffa8315f0e7efa0960e0d46af9f0d8b5`  
		Last Modified: Tue, 31 Mar 2020 20:41:58 GMT  
		Size: 5.5 MB (5504367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ac299e82e885c22fdc6324775b8b3b119d15c21538f03b6c2c97f7cbb55c5`  
		Last Modified: Tue, 31 Mar 2020 20:41:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821205250f444eec5b66fd0a6a724149775aa19c4f7c4a5d7bb890a45746717`  
		Last Modified: Tue, 31 Mar 2020 20:42:08 GMT  
		Size: 41.0 MB (40996651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe20f7391117a10902bbf562107cf5460f218a7e33bcb9bd97b31f0573e66d`  
		Last Modified: Tue, 31 Mar 2020 20:55:13 GMT  
		Size: 9.7 MB (9679486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54af02305088c4d508c3cf312f12229b4088e36246bf020f5b030610d537828b`  
		Last Modified: Tue, 31 Mar 2020 20:55:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4-jre11-slim`

```console
$ docker pull jetty@sha256:984d138cadf8471babeb4d5bb3b12b4be76df0b26c395cebb9442dcb61533d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9.4-jre11-slim` - linux; amd64

```console
$ docker pull jetty@sha256:089d27d019e43327441e56ca2d32d30f56d6d76c220176544408d0b9146cdc1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82473905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e4bb657ff7e7bd25ed90e58342f77441fae9c3f6ccd150423dab01417c3cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:31:09 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 01:33:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 01:33:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 01:33:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 01:33:15 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 01:33:46 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 01:33:46 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 01:33:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 07:22:03 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:19 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:19 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:19 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:19 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:20 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e36ba391601ebce2c22f34982f56ce9236ca9cfdef13b2bc60457881d84e8`  
		Last Modified: Tue, 31 Mar 2020 01:35:26 GMT  
		Size: 3.2 MB (3249089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f5150f7beb631588d1fd1dc420e1529f2db039f6c330d8cad4d7fc17fe51e5`  
		Last Modified: Tue, 31 Mar 2020 01:36:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be7a8683667eb197d08e2e4bb4989fa299e1cdcc681a771902483bfbd724f0f`  
		Last Modified: Tue, 31 Mar 2020 01:37:13 GMT  
		Size: 42.2 MB (42172502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f957f41afae6be1154dc432db6a75a02efb8649d4631a6d9c47d3da5e584d8`  
		Last Modified: Wed, 01 Apr 2020 07:23:17 GMT  
		Size: 10.0 MB (9958824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b40c05e88a1a96ab80d070af8955d4a24533c355cfe830c004eb130185c9cdd`  
		Last Modified: Wed, 01 Apr 2020 07:23:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11-slim` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2f792774dfb48c32f5efba874919ac61d7887902363095fb60ee848492404f9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80185165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4758f10250aa1034ee74a23d1ba99531da961a420a4d54453e4d792b613fcb25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:47:39 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 03:47:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 03:47:41 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 03:47:44 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 03:47:45 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 03:48:47 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 03:48:47 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 03:49:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Tue, 31 Mar 2020 20:53:10 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 31 Mar 2020 20:53:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Mar 2020 20:53:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Mar 2020 20:53:20 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Mar 2020 20:53:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:53:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 31 Mar 2020 20:53:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 31 Mar 2020 20:54:14 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Mar 2020 20:54:15 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Mar 2020 20:54:16 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 31 Mar 2020 20:54:16 GMT
USER jetty
# Tue, 31 Mar 2020 20:54:17 GMT
EXPOSE 8080
# Tue, 31 Mar 2020 20:54:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Mar 2020 20:54:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94531fd03e27a9de9cc97ba8ac3e4779fd0396c9d115a52f7fe459b8bff1eb9`  
		Last Modified: Tue, 31 Mar 2020 03:49:42 GMT  
		Size: 3.1 MB (3101189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f099899933d1e166be4ac82b1101a984d575ad5b8fe8660d5175e53ea0efa`  
		Last Modified: Tue, 31 Mar 2020 03:49:41 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447e5e868c8eaef5b9009e7c422a374738ae27359026467367755b01fae2f01`  
		Last Modified: Tue, 31 Mar 2020 03:50:46 GMT  
		Size: 41.3 MB (41271733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68444a20d9c20b143ac4134b43673b098d8ef76f05b7778ff67abada21edfbb1`  
		Last Modified: Tue, 31 Mar 2020 20:54:59 GMT  
		Size: 10.0 MB (9958971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcd9cd42c852b579f80f092e0ec3cd705881341828f297aac078999526e9a31`  
		Last Modified: Tue, 31 Mar 2020 20:54:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4-jre8`

```console
$ docker pull jetty@sha256:9df77303ee185d2aa621cc704f9adb02359ccd8b43775feff99c1d79cf0a6e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9.4-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:f4a1a5337546c8eb8e97450b2174994d8f55b2a6b865d8bb308d26c77765cd50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123588515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8814a4f48b4e32ed4aaae57ee6d2774905e69ed569991db26ef06ce110ee423`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:22:34 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:39 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:40 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:40 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:40 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:40 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:41 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0242f3c63707290544d3b147fee941350befb14e8eb23158dfa0ff4e384cab9`  
		Last Modified: Wed, 01 Apr 2020 07:23:26 GMT  
		Size: 9.7 MB (9679410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7701495cfb58aab26d6631294dce8d7794e433db5390149d34e01447dcc8dfa1`  
		Last Modified: Wed, 01 Apr 2020 07:23:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jdk13`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9-jdk13` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jdk13-slim`

```console
$ docker pull jetty@sha256:1173c0983b165e57669b6881c75619642dfe3baf150fa73e2619fdc386bf474e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9-jdk13-slim` - linux; amd64

```console
$ docker pull jetty@sha256:36ae70cf819fce461383a33d06e8afbcb2884793fdb085eb5baf4ea215eb8758
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236975018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbc63ee63b891f126ec24c56bec48445094be161afed3e3526464a893d01b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:19:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Wed, 26 Feb 2020 20:19:24 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:19:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_VERSION=13.0.2
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Wed, 26 Feb 2020 20:19:25 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Wed, 26 Feb 2020 20:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:19:47 GMT
CMD ["jshell"]
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 28 Feb 2020 22:28:32 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 28 Feb 2020 22:28:32 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 28 Feb 2020 22:28:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Feb 2020 22:28:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Fri, 28 Feb 2020 22:28:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Fri, 28 Feb 2020 22:28:46 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Fri, 28 Feb 2020 22:28:46 GMT
WORKDIR /var/lib/jetty
# Fri, 28 Feb 2020 22:28:47 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Fri, 28 Feb 2020 22:28:47 GMT
USER jetty
# Fri, 28 Feb 2020 22:28:47 GMT
EXPOSE 8080
# Fri, 28 Feb 2020 22:28:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 28 Feb 2020 22:28:47 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4874c5772968dcab87c114bee2baf2c7e9a06dda36e63bdfeab71bd4d6f02890`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 3.2 MB (3249096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a0f4652d3adec4d455dd21ebcb5a6a4fa159dd2fb0350a661db90355ef66f7`  
		Last Modified: Wed, 26 Feb 2020 20:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fff129ced58518df785f81c0a069ce3089f82742923c6b75c5332b51592510`  
		Last Modified: Wed, 26 Feb 2020 20:26:09 GMT  
		Size: 196.7 MB (196675216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca51a886b8455ec5d55e08df270cb6ce33383fbffd5d756e9dacd60d52841d37`  
		Last Modified: Fri, 28 Feb 2020 22:29:33 GMT  
		Size: 10.0 MB (9957260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc46c9cf35624036939a30e192784c7a5ac5389d3e5f75c5cf5950d3226a8fd6`  
		Last Modified: Fri, 28 Feb 2020 22:29:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jre11`

```console
$ docker pull jetty@sha256:bae51bd52f6ba18a349f9779cd35c68a88973286b99e5221b49b1adc4cf0b934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jre11` - linux; amd64

```console
$ docker pull jetty@sha256:81d868c694ff7a361b71ba619b0c61b12bbe209f3f8addf4bde1f3beb09b2a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125295268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e2fc3f355754885c033d0f9df1360ff3fc22aea778241f8594be2c59d5d94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:25 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:29 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:29 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:30 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:30 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:30 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:30 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acb3faf5fa85df74c5057abb2e439e46ad84d5ad3f0f5c32029c676253004c9`  
		Last Modified: Wed, 01 Apr 2020 07:23:22 GMT  
		Size: 9.7 MB (9679415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6e70711740a045f787e3b45b110a5c064b81a90e5c502ec8e2a1c247d8946`  
		Last Modified: Wed, 01 Apr 2020 07:23:21 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:6ba9d226aa804b78d975b2857972f283378e176d0776081cc18339924cc055be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123017415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bc1d4876d8c1acdc7ab54ac08ad0321dc7dec88171563d750993e196c08d78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:07 GMT
ADD file:d0df7ac13226f8d35c078941a20d8a465b09a4e226c5ca37709fa23599cd56dc in / 
# Tue, 31 Mar 2020 02:05:09 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:33:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:33:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 20:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 20:40:17 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 20:40:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 20:40:18 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:40:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 20:40:22 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 20:40:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 20:40:23 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 20:40:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Tue, 31 Mar 2020 20:54:34 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 31 Mar 2020 20:54:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Mar 2020 20:54:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Mar 2020 20:54:36 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Mar 2020 20:54:36 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:54:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 31 Mar 2020 20:54:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 31 Mar 2020 20:54:44 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Mar 2020 20:54:45 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Mar 2020 20:54:46 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 31 Mar 2020 20:54:46 GMT
USER jetty
# Tue, 31 Mar 2020 20:54:47 GMT
EXPOSE 8080
# Tue, 31 Mar 2020 20:54:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Mar 2020 20:54:48 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5767fbcc7692f25971758138978eed9bd3add831a79561cd58bf281e60a5159f`  
		Last Modified: Tue, 31 Mar 2020 02:11:54 GMT  
		Size: 49.2 MB (49169998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b632de0573ae234fd668631d1aba00e13ea3a66cdd1732e58533b119480e4e9`  
		Last Modified: Tue, 31 Mar 2020 04:46:42 GMT  
		Size: 7.7 MB (7681336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f852028d4482a56b904b98dfe16c9781cb55380b9a7f6b6cf59622e3ef0de0`  
		Last Modified: Tue, 31 Mar 2020 04:46:38 GMT  
		Size: 10.0 MB (9983948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63afb8f982cf457f13a6f2c5ceea33ffa8315f0e7efa0960e0d46af9f0d8b5`  
		Last Modified: Tue, 31 Mar 2020 20:41:58 GMT  
		Size: 5.5 MB (5504367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ac299e82e885c22fdc6324775b8b3b119d15c21538f03b6c2c97f7cbb55c5`  
		Last Modified: Tue, 31 Mar 2020 20:41:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821205250f444eec5b66fd0a6a724149775aa19c4f7c4a5d7bb890a45746717`  
		Last Modified: Tue, 31 Mar 2020 20:42:08 GMT  
		Size: 41.0 MB (40996651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe20f7391117a10902bbf562107cf5460f218a7e33bcb9bd97b31f0573e66d`  
		Last Modified: Tue, 31 Mar 2020 20:55:13 GMT  
		Size: 9.7 MB (9679486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54af02305088c4d508c3cf312f12229b4088e36246bf020f5b030610d537828b`  
		Last Modified: Tue, 31 Mar 2020 20:55:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jre11-slim`

```console
$ docker pull jetty@sha256:984d138cadf8471babeb4d5bb3b12b4be76df0b26c395cebb9442dcb61533d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jre11-slim` - linux; amd64

```console
$ docker pull jetty@sha256:089d27d019e43327441e56ca2d32d30f56d6d76c220176544408d0b9146cdc1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82473905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e4bb657ff7e7bd25ed90e58342f77441fae9c3f6ccd150423dab01417c3cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:31:09 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 01:33:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 01:33:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 01:33:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 01:33:15 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 01:33:46 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 01:33:46 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 01:33:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 07:22:03 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:04 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:19 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:19 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:19 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:19 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:20 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:20 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e36ba391601ebce2c22f34982f56ce9236ca9cfdef13b2bc60457881d84e8`  
		Last Modified: Tue, 31 Mar 2020 01:35:26 GMT  
		Size: 3.2 MB (3249089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f5150f7beb631588d1fd1dc420e1529f2db039f6c330d8cad4d7fc17fe51e5`  
		Last Modified: Tue, 31 Mar 2020 01:36:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be7a8683667eb197d08e2e4bb4989fa299e1cdcc681a771902483bfbd724f0f`  
		Last Modified: Tue, 31 Mar 2020 01:37:13 GMT  
		Size: 42.2 MB (42172502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f957f41afae6be1154dc432db6a75a02efb8649d4631a6d9c47d3da5e584d8`  
		Last Modified: Wed, 01 Apr 2020 07:23:17 GMT  
		Size: 10.0 MB (9958824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b40c05e88a1a96ab80d070af8955d4a24533c355cfe830c004eb130185c9cdd`  
		Last Modified: Wed, 01 Apr 2020 07:23:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11-slim` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2f792774dfb48c32f5efba874919ac61d7887902363095fb60ee848492404f9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80185165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4758f10250aa1034ee74a23d1ba99531da961a420a4d54453e4d792b613fcb25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:47:39 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 03:47:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 03:47:41 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 03:47:44 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 03:47:45 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 03:48:47 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 03:48:47 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 03:49:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Tue, 31 Mar 2020 20:53:10 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 31 Mar 2020 20:53:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Mar 2020 20:53:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Mar 2020 20:53:20 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Mar 2020 20:53:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 20:53:26 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 31 Mar 2020 20:53:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 31 Mar 2020 20:54:14 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 		gnupg 		curl 		;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Mar 2020 20:54:15 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Mar 2020 20:54:16 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 31 Mar 2020 20:54:16 GMT
USER jetty
# Tue, 31 Mar 2020 20:54:17 GMT
EXPOSE 8080
# Tue, 31 Mar 2020 20:54:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Mar 2020 20:54:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94531fd03e27a9de9cc97ba8ac3e4779fd0396c9d115a52f7fe459b8bff1eb9`  
		Last Modified: Tue, 31 Mar 2020 03:49:42 GMT  
		Size: 3.1 MB (3101189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f099899933d1e166be4ac82b1101a984d575ad5b8fe8660d5175e53ea0efa`  
		Last Modified: Tue, 31 Mar 2020 03:49:41 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447e5e868c8eaef5b9009e7c422a374738ae27359026467367755b01fae2f01`  
		Last Modified: Tue, 31 Mar 2020 03:50:46 GMT  
		Size: 41.3 MB (41271733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68444a20d9c20b143ac4134b43673b098d8ef76f05b7778ff67abada21edfbb1`  
		Last Modified: Tue, 31 Mar 2020 20:54:59 GMT  
		Size: 10.0 MB (9958971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcd9cd42c852b579f80f092e0ec3cd705881341828f297aac078999526e9a31`  
		Last Modified: Tue, 31 Mar 2020 20:54:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jre8`

```console
$ docker pull jetty@sha256:9df77303ee185d2aa621cc704f9adb02359ccd8b43775feff99c1d79cf0a6e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:9-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:f4a1a5337546c8eb8e97450b2174994d8f55b2a6b865d8bb308d26c77765cd50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123588515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8814a4f48b4e32ed4aaae57ee6d2774905e69ed569991db26ef06ce110ee423`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 07:22:34 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Wed, 01 Apr 2020 07:22:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Apr 2020 07:22:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Wed, 01 Apr 2020 07:22:35 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 01 Apr 2020 07:22:39 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 01 Apr 2020 07:22:40 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Apr 2020 07:22:40 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Wed, 01 Apr 2020 07:22:40 GMT
USER jetty
# Wed, 01 Apr 2020 07:22:40 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 07:22:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2020 07:22:41 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0242f3c63707290544d3b147fee941350befb14e8eb23158dfa0ff4e384cab9`  
		Last Modified: Wed, 01 Apr 2020 07:23:26 GMT  
		Size: 9.7 MB (9679410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7701495cfb58aab26d6631294dce8d7794e433db5390149d34e01447dcc8dfa1`  
		Last Modified: Wed, 01 Apr 2020 07:23:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:jdk13`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:jdk13` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:latest`

```console
$ docker pull jetty@sha256:f7fc4aa105f1cf8a917be9315dd058ce4851a7ff05be8150be6a341a3bd63203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:latest` - linux; amd64

```console
$ docker pull jetty@sha256:bee9ba39ac04c321af19ed894f5dbf9688e9564fdebc710cedb9b4c476e99cda
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263550376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7100647695e3917da6a103cd4852e50c22f3f3fdc4ea6a51f9c1dfdd8daaf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-13
# Tue, 10 Mar 2020 02:40:08 GMT
ENV PATH=/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_VERSION=13.0.2
# Tue, 10 Mar 2020 02:40:08 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:40:09 GMT
ENV JAVA_SHA256=acc7a6aabced44e62ec3b83e3b5959df2b1aa6b3d610d58ee45f0c21a7821a71
# Tue, 10 Mar 2020 02:40:34 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:40:34 GMT
CMD ["jshell"]
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_VERSION=9.4.27.v20200227
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 10 Mar 2020 22:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 10 Mar 2020 22:58:55 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-13/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.27.v20200227/jetty-home-9.4.27.v20200227.tar.gz
# Tue, 10 Mar 2020 22:58:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Tue, 10 Mar 2020 22:58:59 GMT
RUN set -xe ;         export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ;         for key in $JETTY_GPG_KEYS; do                 for server in                         ha.pool.sks-keyservers.net                         p80.pool.sks-keyservers.net:80                         ipv4.pool.sks-keyservers.net                         pgp.mit.edu ;                 do                         if gpg --batch --keyserver "$server" --recv-keys "$key"; then                                 break;                         fi;                 done;         done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 10 Mar 2020 22:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 10 Mar 2020 22:58:59 GMT
COPY multi:b8b1838b39ef7d9df547fe9a734d87e1a3923c8022961091b24ee37feff4d404 in / 
# Tue, 10 Mar 2020 22:59:00 GMT
USER jetty
# Tue, 10 Mar 2020 22:59:00 GMT
EXPOSE 8080
# Tue, 10 Mar 2020 22:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:59:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00902ec9e71adeff6a5b90b0d6f0d3527baec74ca75174ed4bc05a0cf0e2b`  
		Last Modified: Tue, 10 Mar 2020 02:46:34 GMT  
		Size: 196.4 MB (196373417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4198a998add0ee34b04673daf72b241f58046ccfb6a9e01a3389b8098b33c9`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 9.7 MB (9679711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e41e5702d2994e9ff1f345cdffdfd27dcd9ce1cb82ca33efd4b3fbbfa60198`  
		Last Modified: Tue, 10 Mar 2020 22:59:19 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
