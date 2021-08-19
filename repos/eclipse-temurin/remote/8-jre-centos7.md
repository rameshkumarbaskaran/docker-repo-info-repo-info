## `eclipse-temurin:8-jre-centos7`

```console
$ docker pull eclipse-temurin@sha256:ef0460238b5388be59a6486d4cf44909081224ed66c2b24890e9060518798ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:42e30860327a8949fb2db45ce599a0459130f633108d5e410079be41332d8340
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130517054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92450c4825a62f8cdb5af72f88b2e934226825e4d51495d1015c1cf7e4cf29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Aug 2021 21:32:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Aug 2021 20:22:39 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Thu, 19 Aug 2021 20:22:40 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:22:43 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Aug 2021 20:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Aug 2021 20:22:44 GMT
RUN echo Verifying install ...     && echo   java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1eca6508a54d6486c9579af8a665934246b75ae6125ae50edb86b793a8e727`  
		Last Modified: Thu, 19 Aug 2021 20:23:55 GMT  
		Size: 12.7 MB (12705572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d1c5b5463d3890496389fb6ee77363b5edfa800c029590e6873701e6f52484`  
		Last Modified: Thu, 19 Aug 2021 20:23:58 GMT  
		Size: 41.7 MB (41714163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6176de9b069aee30fd8976a2d84b8bfc9a97ba358fef033909acfef71ede27b6`  
		Last Modified: Thu, 19 Aug 2021 20:23:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
