## `eclipse-temurin:8u302-b08-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:3ba182fda8fc1a7b584bad500c3ede6ac869eea4ead5f767c88c24d519bce4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u302-b08-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:259019760a21d85abf527a6874821069a49ad3fed6ede263d32536787d592b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86312650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad64d8568d4727abe7bed54f223bd130023b2ba7412e0d64fe1d56485a6b3b86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:59:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Aug 2021 20:21:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Aug 2021 20:22:00 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:22:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Aug 2021 20:22:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Aug 2021 20:22:05 GMT
RUN echo Verifying install ...     && echo   java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07835b17b92ab861c8965cceb50fb949c78dfadc034faaead298983cc494906f`  
		Last Modified: Thu, 19 Aug 2021 20:23:41 GMT  
		Size: 16.0 MB (16032608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d6d46cb5dafc99d7cddddf2bd3e51092da5d10027b018b6d1f64f5a45d1de7`  
		Last Modified: Thu, 19 Aug 2021 20:23:43 GMT  
		Size: 41.7 MB (41711938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272c4372a00c532a7f86afdb1a365b2dc393c4eb7b0b83eac6b6d91c1a68249c`  
		Last Modified: Thu, 19 Aug 2021 20:23:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
