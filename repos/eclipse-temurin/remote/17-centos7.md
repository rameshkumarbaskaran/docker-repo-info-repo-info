## `eclipse-temurin:17-centos7`

```console
$ docker pull eclipse-temurin@sha256:8a15f53b06baca399374accbdf7391a7460879abff3427d9465910e31b70016d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bbf3f3ea6b1879b6252e9fd0b3f99b813108082a0b9f14c48c2946c3415f6901
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281776033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1348f16a74615139057ecab402876396805f4de3ed127cf239fd9860346b4d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:53:12 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar binutils     && yum clean all
# Wed, 22 Sep 2021 19:57:35 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:57:44 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 22 Sep 2021 19:57:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Sep 2021 19:57:45 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Sep 2021 19:57:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eafaeccaf7b18df74301fade3ec58483f58947f3a10bbc458aa7fe6e063d060`  
		Last Modified: Wed, 15 Sep 2021 18:55:36 GMT  
		Size: 12.7 MB (12704282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d22ee19ecd4fd89904b3fac437c028efb727805dd41d98682a1ce579afc3a0`  
		Last Modified: Wed, 22 Sep 2021 20:01:53 GMT  
		Size: 193.0 MB (192974434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea51de58bc12d09b97947ddac0a9ce294d4f30c772b88c5377f8bce0018fc38f`  
		Last Modified: Wed, 22 Sep 2021 20:01:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
