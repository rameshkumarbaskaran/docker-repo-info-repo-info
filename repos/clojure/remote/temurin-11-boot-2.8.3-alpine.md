## `clojure:temurin-11-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:10dade73cc101e2c191cd40bf997b4784f896199f98ff8eeb45dfcf8a71c1c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a2525ad573b4d722c120d994da50532e6950ef3a2db152cf89c904cb825c6f48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268920464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63abbad88fff8c9def0857980c7960d936e407854e6552e5c537c969a3499379`
-	Default Command: `["boot","repl"]`

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
# Mon, 09 Jan 2023 17:40:44 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Mon, 09 Jan 2023 17:40:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='774d5955c09893dda14e3eb0fd3e239a6b2cec58615fcf4ec68747260b6e1cc1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 09 Jan 2023 17:41:00 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 09 Jan 2023 17:41:00 GMT
CMD ["jshell"]
# Mon, 09 Jan 2023 21:30:51 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 09 Jan 2023 21:30:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 09 Jan 2023 21:30:51 GMT
WORKDIR /tmp
# Mon, 09 Jan 2023 21:30:53 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 09 Jan 2023 21:30:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Jan 2023 21:30:53 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 09 Jan 2023 21:31:38 GMT
RUN boot
# Mon, 09 Jan 2023 21:31:38 GMT
CMD ["boot" "repl"]
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
	-	`sha256:757b01b0b48f99a2f5e239f173b15678e8f1c1c91cb98fa568e12ed3ccaaeafe`  
		Last Modified: Mon, 09 Jan 2023 17:45:32 GMT  
		Size: 193.8 MB (193812585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd76e48fe00d19e510bc7b4b236ab01963c83cc619d3ff619c87c5f67603813`  
		Last Modified: Mon, 09 Jan 2023 17:45:18 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fbdc72df21590d3b0fcdd3105acc6b20b98010096f9c2313e00ecafa838793`  
		Last Modified: Mon, 09 Jan 2023 21:38:20 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86263eae086212d941e39a900e0e27c1de1c1b2558de383c7b4efd8b0eee7c5c`  
		Last Modified: Mon, 09 Jan 2023 21:38:24 GMT  
		Size: 58.8 MB (58820864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
