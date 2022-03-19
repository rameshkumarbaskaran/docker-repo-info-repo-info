<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jruby`

-	[`jruby:9`](#jruby9)
-	[`jruby:9-jdk`](#jruby9-jdk)
-	[`jruby:9-jdk8`](#jruby9-jdk8)
-	[`jruby:9.2`](#jruby92)
-	[`jruby:9.2-jdk`](#jruby92-jdk)
-	[`jruby:9.2-jdk11`](#jruby92-jdk11)
-	[`jruby:9.2-jdk17`](#jruby92-jdk17)
-	[`jruby:9.2-jdk8`](#jruby92-jdk8)
-	[`jruby:9.2-jre`](#jruby92-jre)
-	[`jruby:9.2-jre11`](#jruby92-jre11)
-	[`jruby:9.2-jre8`](#jruby92-jre8)
-	[`jruby:9.2-onbuild`](#jruby92-onbuild)
-	[`jruby:9.2.20`](#jruby9220)
-	[`jruby:9.2.20-jdk`](#jruby9220-jdk)
-	[`jruby:9.2.20-jdk11`](#jruby9220-jdk11)
-	[`jruby:9.2.20-jdk17`](#jruby9220-jdk17)
-	[`jruby:9.2.20-jdk8`](#jruby9220-jdk8)
-	[`jruby:9.2.20-jre`](#jruby9220-jre)
-	[`jruby:9.2.20-jre11`](#jruby9220-jre11)
-	[`jruby:9.2.20-jre8`](#jruby9220-jre8)
-	[`jruby:9.2.20-onbuild`](#jruby9220-onbuild)
-	[`jruby:9.2.20.0-jdk`](#jruby92200-jdk)
-	[`jruby:9.2.20.0-jre`](#jruby92200-jre)
-	[`jruby:9.2.20.0-jre8`](#jruby92200-jre8)
-	[`jruby:9.2.20.1`](#jruby92201)
-	[`jruby:9.2.20.1-jdk11`](#jruby92201-jdk11)
-	[`jruby:9.2.20.1-jdk17`](#jruby92201-jdk17)
-	[`jruby:9.2.20.1-jdk8`](#jruby92201-jdk8)
-	[`jruby:9.2.20.1-jre11`](#jruby92201-jre11)
-	[`jruby:9.2.20.1-onbuild`](#jruby92201-onbuild)
-	[`jruby:9.3`](#jruby93)
-	[`jruby:9.3-jdk`](#jruby93-jdk)
-	[`jruby:9.3-jdk11`](#jruby93-jdk11)
-	[`jruby:9.3-jdk17`](#jruby93-jdk17)
-	[`jruby:9.3-jdk8`](#jruby93-jdk8)
-	[`jruby:9.3-jre`](#jruby93-jre)
-	[`jruby:9.3-jre11`](#jruby93-jre11)
-	[`jruby:9.3-jre8`](#jruby93-jre8)
-	[`jruby:9.3.3`](#jruby933)
-	[`jruby:9.3.3-jdk`](#jruby933-jdk)
-	[`jruby:9.3.3-jdk11`](#jruby933-jdk11)
-	[`jruby:9.3.3-jdk17`](#jruby933-jdk17)
-	[`jruby:9.3.3-jdk8`](#jruby933-jdk8)
-	[`jruby:9.3.3-jre`](#jruby933-jre)
-	[`jruby:9.3.3-jre11`](#jruby933-jre11)
-	[`jruby:9.3.3-jre8`](#jruby933-jre8)
-	[`jruby:9.3.3.0`](#jruby9330)
-	[`jruby:9.3.3.0-jdk`](#jruby9330-jdk)
-	[`jruby:9.3.3.0-jdk11`](#jruby9330-jdk11)
-	[`jruby:9.3.3.0-jdk17`](#jruby9330-jdk17)
-	[`jruby:9.3.3.0-jdk8`](#jruby9330-jdk8)
-	[`jruby:9.3.3.0-jre`](#jruby9330-jre)
-	[`jruby:9.3.3.0-jre11`](#jruby9330-jre11)
-	[`jruby:9.3.3.0-jre8`](#jruby9330-jre8)
-	[`jruby:latest`](#jrubylatest)

## `jruby:9`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk`

```console
$ docker pull jruby@sha256:7185266f95d632f6f6a004dd73658f7f603e6b40ad88eafcf80c25c0560716b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:a766bcb84f1971423a46c61ff377c37b78011d522bc1f3665139d069dd0771ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3d7a08960453d84ca781c2f890808b7adc52814c0688ee15062356b61b765`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk11`

```console
$ docker pull jruby@sha256:2272a5b39ded2076416caa4dd7b72d9afa47a4917871aa390aa0a27467431981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:76b200fd742c729bd948e06fe872afda7cbb4d36d5767f59afa08c26a17854a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365416797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e35c9fcb49c1d75c3bf1801667704bfeb5c2fd39c0d1ef099ebda08978e4132`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:03 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:26:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:26:31 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:42:23 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:42:23 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:26 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:27 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:42:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:42:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f30a831c1a9aca6f978e51ea8ed88eaff501aa9a21062c95de6d89e1016e2`  
		Last Modified: Sat, 19 Mar 2022 10:45:08 GMT  
		Size: 5.3 MB (5286496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea684d520abfaeda4a91b1f05dcfdd7d78fe488a5b8b2df6ac9eb6e6160e8718`  
		Last Modified: Sat, 19 Mar 2022 10:45:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dac09b64de5415f528e3a4a2540c594392b379e925448a7dcd2e5a8c3c03c46`  
		Last Modified: Sat, 19 Mar 2022 10:45:23 GMT  
		Size: 203.3 MB (203260532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32488f910728c22a3b1cb670a048ddf9dc044368709455c69ba9933d61114f37`  
		Last Modified: Sat, 19 Mar 2022 14:46:19 GMT  
		Size: 7.9 MB (7855689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7e7baeb62ee0ffa475ac3cf2c2cff1603ffc00c0c2e20c080941ad67790d03`  
		Last Modified: Sat, 19 Mar 2022 14:48:10 GMT  
		Size: 27.9 MB (27850009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339c5631a69f7787ce2cca8107aa47a0cb3419526e0ab01c3d530cfdb9e672c3`  
		Last Modified: Sat, 19 Mar 2022 14:48:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12ed74047d5052bdc5d5e89a20e701e1a5c7e5f1a959ed82f2502548ef2c73`  
		Last Modified: Sat, 19 Mar 2022 14:48:08 GMT  
		Size: 1.1 MB (1051171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b466d6c6d629c81f661c4b28ca98b0e23c314f0606b3ed8ebab0c88d2935379c`  
		Last Modified: Sat, 19 Mar 2022 14:48:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk17`

```console
$ docker pull jruby@sha256:34aaf313a166e6d8c906dbdad953b321d82128fdcee58b9a28616062f70218ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:78043bb5a3c2357f03f8d579940dd1a0dfe39abd422d5414044d4d022bafcf4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358424768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43971257875fad8be4c6472cb153e65d96ae7ddba19f9ca5e6ab65630498d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:23:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 19 Mar 2022 10:23:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:23:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:23:09 GMT
ENV JAVA_VERSION=17.0.2
# Sat, 19 Mar 2022 10:23:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:23:19 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:42:52 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:42:52 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:56 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:43:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:43:14 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:43:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:43:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25299f1f342403e9c0e28d57d5a4da4470e18083460fa540e198be442286c9c`  
		Last Modified: Sat, 19 Mar 2022 10:36:56 GMT  
		Size: 13.9 MB (13921274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57415387047b38bce51b83f76ee83dd55e93536d6feeac693ba47470bada257`  
		Last Modified: Sat, 19 Mar 2022 10:42:04 GMT  
		Size: 187.6 MB (187632031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbdfc195411eabe8bc79554f459e7fda7c6ddf81cf559de48f3d0a2daa25845`  
		Last Modified: Sat, 19 Mar 2022 14:46:35 GMT  
		Size: 7.9 MB (7857496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca65493d6fa917993be6aa6ad9ab747beda4fc516a90887a6044cb193c5b9c`  
		Last Modified: Sat, 19 Mar 2022 14:48:27 GMT  
		Size: 27.9 MB (27850071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7b11784031401e99605fee60792e588b0fb5a23ef9c33fd2f46597534e0c27`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1168f294dfc7785e88d849178a23f2dcdda99f40450be3dcb5333a1b3e4a7`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 1.1 MB (1051208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e134f6ee6e8de0943e52ed09c44dcaea04f55dcb3094448de773f933912928c`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk8`

```console
$ docker pull jruby@sha256:7185266f95d632f6f6a004dd73658f7f603e6b40ad88eafcf80c25c0560716b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:a766bcb84f1971423a46c61ff377c37b78011d522bc1f3665139d069dd0771ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3d7a08960453d84ca781c2f890808b7adc52814c0688ee15062356b61b765`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre11`

```console
$ docker pull jruby@sha256:4c0963562b2b93b8879c96dfb16cbe16fd0e49f4a32b5dcf2e2cc924101a3b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:fdd2f792bbeea1855079a5af8dd39ea63725ea80368668edadd1e554232e3a50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157411164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70703a946819dc8c3fdb20cd599ff6fdc33087490c9cec82796f5d22e8040b0c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 14:39:37 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:59 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:59 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:02 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:42:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:42:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:42:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca486c90ae5fe6f88923feab4a27336ade1136701513bdb8155331fbe1c532`  
		Last Modified: Sat, 19 Mar 2022 14:46:03 GMT  
		Size: 7.8 MB (7829188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca684b5e244d75fa1d3079f61a18d318c4fe5c67e6513744d979b8e62b3f78d`  
		Last Modified: Sat, 19 Mar 2022 14:47:53 GMT  
		Size: 27.8 MB (27849800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f506d2332b3956f40d2b8ac6effa0b775b73847a125aa1fb9e88f9ca58e0bab9`  
		Last Modified: Sat, 19 Mar 2022 14:47:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b86cce8b12ad3ca94a57a5a8e79516574056f42f577c221856cbe3478f733`  
		Last Modified: Sat, 19 Mar 2022 14:47:51 GMT  
		Size: 1.1 MB (1051162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082d7c54d3b5f913c8d07b57778e6e7e14fc078fd48e7109b44d87caca4714a9`  
		Last Modified: Sat, 19 Mar 2022 14:47:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre8`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-onbuild`

```console
$ docker pull jruby@sha256:02ec04cb1a6f6aabb5f231de8664890f23a739481bc8baf68a36a51641875eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:3567208690b5a44249644969338cda86e61f35420b6f8277b3228f56c0e0e1ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b701f65fd5fd6fd931a0086dfe6ad71f6343c04017539348b0295cc251baaa`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
# Sat, 19 Mar 2022 14:43:22 GMT
RUN mkdir -p /usr/src/app
# Sat, 19 Mar 2022 14:43:22 GMT
WORKDIR /usr/src/app
# Sat, 19 Mar 2022 14:43:22 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD RUN bundle install --system
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea769075fdac5823dd9a65c47092ca41c9676fd2c3dd3fb70fc5300845546c2b`  
		Last Modified: Sat, 19 Mar 2022 14:48:40 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jdk`

```console
$ docker pull jruby@sha256:7185266f95d632f6f6a004dd73658f7f603e6b40ad88eafcf80c25c0560716b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:a766bcb84f1971423a46c61ff377c37b78011d522bc1f3665139d069dd0771ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3d7a08960453d84ca781c2f890808b7adc52814c0688ee15062356b61b765`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jdk11`

```console
$ docker pull jruby@sha256:2272a5b39ded2076416caa4dd7b72d9afa47a4917871aa390aa0a27467431981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:76b200fd742c729bd948e06fe872afda7cbb4d36d5767f59afa08c26a17854a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365416797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e35c9fcb49c1d75c3bf1801667704bfeb5c2fd39c0d1ef099ebda08978e4132`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:03 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:26:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:26:31 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:42:23 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:42:23 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:26 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:27 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:42:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:42:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f30a831c1a9aca6f978e51ea8ed88eaff501aa9a21062c95de6d89e1016e2`  
		Last Modified: Sat, 19 Mar 2022 10:45:08 GMT  
		Size: 5.3 MB (5286496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea684d520abfaeda4a91b1f05dcfdd7d78fe488a5b8b2df6ac9eb6e6160e8718`  
		Last Modified: Sat, 19 Mar 2022 10:45:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dac09b64de5415f528e3a4a2540c594392b379e925448a7dcd2e5a8c3c03c46`  
		Last Modified: Sat, 19 Mar 2022 10:45:23 GMT  
		Size: 203.3 MB (203260532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32488f910728c22a3b1cb670a048ddf9dc044368709455c69ba9933d61114f37`  
		Last Modified: Sat, 19 Mar 2022 14:46:19 GMT  
		Size: 7.9 MB (7855689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7e7baeb62ee0ffa475ac3cf2c2cff1603ffc00c0c2e20c080941ad67790d03`  
		Last Modified: Sat, 19 Mar 2022 14:48:10 GMT  
		Size: 27.9 MB (27850009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339c5631a69f7787ce2cca8107aa47a0cb3419526e0ab01c3d530cfdb9e672c3`  
		Last Modified: Sat, 19 Mar 2022 14:48:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12ed74047d5052bdc5d5e89a20e701e1a5c7e5f1a959ed82f2502548ef2c73`  
		Last Modified: Sat, 19 Mar 2022 14:48:08 GMT  
		Size: 1.1 MB (1051171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b466d6c6d629c81f661c4b28ca98b0e23c314f0606b3ed8ebab0c88d2935379c`  
		Last Modified: Sat, 19 Mar 2022 14:48:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jdk17`

```console
$ docker pull jruby@sha256:34aaf313a166e6d8c906dbdad953b321d82128fdcee58b9a28616062f70218ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:78043bb5a3c2357f03f8d579940dd1a0dfe39abd422d5414044d4d022bafcf4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358424768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43971257875fad8be4c6472cb153e65d96ae7ddba19f9ca5e6ab65630498d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:23:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 19 Mar 2022 10:23:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:23:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:23:09 GMT
ENV JAVA_VERSION=17.0.2
# Sat, 19 Mar 2022 10:23:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:23:19 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:42:52 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:42:52 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:56 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:43:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:43:14 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:43:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:43:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25299f1f342403e9c0e28d57d5a4da4470e18083460fa540e198be442286c9c`  
		Last Modified: Sat, 19 Mar 2022 10:36:56 GMT  
		Size: 13.9 MB (13921274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57415387047b38bce51b83f76ee83dd55e93536d6feeac693ba47470bada257`  
		Last Modified: Sat, 19 Mar 2022 10:42:04 GMT  
		Size: 187.6 MB (187632031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbdfc195411eabe8bc79554f459e7fda7c6ddf81cf559de48f3d0a2daa25845`  
		Last Modified: Sat, 19 Mar 2022 14:46:35 GMT  
		Size: 7.9 MB (7857496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca65493d6fa917993be6aa6ad9ab747beda4fc516a90887a6044cb193c5b9c`  
		Last Modified: Sat, 19 Mar 2022 14:48:27 GMT  
		Size: 27.9 MB (27850071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7b11784031401e99605fee60792e588b0fb5a23ef9c33fd2f46597534e0c27`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1168f294dfc7785e88d849178a23f2dcdda99f40450be3dcb5333a1b3e4a7`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 1.1 MB (1051208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e134f6ee6e8de0943e52ed09c44dcaea04f55dcb3094448de773f933912928c`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jdk8`

```console
$ docker pull jruby@sha256:7185266f95d632f6f6a004dd73658f7f603e6b40ad88eafcf80c25c0560716b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:a766bcb84f1971423a46c61ff377c37b78011d522bc1f3665139d069dd0771ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3d7a08960453d84ca781c2f890808b7adc52814c0688ee15062356b61b765`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jre`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jre` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jre11`

```console
$ docker pull jruby@sha256:4c0963562b2b93b8879c96dfb16cbe16fd0e49f4a32b5dcf2e2cc924101a3b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:fdd2f792bbeea1855079a5af8dd39ea63725ea80368668edadd1e554232e3a50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157411164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70703a946819dc8c3fdb20cd599ff6fdc33087490c9cec82796f5d22e8040b0c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 14:39:37 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:59 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:59 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:02 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:42:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:42:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:42:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca486c90ae5fe6f88923feab4a27336ade1136701513bdb8155331fbe1c532`  
		Last Modified: Sat, 19 Mar 2022 14:46:03 GMT  
		Size: 7.8 MB (7829188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca684b5e244d75fa1d3079f61a18d318c4fe5c67e6513744d979b8e62b3f78d`  
		Last Modified: Sat, 19 Mar 2022 14:47:53 GMT  
		Size: 27.8 MB (27849800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f506d2332b3956f40d2b8ac6effa0b775b73847a125aa1fb9e88f9ca58e0bab9`  
		Last Modified: Sat, 19 Mar 2022 14:47:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b86cce8b12ad3ca94a57a5a8e79516574056f42f577c221856cbe3478f733`  
		Last Modified: Sat, 19 Mar 2022 14:47:51 GMT  
		Size: 1.1 MB (1051162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082d7c54d3b5f913c8d07b57778e6e7e14fc078fd48e7109b44d87caca4714a9`  
		Last Modified: Sat, 19 Mar 2022 14:47:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-jre8`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20-onbuild`

```console
$ docker pull jruby@sha256:02ec04cb1a6f6aabb5f231de8664890f23a739481bc8baf68a36a51641875eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:3567208690b5a44249644969338cda86e61f35420b6f8277b3228f56c0e0e1ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b701f65fd5fd6fd931a0086dfe6ad71f6343c04017539348b0295cc251baaa`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
# Sat, 19 Mar 2022 14:43:22 GMT
RUN mkdir -p /usr/src/app
# Sat, 19 Mar 2022 14:43:22 GMT
WORKDIR /usr/src/app
# Sat, 19 Mar 2022 14:43:22 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD RUN bundle install --system
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea769075fdac5823dd9a65c47092ca41c9676fd2c3dd3fb70fc5300845546c2b`  
		Last Modified: Sat, 19 Mar 2022 14:48:40 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.0-jdk`

```console
$ docker pull jruby@sha256:7185266f95d632f6f6a004dd73658f7f603e6b40ad88eafcf80c25c0560716b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:a766bcb84f1971423a46c61ff377c37b78011d522bc1f3665139d069dd0771ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3d7a08960453d84ca781c2f890808b7adc52814c0688ee15062356b61b765`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.0-jre`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.0-jre8`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.1`

```console
$ docker pull jruby@sha256:020a2509becb04f82d3179541ee43976636f004df6a5429b576c773b77dadf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.1` - linux; amd64

```console
$ docker pull jruby@sha256:ed61d8a0b18954c86c9fb212a646942826ef730e1847549b9562bf94ce1467dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153593164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c8fa65b1f9cb55af51d6e7c840f49aa8f88ba90799383fd475d8dfecd58dfc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:12 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:15 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13fe339a409001c64358039abb1322f0abd5153032d1d121275d8edf3c3f03`  
		Last Modified: Sat, 19 Mar 2022 14:46:52 GMT  
		Size: 27.8 MB (27849821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca9eb45196d2768cecad9c7349bd2857b55c3852444508ef59b895ac9b33b46`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8d41e63041af38f649fdb20443ae64612cd414fbb014aa7ed4ed1ba2de050`  
		Last Modified: Sat, 19 Mar 2022 14:46:50 GMT  
		Size: 1.1 MB (1051196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15adadd57187a67d118890b1eb618601088384034f6897d7d4a68ffa27d64892`  
		Last Modified: Sat, 19 Mar 2022 14:46:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.1-jdk11`

```console
$ docker pull jruby@sha256:2272a5b39ded2076416caa4dd7b72d9afa47a4917871aa390aa0a27467431981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.1-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:76b200fd742c729bd948e06fe872afda7cbb4d36d5767f59afa08c26a17854a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365416797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e35c9fcb49c1d75c3bf1801667704bfeb5c2fd39c0d1ef099ebda08978e4132`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:03 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:26:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:26:31 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:42:23 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:42:23 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:26 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:27 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:42:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:42:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f30a831c1a9aca6f978e51ea8ed88eaff501aa9a21062c95de6d89e1016e2`  
		Last Modified: Sat, 19 Mar 2022 10:45:08 GMT  
		Size: 5.3 MB (5286496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea684d520abfaeda4a91b1f05dcfdd7d78fe488a5b8b2df6ac9eb6e6160e8718`  
		Last Modified: Sat, 19 Mar 2022 10:45:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dac09b64de5415f528e3a4a2540c594392b379e925448a7dcd2e5a8c3c03c46`  
		Last Modified: Sat, 19 Mar 2022 10:45:23 GMT  
		Size: 203.3 MB (203260532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32488f910728c22a3b1cb670a048ddf9dc044368709455c69ba9933d61114f37`  
		Last Modified: Sat, 19 Mar 2022 14:46:19 GMT  
		Size: 7.9 MB (7855689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7e7baeb62ee0ffa475ac3cf2c2cff1603ffc00c0c2e20c080941ad67790d03`  
		Last Modified: Sat, 19 Mar 2022 14:48:10 GMT  
		Size: 27.9 MB (27850009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339c5631a69f7787ce2cca8107aa47a0cb3419526e0ab01c3d530cfdb9e672c3`  
		Last Modified: Sat, 19 Mar 2022 14:48:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12ed74047d5052bdc5d5e89a20e701e1a5c7e5f1a959ed82f2502548ef2c73`  
		Last Modified: Sat, 19 Mar 2022 14:48:08 GMT  
		Size: 1.1 MB (1051171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b466d6c6d629c81f661c4b28ca98b0e23c314f0606b3ed8ebab0c88d2935379c`  
		Last Modified: Sat, 19 Mar 2022 14:48:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.1-jdk17`

```console
$ docker pull jruby@sha256:34aaf313a166e6d8c906dbdad953b321d82128fdcee58b9a28616062f70218ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.1-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:78043bb5a3c2357f03f8d579940dd1a0dfe39abd422d5414044d4d022bafcf4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358424768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43971257875fad8be4c6472cb153e65d96ae7ddba19f9ca5e6ab65630498d`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:23:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 19 Mar 2022 10:23:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:23:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:23:09 GMT
ENV JAVA_VERSION=17.0.2
# Sat, 19 Mar 2022 10:23:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:23:19 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:42:52 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:42:52 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:56 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:56 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:43:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:43:14 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:43:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:43:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25299f1f342403e9c0e28d57d5a4da4470e18083460fa540e198be442286c9c`  
		Last Modified: Sat, 19 Mar 2022 10:36:56 GMT  
		Size: 13.9 MB (13921274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57415387047b38bce51b83f76ee83dd55e93536d6feeac693ba47470bada257`  
		Last Modified: Sat, 19 Mar 2022 10:42:04 GMT  
		Size: 187.6 MB (187632031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbdfc195411eabe8bc79554f459e7fda7c6ddf81cf559de48f3d0a2daa25845`  
		Last Modified: Sat, 19 Mar 2022 14:46:35 GMT  
		Size: 7.9 MB (7857496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca65493d6fa917993be6aa6ad9ab747beda4fc516a90887a6044cb193c5b9c`  
		Last Modified: Sat, 19 Mar 2022 14:48:27 GMT  
		Size: 27.9 MB (27850071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7b11784031401e99605fee60792e588b0fb5a23ef9c33fd2f46597534e0c27`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1168f294dfc7785e88d849178a23f2dcdda99f40450be3dcb5333a1b3e4a7`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 1.1 MB (1051208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e134f6ee6e8de0943e52ed09c44dcaea04f55dcb3094448de773f933912928c`  
		Last Modified: Sat, 19 Mar 2022 14:48:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.1-jdk8`

```console
$ docker pull jruby@sha256:7185266f95d632f6f6a004dd73658f7f603e6b40ad88eafcf80c25c0560716b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.1-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:a766bcb84f1971423a46c61ff377c37b78011d522bc1f3665139d069dd0771ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3d7a08960453d84ca781c2f890808b7adc52814c0688ee15062356b61b765`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.1-jre11`

```console
$ docker pull jruby@sha256:4c0963562b2b93b8879c96dfb16cbe16fd0e49f4a32b5dcf2e2cc924101a3b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.1-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:fdd2f792bbeea1855079a5af8dd39ea63725ea80368668edadd1e554232e3a50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157411164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70703a946819dc8c3fdb20cd599ff6fdc33087490c9cec82796f5d22e8040b0c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 14:39:37 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:59 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:59 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:42:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:42:02 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:42:18 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:42:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:42:18 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:42:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:42:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca486c90ae5fe6f88923feab4a27336ade1136701513bdb8155331fbe1c532`  
		Last Modified: Sat, 19 Mar 2022 14:46:03 GMT  
		Size: 7.8 MB (7829188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca684b5e244d75fa1d3079f61a18d318c4fe5c67e6513744d979b8e62b3f78d`  
		Last Modified: Sat, 19 Mar 2022 14:47:53 GMT  
		Size: 27.8 MB (27849800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f506d2332b3956f40d2b8ac6effa0b775b73847a125aa1fb9e88f9ca58e0bab9`  
		Last Modified: Sat, 19 Mar 2022 14:47:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b86cce8b12ad3ca94a57a5a8e79516574056f42f577c221856cbe3478f733`  
		Last Modified: Sat, 19 Mar 2022 14:47:51 GMT  
		Size: 1.1 MB (1051162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082d7c54d3b5f913c8d07b57778e6e7e14fc078fd48e7109b44d87caca4714a9`  
		Last Modified: Sat, 19 Mar 2022 14:47:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.20.1-onbuild`

```console
$ docker pull jruby@sha256:02ec04cb1a6f6aabb5f231de8664890f23a739481bc8baf68a36a51641875eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.20.1-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:3567208690b5a44249644969338cda86e61f35420b6f8277b3228f56c0e0e1ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b701f65fd5fd6fd931a0086dfe6ad71f6343c04017539348b0295cc251baaa`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_VERSION=9.2.20.1
# Sat, 19 Mar 2022 14:41:36 GMT
ENV JRUBY_SHA256=79cdbc475a7041f4b44766c069051d21dd2473ce1638a0b668aa9439fb631963
# Sat, 19 Mar 2022 14:41:38 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:41:38 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:39 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:52 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:53 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:54 GMT
CMD ["irb"]
# Sat, 19 Mar 2022 14:43:22 GMT
RUN mkdir -p /usr/src/app
# Sat, 19 Mar 2022 14:43:22 GMT
WORKDIR /usr/src/app
# Sat, 19 Mar 2022 14:43:22 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD RUN bundle install --system
# Sat, 19 Mar 2022 14:43:23 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7bbd9ffb89cbff0b7ef2435f13b4c71b92b24c239fc44c7df59bb8e82b190`  
		Last Modified: Sat, 19 Mar 2022 14:47:27 GMT  
		Size: 27.8 MB (27849964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d98181df56c87f653d57defad9f6ddf119ad9347cd60c5dfe5ec65db912ca7`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb31e448b6d2c8d17396ca081fe85779607f57739b7a884424aae7d34997d3`  
		Last Modified: Sat, 19 Mar 2022 14:47:24 GMT  
		Size: 1.1 MB (1051163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125f5c3387554052dbe476b90056f45f5c36a774d37986b4f07da31f2f8966c`  
		Last Modified: Sat, 19 Mar 2022 14:47:23 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea769075fdac5823dd9a65c47092ca41c9676fd2c3dd3fb70fc5300845546c2b`  
		Last Modified: Sat, 19 Mar 2022 14:48:40 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk11`

```console
$ docker pull jruby@sha256:123632ea0806bebb82ad8f68d5c3b038e8bf938bfb2d2f0db13a5195d657a119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:eed781203d95525cb104fec95b7e06f4cc3990d2ee4a22ece4f77933f4fb3f05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365343666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8471db1dc200b5ebea5a0ec38ea9582534094e182500e40a1e01c23ba8a6f99`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:03 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:26:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:26:31 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:40:18 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:40:18 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:40:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:40:20 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:40:35 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:40:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:35 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:40:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f30a831c1a9aca6f978e51ea8ed88eaff501aa9a21062c95de6d89e1016e2`  
		Last Modified: Sat, 19 Mar 2022 10:45:08 GMT  
		Size: 5.3 MB (5286496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea684d520abfaeda4a91b1f05dcfdd7d78fe488a5b8b2df6ac9eb6e6160e8718`  
		Last Modified: Sat, 19 Mar 2022 10:45:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dac09b64de5415f528e3a4a2540c594392b379e925448a7dcd2e5a8c3c03c46`  
		Last Modified: Sat, 19 Mar 2022 10:45:23 GMT  
		Size: 203.3 MB (203260532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32488f910728c22a3b1cb670a048ddf9dc044368709455c69ba9933d61114f37`  
		Last Modified: Sat, 19 Mar 2022 14:46:19 GMT  
		Size: 7.9 MB (7855689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827b31014a6ef2529c5ff0992843737edc9ae7661b3fee05d5ae7d60ab2ed26c`  
		Last Modified: Sat, 19 Mar 2022 14:46:21 GMT  
		Size: 27.8 MB (27776755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1218f5fbf39d5915071a74e97bbf4c3ca83f4bfe4f15626440cbef73641de811`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c00c9d0cb7cdbc7ed9281b0a331e0e6d5302bbafb6da0ddc90d69ad5badbe39`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 1.1 MB (1051294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d74a270fae58525a043b1360e5e2dba672a7dc62d30a9be1c087521273ddc36`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:d113e82ea192d118fe7b4d48cde37c13f881c69d81736d2efd413ce3c5f5e888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:3a3e468c40b4fdde64221508a1f0a4f3d0e9a6e2c852161c8948fcee8e529690
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358350980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b66cfa0a09bd188fc2c42706e85c59dfbc4558a04728c527c6faa041843952`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:23:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 19 Mar 2022 10:23:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:23:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:23:09 GMT
ENV JAVA_VERSION=17.0.2
# Sat, 19 Mar 2022 10:23:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:23:19 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:40:43 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:40:43 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:40:47 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:40:47 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:48 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25299f1f342403e9c0e28d57d5a4da4470e18083460fa540e198be442286c9c`  
		Last Modified: Sat, 19 Mar 2022 10:36:56 GMT  
		Size: 13.9 MB (13921274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57415387047b38bce51b83f76ee83dd55e93536d6feeac693ba47470bada257`  
		Last Modified: Sat, 19 Mar 2022 10:42:04 GMT  
		Size: 187.6 MB (187632031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbdfc195411eabe8bc79554f459e7fda7c6ddf81cf559de48f3d0a2daa25845`  
		Last Modified: Sat, 19 Mar 2022 14:46:35 GMT  
		Size: 7.9 MB (7857496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eb02b3f3611e4a8afe0f2f1cb4a11d2adf42f131e6aded517586c891487e03`  
		Last Modified: Sat, 19 Mar 2022 14:46:37 GMT  
		Size: 27.8 MB (27776226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2d9c4f522f4bd1b637ae0f3d0848e353a38cc66b0a3fbd7d4ca61f2b251cfd`  
		Last Modified: Sat, 19 Mar 2022 14:46:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f80380fafcf5df83498ce5778a0d5e3df9253722fe15c2c535ec1610dc64f3`  
		Last Modified: Sat, 19 Mar 2022 14:46:34 GMT  
		Size: 1.1 MB (1051265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa338ca74d999d3d490400e82c55959955e44f9c7655f6ab2d39d1b30151dc3`  
		Last Modified: Sat, 19 Mar 2022 14:46:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk8`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre11`

```console
$ docker pull jruby@sha256:200f73085cc68e2ac60986cba71f1b3555bd5620ed0d8049c3f7f3f93376fb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:9d746c1abf8abe58ac0debb65357b3ac1d1c7260bba2e2ec47dfbe02d1cd7bad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157337579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ded8b53e2188eb20eda02c382822fef39ab47300c491b0aaac830774666f70c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 14:39:37 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:39:37 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:39:38 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:43 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:40:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:40:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:40:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca486c90ae5fe6f88923feab4a27336ade1136701513bdb8155331fbe1c532`  
		Last Modified: Sat, 19 Mar 2022 14:46:03 GMT  
		Size: 7.8 MB (7829188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d111b6636983a932724da6abe00f1a8197d90a5671d59615b77b25c6882af7c8`  
		Last Modified: Sat, 19 Mar 2022 14:46:04 GMT  
		Size: 27.8 MB (27776084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a90d6af1f62f55d3c3935e9b74c0872cdf25144a6d7d5fcf8cd7e995000a7e0`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a391ac0c07d00024c453345af3d67c43b857e53217b10f33dd97d8f2b1bec7`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 1.1 MB (1051292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f009d48dee0231ce101b5ddccec0b3ab2ef727a996c5d9785470fcfa6682fb`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre8`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jdk`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jdk11`

```console
$ docker pull jruby@sha256:123632ea0806bebb82ad8f68d5c3b038e8bf938bfb2d2f0db13a5195d657a119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:eed781203d95525cb104fec95b7e06f4cc3990d2ee4a22ece4f77933f4fb3f05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365343666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8471db1dc200b5ebea5a0ec38ea9582534094e182500e40a1e01c23ba8a6f99`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:03 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:26:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:26:31 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:40:18 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:40:18 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:40:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:40:20 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:40:35 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:40:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:35 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:40:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f30a831c1a9aca6f978e51ea8ed88eaff501aa9a21062c95de6d89e1016e2`  
		Last Modified: Sat, 19 Mar 2022 10:45:08 GMT  
		Size: 5.3 MB (5286496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea684d520abfaeda4a91b1f05dcfdd7d78fe488a5b8b2df6ac9eb6e6160e8718`  
		Last Modified: Sat, 19 Mar 2022 10:45:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dac09b64de5415f528e3a4a2540c594392b379e925448a7dcd2e5a8c3c03c46`  
		Last Modified: Sat, 19 Mar 2022 10:45:23 GMT  
		Size: 203.3 MB (203260532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32488f910728c22a3b1cb670a048ddf9dc044368709455c69ba9933d61114f37`  
		Last Modified: Sat, 19 Mar 2022 14:46:19 GMT  
		Size: 7.9 MB (7855689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827b31014a6ef2529c5ff0992843737edc9ae7661b3fee05d5ae7d60ab2ed26c`  
		Last Modified: Sat, 19 Mar 2022 14:46:21 GMT  
		Size: 27.8 MB (27776755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1218f5fbf39d5915071a74e97bbf4c3ca83f4bfe4f15626440cbef73641de811`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c00c9d0cb7cdbc7ed9281b0a331e0e6d5302bbafb6da0ddc90d69ad5badbe39`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 1.1 MB (1051294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d74a270fae58525a043b1360e5e2dba672a7dc62d30a9be1c087521273ddc36`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jdk17`

```console
$ docker pull jruby@sha256:d113e82ea192d118fe7b4d48cde37c13f881c69d81736d2efd413ce3c5f5e888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:3a3e468c40b4fdde64221508a1f0a4f3d0e9a6e2c852161c8948fcee8e529690
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358350980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b66cfa0a09bd188fc2c42706e85c59dfbc4558a04728c527c6faa041843952`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:23:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 19 Mar 2022 10:23:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:23:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:23:09 GMT
ENV JAVA_VERSION=17.0.2
# Sat, 19 Mar 2022 10:23:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:23:19 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:40:43 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:40:43 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:40:47 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:40:47 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:48 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25299f1f342403e9c0e28d57d5a4da4470e18083460fa540e198be442286c9c`  
		Last Modified: Sat, 19 Mar 2022 10:36:56 GMT  
		Size: 13.9 MB (13921274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57415387047b38bce51b83f76ee83dd55e93536d6feeac693ba47470bada257`  
		Last Modified: Sat, 19 Mar 2022 10:42:04 GMT  
		Size: 187.6 MB (187632031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbdfc195411eabe8bc79554f459e7fda7c6ddf81cf559de48f3d0a2daa25845`  
		Last Modified: Sat, 19 Mar 2022 14:46:35 GMT  
		Size: 7.9 MB (7857496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eb02b3f3611e4a8afe0f2f1cb4a11d2adf42f131e6aded517586c891487e03`  
		Last Modified: Sat, 19 Mar 2022 14:46:37 GMT  
		Size: 27.8 MB (27776226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2d9c4f522f4bd1b637ae0f3d0848e353a38cc66b0a3fbd7d4ca61f2b251cfd`  
		Last Modified: Sat, 19 Mar 2022 14:46:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f80380fafcf5df83498ce5778a0d5e3df9253722fe15c2c535ec1610dc64f3`  
		Last Modified: Sat, 19 Mar 2022 14:46:34 GMT  
		Size: 1.1 MB (1051265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa338ca74d999d3d490400e82c55959955e44f9c7655f6ab2d39d1b30151dc3`  
		Last Modified: Sat, 19 Mar 2022 14:46:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jdk8`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jre`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jre11`

```console
$ docker pull jruby@sha256:200f73085cc68e2ac60986cba71f1b3555bd5620ed0d8049c3f7f3f93376fb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:9d746c1abf8abe58ac0debb65357b3ac1d1c7260bba2e2ec47dfbe02d1cd7bad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157337579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ded8b53e2188eb20eda02c382822fef39ab47300c491b0aaac830774666f70c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 14:39:37 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:39:37 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:39:38 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:43 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:40:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:40:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:40:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca486c90ae5fe6f88923feab4a27336ade1136701513bdb8155331fbe1c532`  
		Last Modified: Sat, 19 Mar 2022 14:46:03 GMT  
		Size: 7.8 MB (7829188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d111b6636983a932724da6abe00f1a8197d90a5671d59615b77b25c6882af7c8`  
		Last Modified: Sat, 19 Mar 2022 14:46:04 GMT  
		Size: 27.8 MB (27776084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a90d6af1f62f55d3c3935e9b74c0872cdf25144a6d7d5fcf8cd7e995000a7e0`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a391ac0c07d00024c453345af3d67c43b857e53217b10f33dd97d8f2b1bec7`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 1.1 MB (1051292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f009d48dee0231ce101b5ddccec0b3ab2ef727a996c5d9785470fcfa6682fb`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3-jre8`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jdk`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jdk11`

```console
$ docker pull jruby@sha256:123632ea0806bebb82ad8f68d5c3b038e8bf938bfb2d2f0db13a5195d657a119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:eed781203d95525cb104fec95b7e06f4cc3990d2ee4a22ece4f77933f4fb3f05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365343666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8471db1dc200b5ebea5a0ec38ea9582534094e182500e40a1e01c23ba8a6f99`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:26:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:26:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:26:03 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:26:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:26:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:26:31 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:40:18 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:40:18 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:40:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:40:20 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:40:35 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:40:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:35 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:40:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7f30a831c1a9aca6f978e51ea8ed88eaff501aa9a21062c95de6d89e1016e2`  
		Last Modified: Sat, 19 Mar 2022 10:45:08 GMT  
		Size: 5.3 MB (5286496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea684d520abfaeda4a91b1f05dcfdd7d78fe488a5b8b2df6ac9eb6e6160e8718`  
		Last Modified: Sat, 19 Mar 2022 10:45:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dac09b64de5415f528e3a4a2540c594392b379e925448a7dcd2e5a8c3c03c46`  
		Last Modified: Sat, 19 Mar 2022 10:45:23 GMT  
		Size: 203.3 MB (203260532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32488f910728c22a3b1cb670a048ddf9dc044368709455c69ba9933d61114f37`  
		Last Modified: Sat, 19 Mar 2022 14:46:19 GMT  
		Size: 7.9 MB (7855689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827b31014a6ef2529c5ff0992843737edc9ae7661b3fee05d5ae7d60ab2ed26c`  
		Last Modified: Sat, 19 Mar 2022 14:46:21 GMT  
		Size: 27.8 MB (27776755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1218f5fbf39d5915071a74e97bbf4c3ca83f4bfe4f15626440cbef73641de811`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c00c9d0cb7cdbc7ed9281b0a331e0e6d5302bbafb6da0ddc90d69ad5badbe39`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 1.1 MB (1051294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d74a270fae58525a043b1360e5e2dba672a7dc62d30a9be1c087521273ddc36`  
		Last Modified: Sat, 19 Mar 2022 14:46:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jdk17`

```console
$ docker pull jruby@sha256:d113e82ea192d118fe7b4d48cde37c13f881c69d81736d2efd413ce3c5f5e888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:3a3e468c40b4fdde64221508a1f0a4f3d0e9a6e2c852161c8948fcee8e529690
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358350980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b66cfa0a09bd188fc2c42706e85c59dfbc4558a04728c527c6faa041843952`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:32:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:23:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 19 Mar 2022 10:23:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:23:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:23:09 GMT
ENV JAVA_VERSION=17.0.2
# Sat, 19 Mar 2022 10:23:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:23:19 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 14:40:43 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:40:43 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:40:43 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:40:47 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:40:47 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:48 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:41:06 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:41:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:41:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:41:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:41:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260dee23bc81622ef145aff36ad9816cca1c98bfa9361ad1bdf03c8975b104e`  
		Last Modified: Fri, 18 Mar 2022 07:05:07 GMT  
		Size: 51.8 MB (51843594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25299f1f342403e9c0e28d57d5a4da4470e18083460fa540e198be442286c9c`  
		Last Modified: Sat, 19 Mar 2022 10:36:56 GMT  
		Size: 13.9 MB (13921274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57415387047b38bce51b83f76ee83dd55e93536d6feeac693ba47470bada257`  
		Last Modified: Sat, 19 Mar 2022 10:42:04 GMT  
		Size: 187.6 MB (187632031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbdfc195411eabe8bc79554f459e7fda7c6ddf81cf559de48f3d0a2daa25845`  
		Last Modified: Sat, 19 Mar 2022 14:46:35 GMT  
		Size: 7.9 MB (7857496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eb02b3f3611e4a8afe0f2f1cb4a11d2adf42f131e6aded517586c891487e03`  
		Last Modified: Sat, 19 Mar 2022 14:46:37 GMT  
		Size: 27.8 MB (27776226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2d9c4f522f4bd1b637ae0f3d0848e353a38cc66b0a3fbd7d4ca61f2b251cfd`  
		Last Modified: Sat, 19 Mar 2022 14:46:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f80380fafcf5df83498ce5778a0d5e3df9253722fe15c2c535ec1610dc64f3`  
		Last Modified: Sat, 19 Mar 2022 14:46:34 GMT  
		Size: 1.1 MB (1051265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa338ca74d999d3d490400e82c55959955e44f9c7655f6ab2d39d1b30151dc3`  
		Last Modified: Sat, 19 Mar 2022 14:46:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jdk8`

```console
$ docker pull jruby@sha256:c1411b720a82d5f6d1f9e2dfd786a315193f716fab5bd10e3834689694b120ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:4099a2624ffa4ac488367b435f2607874d6eed525618d1560459d7251f7be33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272570413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e7910b8c718db41bb887b0da58d086cb7c8cf0594f9583594574127b16c9e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:28:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:28:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:28:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:39 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:28:39 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:29:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 19 Mar 2022 14:38:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:56 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:01 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:01 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:02 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:39:21 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:39:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:39:22 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:39:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd8f6c2501f1cdc9feb11cba7ec67178be0baee18065067ecd65548f5aa7b0`  
		Last Modified: Sat, 19 Mar 2022 10:44:15 GMT  
		Size: 5.4 MB (5420190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c168de4f14ac464e66e39438fdd88a923ab323cd8583342a37fee178532f1d8`  
		Last Modified: Sat, 19 Mar 2022 10:47:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44516a0bcb601ed7c8b565ba6447d463c6cc7d8f658ff6d1046d925d458ee172`  
		Last Modified: Sat, 19 Mar 2022 10:47:58 GMT  
		Size: 106.1 MB (106072290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48c7109a757242371a14307a860e584ee3dcdd43d1d2a5ac87b2f461f20c90b`  
		Last Modified: Sat, 19 Mar 2022 14:45:29 GMT  
		Size: 6.7 MB (6724000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86849aec6ea1dfa8bc8558cf80e9d43f7d75763d1694c891934470cf3c2f5e2e`  
		Last Modified: Sat, 19 Mar 2022 14:45:30 GMT  
		Size: 27.8 MB (27776688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea7c17ac403cc6ba03d34022e76a443010ffcae6574c341e4bd688cc18a19d`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd525553a4e662b2ae608249d147c124541ab8817971ae2edf0db746925e1b9`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 1.1 MB (1051322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecad6273c368469ad645a1fdfbd51b4101609539f9418a804236426233b3f69`  
		Last Modified: Sat, 19 Mar 2022 14:45:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jre`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jre11`

```console
$ docker pull jruby@sha256:200f73085cc68e2ac60986cba71f1b3555bd5620ed0d8049c3f7f3f93376fb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:9d746c1abf8abe58ac0debb65357b3ac1d1c7260bba2e2ec47dfbe02d1cd7bad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157337579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ded8b53e2188eb20eda02c382822fef39ab47300c491b0aaac830774666f70c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 19 Mar 2022 10:27:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:27:31 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:27:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:27:32 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:27:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 19 Mar 2022 14:39:37 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:39:37 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:39:38 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:39:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:39:43 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:39:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:40:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:40:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:40:04 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:40:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:40:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e469609e9ec2676caa5d062ead7d0f994058374f53b23c6a33a8a20d86e34d0a`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c688f20bd440c61c0446aa66f3570f9c2175adf6dd85c64b7c1d47e749d8573`  
		Last Modified: Sat, 19 Mar 2022 10:46:26 GMT  
		Size: 46.9 MB (46879453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca486c90ae5fe6f88923feab4a27336ade1136701513bdb8155331fbe1c532`  
		Last Modified: Sat, 19 Mar 2022 14:46:03 GMT  
		Size: 7.8 MB (7829188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d111b6636983a932724da6abe00f1a8197d90a5671d59615b77b25c6882af7c8`  
		Last Modified: Sat, 19 Mar 2022 14:46:04 GMT  
		Size: 27.8 MB (27776084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a90d6af1f62f55d3c3935e9b74c0872cdf25144a6d7d5fcf8cd7e995000a7e0`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a391ac0c07d00024c453345af3d67c43b857e53217b10f33dd97d8f2b1bec7`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 1.1 MB (1051292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f009d48dee0231ce101b5ddccec0b3ab2ef727a996c5d9785470fcfa6682fb`  
		Last Modified: Sat, 19 Mar 2022 14:46:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.3.0-jre8`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.3.3.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:latest`

```console
$ docker pull jruby@sha256:c448764964c791247f14de04c60ff68b384369ed464f293b95c70477af6c7513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:fda5a11318b6407e329ecfa1e9ceb46ab74aafc2180076248ff3391278368297
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153520104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5a0cf49eb70d09a5609f5aa72ec44d62c46bbb382cfc6e00b8501b07d9f6c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:29:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:29:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:29:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:29:54 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:29:54 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 14:38:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_VERSION=9.3.3.0
# Sat, 19 Mar 2022 14:38:21 GMT
ENV JRUBY_SHA256=3da828cbe287d5468507f1c2c42bef6cf34bc5361bcd6a5d99c207b21b9fdc5c
# Sat, 19 Mar 2022 14:38:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Sat, 19 Mar 2022 14:38:24 GMT
ENV PATH=/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Sat, 19 Mar 2022 14:38:38 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Sat, 19 Mar 2022 14:38:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 19 Mar 2022 14:38:39 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 14:38:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 19 Mar 2022 14:38:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e0bf408c56987056d977bb11f39372d03d2f422d5860b0dcaf279163962e8a`  
		Last Modified: Sat, 19 Mar 2022 10:45:53 GMT  
		Size: 5.7 MB (5657082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f906c7a05a96d1a02e10b9e15899c1b50c1f2626d2c909e4aeede63977eab`  
		Last Modified: Sat, 19 Mar 2022 10:48:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f30cb1f647ca626f04737867a423fa81c990fa30218bc084d694a0ba0afb2`  
		Last Modified: Sat, 19 Mar 2022 10:48:52 GMT  
		Size: 41.4 MB (41387584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b61bad63f725821458e2e4029f5b619ca1eaddb3823f24daa55b4b76873986`  
		Last Modified: Sat, 19 Mar 2022 14:44:47 GMT  
		Size: 6.7 MB (6698697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1811f89337a0aa99b2d06ed835707827ace94bb57cec906a12de7689ea7e664`  
		Last Modified: Sat, 19 Mar 2022 14:44:48 GMT  
		Size: 27.8 MB (27776656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe36fb5cf49d0179b3c3eb8bb7c85575fa6af6cc9828acfb58ab5c2b37a8dd6`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f200104ad00bd76eb16aa19ab7ee4c838d8d02782e715a8779b9764e482fa8`  
		Last Modified: Sat, 19 Mar 2022 14:44:45 GMT  
		Size: 1.1 MB (1051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25612f588569d12043a64d64003064239b39d51e6400e17b3aceafb6869493e`  
		Last Modified: Sat, 19 Mar 2022 14:44:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
