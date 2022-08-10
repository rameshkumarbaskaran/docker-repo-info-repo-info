## `clojure:temurin-18-boot-alpine`

```console
$ docker pull clojure@sha256:ef3329741de7e2f3f1a4bbbc999324f244f3ca7bdccd094c77272ad6ff58c4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b010e74ad8de9bf5a92e3c32231224a3d3376c60cd3953147f5e9140c41c453b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267434067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db31206dfeaca048782b75f25c39289cd76ded37d65e3f96b4b38ae1a3d12fbb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:30:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 Aug 2022 01:30:26 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 10 Aug 2022 01:32:54 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 01:33:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:33:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:33:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 01:33:26 GMT
CMD ["jshell"]
# Wed, 10 Aug 2022 06:01:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Aug 2022 06:01:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Aug 2022 06:01:21 GMT
WORKDIR /tmp
# Wed, 10 Aug 2022 06:01:22 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 10 Aug 2022 06:01:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Aug 2022 06:01:23 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Aug 2022 06:01:42 GMT
RUN boot
# Wed, 10 Aug 2022 06:01:42 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Aug 2022 06:01:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Aug 2022 06:01:42 GMT
CMD ["repl"]
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
	-	`sha256:4fb9fee1c1338ebe463c13e4d7ece3e5f95cba558caa64493ce1f6cac2da0e91`  
		Last Modified: Wed, 10 Aug 2022 01:38:09 GMT  
		Size: 192.9 MB (192897563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d5b48ab638eb446c579d5c6d665eb01c2b6816d0f7d043286e500bb729184`  
		Last Modified: Wed, 10 Aug 2022 01:37:54 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5531eeb363c525e47ab1d4d65f97a5684ac50f0b1ab479c169247da24321f386`  
		Last Modified: Wed, 10 Aug 2022 06:06:44 GMT  
		Size: 859.3 KB (859311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bca1e2fb0a2b7e1130ce4fdc8d2eeccc48b8754ef72d662603d0613642127c`  
		Last Modified: Wed, 10 Aug 2022 06:06:48 GMT  
		Size: 58.8 MB (58820497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eabb852f36fbb731f3a807796f23703915ffc98a8d676b3b17bfbb074ef0dc3`  
		Last Modified: Wed, 10 Aug 2022 06:06:43 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
