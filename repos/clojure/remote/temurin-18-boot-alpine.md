## `clojure:temurin-18-boot-alpine`

```console
$ docker pull clojure@sha256:0416ffb3e8f3534e0f5d59058c35be6041ecd17e9cfe074ad823a582cdeb9b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:f0773cc36ae56c8ebd751504a0ef2ca08eae4460547bdeb5e336d60647fac9c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267426857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf32f87fb8a828a47a8111e31fd96952f7af800eb2e6dbcf77af08fbf943588`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Jul 2022 16:20:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 02 Aug 2022 19:09:34 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 19:09:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 19:09:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 19:09:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 02 Aug 2022 19:09:55 GMT
CMD ["jshell"]
# Wed, 03 Aug 2022 12:17:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 Aug 2022 12:17:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 Aug 2022 12:17:53 GMT
WORKDIR /tmp
# Wed, 03 Aug 2022 12:17:55 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 03 Aug 2022 12:17:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 Aug 2022 12:17:55 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 Aug 2022 12:18:15 GMT
RUN boot
# Wed, 03 Aug 2022 12:18:15 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 Aug 2022 12:18:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 Aug 2022 12:18:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2b3b9d0d1a1f972083dde62c850175d26be845971e3c96ff06c8145fbe2fd0`  
		Last Modified: Thu, 28 Jul 2022 16:25:19 GMT  
		Size: 12.1 MB (12050034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63767b55bc166472c10e5963b6ad0046b42e404d6b8d5486f7a8ac826d179660`  
		Last Modified: Tue, 02 Aug 2022 19:18:32 GMT  
		Size: 192.9 MB (192897541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc4105de4129bcb708e2f690c2ac2d9e5a9d6704e5d998ca95a2ce3087cb9e4`  
		Last Modified: Tue, 02 Aug 2022 19:18:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4f4e603d1d6237bb300ffdec068fb26ce2738e4253b65615b830cbc5720230`  
		Last Modified: Wed, 03 Aug 2022 12:29:10 GMT  
		Size: 859.3 KB (859308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733352dd63f2843c211eda5d63dbda057ca0b6d7885126cbd4607807090fb52b`  
		Last Modified: Wed, 03 Aug 2022 12:29:16 GMT  
		Size: 58.8 MB (58820606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3981f41c617935d702ecadebdc833e93f481b414609c0c662401d919b6e8ac2f`  
		Last Modified: Wed, 03 Aug 2022 12:29:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
