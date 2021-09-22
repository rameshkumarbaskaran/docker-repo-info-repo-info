## `eclipse-temurin:17-focal`

```console
$ docker pull eclipse-temurin@sha256:8e78f190c02e608e8f1ffeed61f73b6c0d28e47bbc0f56e25db2259f56d8af81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:864679675993349449ad5ad09efce7260a6e76b6b7f66df134247cdd2aaf640f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241318607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d987db89db6a934c10b8ed723b0fd45f7d86353758934ebfc086876b89b0bd59`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 03:32:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Sep 2021 19:57:20 GMT
ENV JAVA_VERSION=jdk-17+35
# Wed, 22 Sep 2021 19:57:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 22 Sep 2021 19:57:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Sep 2021 19:57:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Sep 2021 19:57:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501c2591907676ca691db1c93900af330416fe68009c9ceabb59897a6a5d30c7`  
		Last Modified: Tue, 31 Aug 2021 03:34:11 GMT  
		Size: 19.8 MB (19775466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dc3df9f2bc5ee8e8372dd3cea3b05894a85ae4fdc144a25290fe76ede833da`  
		Last Modified: Wed, 22 Sep 2021 20:01:27 GMT  
		Size: 193.0 MB (192972907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e983cf7b8a4c876432ac915396f0560429922aed1668ee1c14e70410481a1ead`  
		Last Modified: Wed, 22 Sep 2021 20:01:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
