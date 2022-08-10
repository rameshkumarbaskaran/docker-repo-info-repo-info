## `clojure:temurin-17-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:e185ebe68ccc51d86d65741a9fd08492fe4eb32300025998bc19ecfbae7b7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:3ddb158fa52b8ae2dc6bd8e17b534d7868ee057163b5d40441ab0df8a450660a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265986246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a57347e1e32d3f8969a56046d107bea28b544ca523c806df3eb892f962e069e`
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
# Wed, 10 Aug 2022 01:32:12 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Wed, 10 Aug 2022 01:32:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b356512c955f2d1a66b714ab3acaad942d04f80603af7dcd56e1fe5baeaeeda';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:32:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:32:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 01:32:27 GMT
CMD ["jshell"]
# Wed, 10 Aug 2022 06:00:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Aug 2022 06:00:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Aug 2022 06:00:26 GMT
WORKDIR /tmp
# Wed, 10 Aug 2022 06:00:27 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 10 Aug 2022 06:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Aug 2022 06:00:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Aug 2022 06:00:46 GMT
RUN boot
# Wed, 10 Aug 2022 06:00:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Aug 2022 06:00:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Aug 2022 06:00:46 GMT
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
	-	`sha256:d0c86cb813dfec331cd6ca3534780b06f071b028263de7b3293f47e608dc7114`  
		Last Modified: Wed, 10 Aug 2022 01:37:18 GMT  
		Size: 191.4 MB (191449948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c96b9bf38aeb2ef90b58a5955cf9dfd04b1101131538c3e336cabb6dd9df29`  
		Last Modified: Wed, 10 Aug 2022 01:37:03 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e2a6eb18c346af25bdbcdd5eac587103b801a478c9bff8d294ba3f0c3132a6`  
		Last Modified: Wed, 10 Aug 2022 06:05:37 GMT  
		Size: 859.3 KB (859323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebec88c4492fd628c4e5003695ea3beeab13f7b6e3d34877d27e3cef250f62b`  
		Last Modified: Wed, 10 Aug 2022 06:05:40 GMT  
		Size: 58.8 MB (58820279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a805b1bbcda3c1ffa16414b171dfaeac3d2072e379705bd69342d1d2e5a9e9`  
		Last Modified: Wed, 10 Aug 2022 06:05:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
