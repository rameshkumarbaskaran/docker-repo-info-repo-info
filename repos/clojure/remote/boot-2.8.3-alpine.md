## `clojure:boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:c598bb75ddea09fa883cc55d2c3e7eecd6280198b7086b9f868ed24377a5ae11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:996bf4c2c1eff8b7e7245530280ac3ce7af91a328fbf0b6ddac1e97725bff947
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266845135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade040b7923b602d18775b11302863133ca3a22f633775fb4883829dba461946`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:40:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jan 2023 17:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 17:40:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Jan 2023 17:40:11 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 09 Jan 2023 17:41:26 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Mon, 09 Jan 2023 17:41:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='cb154396ff3bfb6a9082e3640c564643d31ecae1792fab0956149ed5258ad84b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 09 Jan 2023 17:41:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 09 Jan 2023 17:41:48 GMT
CMD ["jshell"]
# Mon, 09 Jan 2023 21:32:36 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 09 Jan 2023 21:32:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 09 Jan 2023 21:32:36 GMT
WORKDIR /tmp
# Mon, 09 Jan 2023 21:32:38 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 09 Jan 2023 21:32:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Jan 2023 21:32:38 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 09 Jan 2023 21:32:58 GMT
RUN boot
# Mon, 09 Jan 2023 21:32:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 09 Jan 2023 21:32:59 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Jan 2023 21:32:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e3b32ee5a149e3ccb99051cdb52e96e11488293cdf72ee88168c88dd335c7`  
		Last Modified: Mon, 09 Jan 2023 17:44:40 GMT  
		Size: 12.0 MB (12020134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c463607450202ffe337c44b04cb674183f6cae4b0ad95de95de3e5139624a844`  
		Last Modified: Mon, 09 Jan 2023 17:46:19 GMT  
		Size: 191.7 MB (191737154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aacfe7df6acfe075630dd184d0d0fa387cc735a0812f82bfbf6b2c114704fb`  
		Last Modified: Mon, 09 Jan 2023 17:46:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d8d0e5ae8c7f48e3b7411fb3549b5fe4b37db09227b46caef116342fdd54c0`  
		Last Modified: Mon, 09 Jan 2023 21:39:08 GMT  
		Size: 896.1 KB (896075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6116bafb92cc93baeea163e91cc333faf05fe77fd48d41cae07f1153930c2a`  
		Last Modified: Mon, 09 Jan 2023 21:39:11 GMT  
		Size: 58.8 MB (58820570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6130356f2de26b2d89e74fb2ef12ccd6a92c17712992efd5c73eab79dd5e419d`  
		Last Modified: Mon, 09 Jan 2023 21:39:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
