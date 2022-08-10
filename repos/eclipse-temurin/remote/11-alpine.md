## `eclipse-temurin:11-alpine`

```console
$ docker pull eclipse-temurin@sha256:6cd5b89ecedeedb2faece0cdb8034fbcb4c2a53d4a6d183fc0b0b31f974834db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cafc88543d918f93b4fbd65e89c1a0e5e3339dc13ba9239118213a764cf38a3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208309697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d642ea62eda74bda67fc213920a01c3fc2664fc6ea63dae3948c47d9cda21fab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:30:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 Aug 2022 01:30:26 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 10 Aug 2022 01:31:04 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 01:31:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='32a93bd824cf34ccdde0881699a41a12722b4d8ff1d57294b2add2102432759b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:31:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:31:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 01:31:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878a9af9475f057a355a16521c6da6195d134a78707eb526021019fe67b702b5`  
		Last Modified: Wed, 10 Aug 2022 01:35:31 GMT  
		Size: 12.1 MB (12050079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a7c745b5187660c398c71d335a3bd951a6092d0c4c43ed1d5510faceeb8e21`  
		Last Modified: Wed, 10 Aug 2022 01:36:28 GMT  
		Size: 193.5 MB (193453405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e0394f18a9e1aa03979ddb6eea7af52707283762c71b856871b03677276922`  
		Last Modified: Wed, 10 Aug 2022 01:36:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
