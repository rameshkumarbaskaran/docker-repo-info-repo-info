## `clojure:temurin-8-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:6c0a8dcd89f7e98ba8f89bf1bcebc1e35acf6be09046599f7ff31f75f22e70d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b9ae387f3cd7f67581bd5c59523a63ac935812de20da3ed6aec491c648294f7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175966737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9e4d9fb6795989e017bf1302c94d02b12d77477c94617b0712d837685e8217`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Jul 2022 16:20:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 02 Aug 2022 19:04:09 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Tue, 02 Aug 2022 19:04:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='fc146a83e30a8b4f17a8558b9da58eed645a615542eea7dc942278a3c60d1efe';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 19:04:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 19:04:18 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 03 Aug 2022 12:10:46 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 Aug 2022 12:10:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 Aug 2022 12:10:47 GMT
WORKDIR /tmp
# Wed, 03 Aug 2022 12:10:48 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 03 Aug 2022 12:10:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 Aug 2022 12:10:48 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 Aug 2022 12:11:07 GMT
RUN boot
# Wed, 03 Aug 2022 12:11:08 GMT
CMD ["boot" "repl"]
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
	-	`sha256:8be0b6baf77aefface13710f3a9be5f1192921ec7b5746908cce4d65d04054f9`  
		Last Modified: Tue, 02 Aug 2022 19:13:06 GMT  
		Size: 101.4 MB (101438063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd7b5c9ba7c0d2fee9ae810b0361fe9f468b5f56c4ccda542789e3ff3bde1e2`  
		Last Modified: Tue, 02 Aug 2022 19:12:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23fcfb9ba3f3ccde4e2329eddd718ef791a40b1f0ed907940013c2473ca0939`  
		Last Modified: Wed, 03 Aug 2022 12:22:47 GMT  
		Size: 859.3 KB (859321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafe9e57f40aa95864ddf4c88819d57bd03f1820fa82c428838c359f89a82a62`  
		Last Modified: Wed, 03 Aug 2022 12:22:50 GMT  
		Size: 58.8 MB (58820353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
