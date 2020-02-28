## `sonarqube:8-developer`

```console
$ docker pull sonarqube@sha256:b032963630a19800f1de9ffcfc6d425ce249343dc62eeb126113c1107ee4a68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:2d13d3d8cd0d0021c78857fb7bdc100008dacd52e6c9948d1714f2102767e7e1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363852837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c93ac932d1919c4129a0ffdf593f83bda42d2adcea16de69d67976623c299a`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:20:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:20:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:20:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:20:24 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:10 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:11 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 28 Feb 2020 00:33:32 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Feb 2020 00:33:32 GMT
EXPOSE 9000
# Fri, 28 Feb 2020 00:33:33 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 28 Feb 2020 00:33:33 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 28 Feb 2020 00:33:55 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
# Fri, 28 Feb 2020 00:33:56 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 28 Feb 2020 00:33:56 GMT
SHELL [/bin/bash -c]
# Fri, 28 Feb 2020 00:33:57 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 28 Feb 2020 00:35:25 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "$SONARQUBE_ZIP_URL"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 28 Feb 2020 00:35:25 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 28 Feb 2020 00:35:25 GMT
USER sonarqube
# Fri, 28 Feb 2020 00:35:25 GMT
WORKDIR /opt/sonarqube
# Fri, 28 Feb 2020 00:35:26 GMT
ENTRYPOINT ["./bin/run.sh"]
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
	-	`sha256:8afa8e973e226cdc57cde0ef199d85ee1aa93b5f6a04abf68dc4952cdab931d5`  
		Last Modified: Wed, 26 Feb 2020 20:26:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c28bc4eb5532356cd06f142ed9cd6cee0811be74e992fdd2190fee8cbcf710`  
		Last Modified: Wed, 26 Feb 2020 20:27:41 GMT  
		Size: 42.2 MB (42172601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d725e653d5dd64a3f6c374306d23158495eb677f283c94d2b43ca590f63516c2`  
		Last Modified: Fri, 28 Feb 2020 00:38:03 GMT  
		Size: 8.7 MB (8709003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2166bcb54cd68c3a99d703a15083d498085d5da754397e9aeb8c943255957b`  
		Last Modified: Fri, 28 Feb 2020 00:38:01 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed4d9baa03270e49de8baf1cd230da444b4685d9a79ccbe1339ee9c1965f184`  
		Last Modified: Fri, 28 Feb 2020 00:38:21 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf84a0772a23a37c6cb04657e8f46ec953777619b96a71007ba2491fc5f26802`  
		Last Modified: Fri, 28 Feb 2020 00:38:39 GMT  
		Size: 282.6 MB (282612665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95fd0c69c48e9f64d1d38a409e404346b7deedc40080562d625e9128760b6eb`  
		Last Modified: Fri, 28 Feb 2020 00:38:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
