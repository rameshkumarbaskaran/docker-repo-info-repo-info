<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sonarqube`

-	[`sonarqube:7.9.5-community`](#sonarqube795-community)
-	[`sonarqube:7.9-community`](#sonarqube79-community)
-	[`sonarqube:8.6.0-community`](#sonarqube860-community)
-	[`sonarqube:8.6.0-developer`](#sonarqube860-developer)
-	[`sonarqube:8.6.0-enterprise`](#sonarqube860-enterprise)
-	[`sonarqube:8.6-community`](#sonarqube86-community)
-	[`sonarqube:8.6-developer`](#sonarqube86-developer)
-	[`sonarqube:8.6-enterprise`](#sonarqube86-enterprise)
-	[`sonarqube:8-community`](#sonarqube8-community)
-	[`sonarqube:8-developer`](#sonarqube8-developer)
-	[`sonarqube:8-enterprise`](#sonarqube8-enterprise)
-	[`sonarqube:community`](#sonarqubecommunity)
-	[`sonarqube:developer`](#sonarqubedeveloper)
-	[`sonarqube:enterprise`](#sonarqubeenterprise)
-	[`sonarqube:latest`](#sonarqubelatest)
-	[`sonarqube:lts`](#sonarqubelts)

## `sonarqube:7.9.5-community`

```console
$ docker pull sonarqube@sha256:343ae55997ceeb965a3b027a38093b05c067515af667e7b8b4b077f993dd2d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:7.9.5-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:7490232166fbbf2acfda101cdd049c14d65b25445897f4d0a13e305d89c89442
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285798048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db221d2e6af0dd973a3d98b7a41be5a14c7abf0c1237c3ab89b7535f6246e812`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 15:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 15:36:22 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 15:38:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Fri, 11 Dec 2020 15:38:39 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 15:38:40 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 11 Dec 2020 15:38:40 GMT
ENV JAVA_VERSION=11.0.9.1
# Fri, 11 Dec 2020 15:39:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Sat, 12 Dec 2020 03:50:38 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 03:50:38 GMT
ENV SONAR_VERSION=7.9.5 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Sat, 12 Dec 2020 03:50:38 GMT
EXPOSE 9000
# Sat, 12 Dec 2020 03:50:39 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Sat, 12 Dec 2020 03:50:40 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Sat, 12 Dec 2020 03:50:56 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Sat, 12 Dec 2020 03:50:57 GMT
VOLUME [/opt/sonarqube/data]
# Sat, 12 Dec 2020 03:50:57 GMT
WORKDIR /opt/sonarqube
# Sat, 12 Dec 2020 03:50:57 GMT
COPY file:d7c6edf99ad4508dcb273783aad5da8017e549d505d617619117cc576bbc8850 in /opt/sonarqube/bin/ 
# Sat, 12 Dec 2020 03:50:57 GMT
USER sonarqube
# Sat, 12 Dec 2020 03:50:57 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177617b11d133131d55a469644e5bcd4e402246268313630a2ae2b32b7a3bcf8`  
		Last Modified: Fri, 11 Dec 2020 15:43:03 GMT  
		Size: 3.2 MB (3248608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273812b9e39505a6a9d7c79b6b35b1981fd4a720e5e6a02e646b46c3274060`  
		Last Modified: Fri, 11 Dec 2020 15:45:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac553cdb1df66be1f35bedcd7381dbc8ec67f6ec386fcf65266474c49a426cb3`  
		Last Modified: Fri, 11 Dec 2020 15:46:01 GMT  
		Size: 42.4 MB (42404790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2444d95f81086a8ca73bb9368b2018a6bc061415593d535491eedec03fbf61`  
		Last Modified: Sat, 12 Dec 2020 03:51:29 GMT  
		Size: 6.0 MB (5985010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9adec26a3d77fff84ba18210e7620e19b43222ca0cdf3474a5ccd4a6ae9edc`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd1f70083bbf720409978dfd735bb57858cc9d39806cff5f6ed4bc0c8dfa34`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f56a7acabd5337aad390dc11cb4262ddc3defcaa87951b99be30e89a7a6ddb`  
		Last Modified: Sat, 12 Dec 2020 03:51:42 GMT  
		Size: 207.1 MB (207055806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d885397a803c8e3481e5c787733fb20ab7958152ab822aceb59098f58953540`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 817.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:7.9-community`

```console
$ docker pull sonarqube@sha256:343ae55997ceeb965a3b027a38093b05c067515af667e7b8b4b077f993dd2d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:7.9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:7490232166fbbf2acfda101cdd049c14d65b25445897f4d0a13e305d89c89442
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285798048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db221d2e6af0dd973a3d98b7a41be5a14c7abf0c1237c3ab89b7535f6246e812`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 15:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 15:36:22 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 15:38:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Fri, 11 Dec 2020 15:38:39 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 15:38:40 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 11 Dec 2020 15:38:40 GMT
ENV JAVA_VERSION=11.0.9.1
# Fri, 11 Dec 2020 15:39:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Sat, 12 Dec 2020 03:50:38 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 03:50:38 GMT
ENV SONAR_VERSION=7.9.5 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Sat, 12 Dec 2020 03:50:38 GMT
EXPOSE 9000
# Sat, 12 Dec 2020 03:50:39 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Sat, 12 Dec 2020 03:50:40 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Sat, 12 Dec 2020 03:50:56 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Sat, 12 Dec 2020 03:50:57 GMT
VOLUME [/opt/sonarqube/data]
# Sat, 12 Dec 2020 03:50:57 GMT
WORKDIR /opt/sonarqube
# Sat, 12 Dec 2020 03:50:57 GMT
COPY file:d7c6edf99ad4508dcb273783aad5da8017e549d505d617619117cc576bbc8850 in /opt/sonarqube/bin/ 
# Sat, 12 Dec 2020 03:50:57 GMT
USER sonarqube
# Sat, 12 Dec 2020 03:50:57 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177617b11d133131d55a469644e5bcd4e402246268313630a2ae2b32b7a3bcf8`  
		Last Modified: Fri, 11 Dec 2020 15:43:03 GMT  
		Size: 3.2 MB (3248608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273812b9e39505a6a9d7c79b6b35b1981fd4a720e5e6a02e646b46c3274060`  
		Last Modified: Fri, 11 Dec 2020 15:45:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac553cdb1df66be1f35bedcd7381dbc8ec67f6ec386fcf65266474c49a426cb3`  
		Last Modified: Fri, 11 Dec 2020 15:46:01 GMT  
		Size: 42.4 MB (42404790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2444d95f81086a8ca73bb9368b2018a6bc061415593d535491eedec03fbf61`  
		Last Modified: Sat, 12 Dec 2020 03:51:29 GMT  
		Size: 6.0 MB (5985010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9adec26a3d77fff84ba18210e7620e19b43222ca0cdf3474a5ccd4a6ae9edc`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd1f70083bbf720409978dfd735bb57858cc9d39806cff5f6ed4bc0c8dfa34`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f56a7acabd5337aad390dc11cb4262ddc3defcaa87951b99be30e89a7a6ddb`  
		Last Modified: Sat, 12 Dec 2020 03:51:42 GMT  
		Size: 207.1 MB (207055806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d885397a803c8e3481e5c787733fb20ab7958152ab822aceb59098f58953540`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 817.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.6.0-community`

```console
$ docker pull sonarqube@sha256:6716837a86ab991205a7579b1630fb087c64624835c7f78aa233b6e1bf305082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8.6.0-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:de70dac6e706c4b40b38319c26fb25f7f9c0bf44d67d2ad603a7c4a75b91998c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.5 MB (464466773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0247bd016bd4b07876aacf3f2e751744ffdde988d4b50f5d90dd5b081244922`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:40:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:40:55 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:40:56 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:40:56 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:40:56 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:40:56 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:40:56 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9c21026d713f7c68ee800a3d10726b112850ab5710e0585b06e11a0d0401f6`  
		Last Modified: Thu, 17 Dec 2020 13:43:21 GMT  
		Size: 261.0 MB (261038750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddac7b0d6339a1748ffa0441186b9b3f5118174ba83d07b5f10625d826e96c7b`  
		Last Modified: Thu, 17 Dec 2020 13:42:51 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.6.0-developer`

```console
$ docker pull sonarqube@sha256:cebe84be79db405de3b0264210d556e307f088684520de5169bb2d5d62032750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8.6.0-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:4d217513dc82c7cb857d067de225b68779a71397b2e761cae8948803d5f5bf8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530428487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18773236431c8eb3f5d89046732e3a9d6421965881b326fa521e5a963737c771`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:02 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:41:34 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:41:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:41:36 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:41:36 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:41:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:41:37 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036881856fa6a75d6556412a272faf24044a037e93e603172f2f9256ca628fb4`  
		Last Modified: Thu, 17 Dec 2020 13:44:05 GMT  
		Size: 327.0 MB (327000464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f239a71cd632fc9f2446268ec51b58e086a3670bcef459af29a5f20119086311`  
		Last Modified: Thu, 17 Dec 2020 13:43:42 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.6.0-enterprise`

```console
$ docker pull sonarqube@sha256:5f15f2180976f892470431e28b9b83a76272d65624efbc2bdd7f15e1c524b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8.6.0-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:ad3e8e1e16e86bc9ebd7f0168036c1205413ae4a30fdc402ea31982214987c9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.1 MB (551084031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d436e58609cd79e1ad4fe26a96a278c46af9125fadb68e4e31acd080d345534`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:42:16 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:42:17 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:42:17 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:42:18 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:42:18 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:42:18 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7364391ec45aa22f43aad3eb3fe643be4982071b9600d285ba550c788143b608`  
		Last Modified: Thu, 17 Dec 2020 13:44:53 GMT  
		Size: 347.7 MB (347656011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d22c4ffccf1589bfdf1624f3e5f9fdf4c0abb216b034e01b03bf2ebd5f129`  
		Last Modified: Thu, 17 Dec 2020 13:44:17 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.6-community`

```console
$ docker pull sonarqube@sha256:6716837a86ab991205a7579b1630fb087c64624835c7f78aa233b6e1bf305082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8.6-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:de70dac6e706c4b40b38319c26fb25f7f9c0bf44d67d2ad603a7c4a75b91998c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.5 MB (464466773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0247bd016bd4b07876aacf3f2e751744ffdde988d4b50f5d90dd5b081244922`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:40:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:40:55 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:40:56 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:40:56 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:40:56 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:40:56 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:40:56 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9c21026d713f7c68ee800a3d10726b112850ab5710e0585b06e11a0d0401f6`  
		Last Modified: Thu, 17 Dec 2020 13:43:21 GMT  
		Size: 261.0 MB (261038750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddac7b0d6339a1748ffa0441186b9b3f5118174ba83d07b5f10625d826e96c7b`  
		Last Modified: Thu, 17 Dec 2020 13:42:51 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.6-developer`

```console
$ docker pull sonarqube@sha256:cebe84be79db405de3b0264210d556e307f088684520de5169bb2d5d62032750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8.6-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:4d217513dc82c7cb857d067de225b68779a71397b2e761cae8948803d5f5bf8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530428487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18773236431c8eb3f5d89046732e3a9d6421965881b326fa521e5a963737c771`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:02 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:41:34 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:41:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:41:36 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:41:36 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:41:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:41:37 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036881856fa6a75d6556412a272faf24044a037e93e603172f2f9256ca628fb4`  
		Last Modified: Thu, 17 Dec 2020 13:44:05 GMT  
		Size: 327.0 MB (327000464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f239a71cd632fc9f2446268ec51b58e086a3670bcef459af29a5f20119086311`  
		Last Modified: Thu, 17 Dec 2020 13:43:42 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8.6-enterprise`

```console
$ docker pull sonarqube@sha256:5f15f2180976f892470431e28b9b83a76272d65624efbc2bdd7f15e1c524b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8.6-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:ad3e8e1e16e86bc9ebd7f0168036c1205413ae4a30fdc402ea31982214987c9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.1 MB (551084031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d436e58609cd79e1ad4fe26a96a278c46af9125fadb68e4e31acd080d345534`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:42:16 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:42:17 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:42:17 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:42:18 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:42:18 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:42:18 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7364391ec45aa22f43aad3eb3fe643be4982071b9600d285ba550c788143b608`  
		Last Modified: Thu, 17 Dec 2020 13:44:53 GMT  
		Size: 347.7 MB (347656011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d22c4ffccf1589bfdf1624f3e5f9fdf4c0abb216b034e01b03bf2ebd5f129`  
		Last Modified: Thu, 17 Dec 2020 13:44:17 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-community`

```console
$ docker pull sonarqube@sha256:6716837a86ab991205a7579b1630fb087c64624835c7f78aa233b6e1bf305082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:de70dac6e706c4b40b38319c26fb25f7f9c0bf44d67d2ad603a7c4a75b91998c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.5 MB (464466773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0247bd016bd4b07876aacf3f2e751744ffdde988d4b50f5d90dd5b081244922`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:40:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:40:55 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:40:56 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:40:56 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:40:56 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:40:56 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:40:56 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9c21026d713f7c68ee800a3d10726b112850ab5710e0585b06e11a0d0401f6`  
		Last Modified: Thu, 17 Dec 2020 13:43:21 GMT  
		Size: 261.0 MB (261038750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddac7b0d6339a1748ffa0441186b9b3f5118174ba83d07b5f10625d826e96c7b`  
		Last Modified: Thu, 17 Dec 2020 13:42:51 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-developer`

```console
$ docker pull sonarqube@sha256:cebe84be79db405de3b0264210d556e307f088684520de5169bb2d5d62032750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:4d217513dc82c7cb857d067de225b68779a71397b2e761cae8948803d5f5bf8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530428487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18773236431c8eb3f5d89046732e3a9d6421965881b326fa521e5a963737c771`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:02 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:41:34 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:41:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:41:36 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:41:36 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:41:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:41:37 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036881856fa6a75d6556412a272faf24044a037e93e603172f2f9256ca628fb4`  
		Last Modified: Thu, 17 Dec 2020 13:44:05 GMT  
		Size: 327.0 MB (327000464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f239a71cd632fc9f2446268ec51b58e086a3670bcef459af29a5f20119086311`  
		Last Modified: Thu, 17 Dec 2020 13:43:42 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:8-enterprise`

```console
$ docker pull sonarqube@sha256:5f15f2180976f892470431e28b9b83a76272d65624efbc2bdd7f15e1c524b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:ad3e8e1e16e86bc9ebd7f0168036c1205413ae4a30fdc402ea31982214987c9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.1 MB (551084031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d436e58609cd79e1ad4fe26a96a278c46af9125fadb68e4e31acd080d345534`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:42:16 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:42:17 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:42:17 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:42:18 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:42:18 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:42:18 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7364391ec45aa22f43aad3eb3fe643be4982071b9600d285ba550c788143b608`  
		Last Modified: Thu, 17 Dec 2020 13:44:53 GMT  
		Size: 347.7 MB (347656011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d22c4ffccf1589bfdf1624f3e5f9fdf4c0abb216b034e01b03bf2ebd5f129`  
		Last Modified: Thu, 17 Dec 2020 13:44:17 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:6716837a86ab991205a7579b1630fb087c64624835c7f78aa233b6e1bf305082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:de70dac6e706c4b40b38319c26fb25f7f9c0bf44d67d2ad603a7c4a75b91998c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.5 MB (464466773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0247bd016bd4b07876aacf3f2e751744ffdde988d4b50f5d90dd5b081244922`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:40:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:40:55 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:40:56 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:40:56 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:40:56 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:40:56 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:40:56 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9c21026d713f7c68ee800a3d10726b112850ab5710e0585b06e11a0d0401f6`  
		Last Modified: Thu, 17 Dec 2020 13:43:21 GMT  
		Size: 261.0 MB (261038750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddac7b0d6339a1748ffa0441186b9b3f5118174ba83d07b5f10625d826e96c7b`  
		Last Modified: Thu, 17 Dec 2020 13:42:51 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:developer`

```console
$ docker pull sonarqube@sha256:cebe84be79db405de3b0264210d556e307f088684520de5169bb2d5d62032750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:4d217513dc82c7cb857d067de225b68779a71397b2e761cae8948803d5f5bf8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530428487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18773236431c8eb3f5d89046732e3a9d6421965881b326fa521e5a963737c771`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:02 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:41:34 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:41:35 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:41:36 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:41:36 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:41:36 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:41:37 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036881856fa6a75d6556412a272faf24044a037e93e603172f2f9256ca628fb4`  
		Last Modified: Thu, 17 Dec 2020 13:44:05 GMT  
		Size: 327.0 MB (327000464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f239a71cd632fc9f2446268ec51b58e086a3670bcef459af29a5f20119086311`  
		Last Modified: Thu, 17 Dec 2020 13:43:42 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:enterprise`

```console
$ docker pull sonarqube@sha256:5f15f2180976f892470431e28b9b83a76272d65624efbc2bdd7f15e1c524b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:ad3e8e1e16e86bc9ebd7f0168036c1205413ae4a30fdc402ea31982214987c9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.1 MB (551084031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d436e58609cd79e1ad4fe26a96a278c46af9125fadb68e4e31acd080d345534`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:41:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:41:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:42:16 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:42:17 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:42:17 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:42:18 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:42:18 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:42:18 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7364391ec45aa22f43aad3eb3fe643be4982071b9600d285ba550c788143b608`  
		Last Modified: Thu, 17 Dec 2020 13:44:53 GMT  
		Size: 347.7 MB (347656011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d22c4ffccf1589bfdf1624f3e5f9fdf4c0abb216b034e01b03bf2ebd5f129`  
		Last Modified: Thu, 17 Dec 2020 13:44:17 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:6716837a86ab991205a7579b1630fb087c64624835c7f78aa233b6e1bf305082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:latest` - linux; amd64

```console
$ docker pull sonarqube@sha256:de70dac6e706c4b40b38319c26fb25f7f9c0bf44d67d2ad603a7c4a75b91998c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.5 MB (464466773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0247bd016bd4b07876aacf3f2e751744ffdde988d4b50f5d90dd5b081244922`
-	Entrypoint: `["bin\/run.sh"]`
-	Default Command: `["bin\/sonar.sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:40:15 GMT
ENV JAVA_VERSION=jdk-11.0.8+10 LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Dec 2020 13:40:23 GMT
RUN set -eux;     apk add --no-cache tzdata --virtual .build-deps curl binutils zstd;     GLIBC_VER="2.32-r0";     ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download";     GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-10.1.0-2-x86_64.pkg.tar.zst";     GCC_LIBS_SHA256="f80320a03ff73e82271064e4f684cd58d7dbdb07aa06a2c4eea8e0f3c507c45c";     ZLIB_URL="https://archive.archlinux.org/packages/z/zlib/zlib-1%3A1.2.11-3-x86_64.pkg.tar.xz";     ZLIB_SHA256=17aede0b9f8baa789c5aa3f358fbf8c68a5f1228c5e6cba1a5dd34102ef4d4e5;     curl -LfsS https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub;     SGERRAND_RSA_SHA256="823b54589c93b02497f1ba4dc622eaef9c813e6b0f0ebbb2f771e32adf9f4ef2";     echo "${SGERRAND_RSA_SHA256} */etc/apk/keys/sgerrand.rsa.pub" | sha256sum -c - ;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/glibc-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-bin-${GLIBC_VER}.apk > /tmp/glibc-bin-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-bin-${GLIBC_VER}.apk;     curl -LfsS ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-i18n-${GLIBC_VER}.apk > /tmp/glibc-i18n-${GLIBC_VER}.apk;     apk add --no-cache /tmp/glibc-i18n-${GLIBC_VER}.apk;     /usr/glibc-compat/bin/localedef --force --inputfile POSIX --charmap UTF-8 "$LANG" || true;     echo "export LANG=$LANG" > /etc/profile.d/locale.sh;     curl -LfsS ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.zst;     echo "${GCC_LIBS_SHA256} */tmp/gcc-libs.tar.zst" | sha256sum -c -;     mkdir /tmp/gcc;     zstd -d /tmp/gcc-libs.tar.zst --output-dir-flat /tmp;     tar -xf /tmp/gcc-libs.tar -C /tmp/gcc;     mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib;     strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*;     curl -LfsS ${ZLIB_URL} -o /tmp/libz.tar.xz;     echo "${ZLIB_SHA256} */tmp/libz.tar.xz" | sha256sum -c -;     mkdir /tmp/libz;     tar -xf /tmp/libz.tar.xz -C /tmp/libz;     mv /tmp/libz/usr/lib/libz.so* /usr/glibc-compat/lib;     apk del --purge .build-deps glibc-i18n;     rm -rf /tmp/*.apk /tmp/gcc /tmp/gcc-libs.tar* /tmp/libz /tmp/libz.tar.xz /var/cache/apk/*;
# Thu, 17 Dec 2020 13:40:34 GMT
RUN set -eux;     apk add --no-cache --virtual .fetch-deps curl;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     export PATH="/opt/java/openjdk/bin:$PATH";     apk del --purge .fetch-deps;     rm -rf /var/cache/apk/*;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_VERSION=8.6.0.39681
# Thu, 17 Dec 2020 13:40:34 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
# Thu, 17 Dec 2020 13:40:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=8.6.0.39681 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Thu, 17 Dec 2020 13:40:55 GMT
# ARGS: SONARQUBE_VERSION=8.6.0.39681 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-8.6.0.39681.zip
RUN set -ex     && addgroup -S -g 1000 sonarqube     && adduser -S -D -u 1000 -G sonarqube sonarqube     && apk add --no-cache --virtual build-dependencies gnupg unzip curl     && apk add --no-cache bash su-exec ttf-dejavu     && sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security"     && for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "${server}" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done     && mkdir --parents /opt     && cd /opt     && curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}"     && curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && rm -rf ${SONARQUBE_HOME}/bin/*     && chown -R sonarqube:sonarqube ${SONARQUBE_HOME}     && chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}"     && apk del --purge build-dependencies
# Thu, 17 Dec 2020 13:40:56 GMT
COPY --chown=sonarqube:sonarqubemulti:aed345498324cc768d63aba16bd3b3de027a0213cb3a62a9a3b27799dbf88552 in /opt/sonarqube/bin/ 
# Thu, 17 Dec 2020 13:40:56 GMT
WORKDIR /opt/sonarqube
# Thu, 17 Dec 2020 13:40:56 GMT
EXPOSE 9000
# Thu, 17 Dec 2020 13:40:56 GMT
ENTRYPOINT ["bin/run.sh"]
# Thu, 17 Dec 2020 13:40:56 GMT
CMD ["bin/sonar.sh"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb833291b55c696ea355b1a18b23e322dcf6af10e084525ca3a7ab6819224b97`  
		Last Modified: Thu, 17 Dec 2020 13:42:54 GMT  
		Size: 6.3 MB (6335497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91bfbe66cb72cdb3957b0c8162b7c42d3fe8de647811de417899b940a94731`  
		Last Modified: Thu, 17 Dec 2020 13:43:20 GMT  
		Size: 194.3 MB (194276565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9c21026d713f7c68ee800a3d10726b112850ab5710e0585b06e11a0d0401f6`  
		Last Modified: Thu, 17 Dec 2020 13:43:21 GMT  
		Size: 261.0 MB (261038750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddac7b0d6339a1748ffa0441186b9b3f5118174ba83d07b5f10625d826e96c7b`  
		Last Modified: Thu, 17 Dec 2020 13:42:51 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:343ae55997ceeb965a3b027a38093b05c067515af667e7b8b4b077f993dd2d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:7490232166fbbf2acfda101cdd049c14d65b25445897f4d0a13e305d89c89442
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285798048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db221d2e6af0dd973a3d98b7a41be5a14c7abf0c1237c3ab89b7535f6246e812`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 15:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 15:36:22 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 15:38:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Fri, 11 Dec 2020 15:38:39 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 15:38:40 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 11 Dec 2020 15:38:40 GMT
ENV JAVA_VERSION=11.0.9.1
# Fri, 11 Dec 2020 15:39:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jre_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Sat, 12 Dec 2020 03:50:38 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 03:50:38 GMT
ENV SONAR_VERSION=7.9.5 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Sat, 12 Dec 2020 03:50:38 GMT
EXPOSE 9000
# Sat, 12 Dec 2020 03:50:39 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Sat, 12 Dec 2020 03:50:40 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Sat, 12 Dec 2020 03:50:56 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Sat, 12 Dec 2020 03:50:57 GMT
VOLUME [/opt/sonarqube/data]
# Sat, 12 Dec 2020 03:50:57 GMT
WORKDIR /opt/sonarqube
# Sat, 12 Dec 2020 03:50:57 GMT
COPY file:d7c6edf99ad4508dcb273783aad5da8017e549d505d617619117cc576bbc8850 in /opt/sonarqube/bin/ 
# Sat, 12 Dec 2020 03:50:57 GMT
USER sonarqube
# Sat, 12 Dec 2020 03:50:57 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177617b11d133131d55a469644e5bcd4e402246268313630a2ae2b32b7a3bcf8`  
		Last Modified: Fri, 11 Dec 2020 15:43:03 GMT  
		Size: 3.2 MB (3248608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10273812b9e39505a6a9d7c79b6b35b1981fd4a720e5e6a02e646b46c3274060`  
		Last Modified: Fri, 11 Dec 2020 15:45:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac553cdb1df66be1f35bedcd7381dbc8ec67f6ec386fcf65266474c49a426cb3`  
		Last Modified: Fri, 11 Dec 2020 15:46:01 GMT  
		Size: 42.4 MB (42404790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2444d95f81086a8ca73bb9368b2018a6bc061415593d535491eedec03fbf61`  
		Last Modified: Sat, 12 Dec 2020 03:51:29 GMT  
		Size: 6.0 MB (5985010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9adec26a3d77fff84ba18210e7620e19b43222ca0cdf3474a5ccd4a6ae9edc`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fd1f70083bbf720409978dfd735bb57858cc9d39806cff5f6ed4bc0c8dfa34`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f56a7acabd5337aad390dc11cb4262ddc3defcaa87951b99be30e89a7a6ddb`  
		Last Modified: Sat, 12 Dec 2020 03:51:42 GMT  
		Size: 207.1 MB (207055806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d885397a803c8e3481e5c787733fb20ab7958152ab822aceb59098f58953540`  
		Last Modified: Sat, 12 Dec 2020 03:51:27 GMT  
		Size: 817.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
