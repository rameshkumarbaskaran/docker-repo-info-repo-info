## `clojure:temurin-8-lein-2.10.0-alpine`

```console
$ docker pull clojure@sha256:38555607968d52b44acc1849ccce1dfaad9f9a2c90e48dbe9f324b5cc345e485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-lein-2.10.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:97b1d4cb313022d3d1d966578d0bd2fe945ac7c1ee5df2ba333a72eb6059dbca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132440034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80514bc6b936c3f3d08b4452315c13ebcbda0ea0fdc3d7539616e53c74472166`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 02:50:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 02:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 02:50:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:22:37 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Thu, 02 Nov 2023 01:10:59 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 02 Nov 2023 01:11:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8dcb1532a1194afa06e4b5ace4e9e279926392442bf46b2d51b49ae1a9a1dfea';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 02 Nov 2023 01:11:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 02 Nov 2023 01:11:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 02 Nov 2023 01:11:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 Nov 2023 01:53:00 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 01:53:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:53:00 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:53:07 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 02 Nov 2023 01:53:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:53:07 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 01:53:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 01:53:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a3a37ba0a441c23edb967d901e4af5b508796b983fbb71e14ad89db9a9999`  
		Last Modified: Mon, 30 Oct 2023 23:32:06 GMT  
		Size: 9.3 MB (9276545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f85f136190f289781fafc943b0e7ce0ec60465189951784079e20706e6abc7`  
		Last Modified: Thu, 02 Nov 2023 01:14:45 GMT  
		Size: 101.5 MB (101507669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875d5e66f386474eed88a4b0db8d14e7374d2fb25a32f32d6e9286a936892d6`  
		Last Modified: Thu, 02 Nov 2023 01:14:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626e04569cb9ec561e9dcfaac22ef575cd1470e6f2ca4605a9b90c3388dbd651`  
		Last Modified: Thu, 02 Nov 2023 01:14:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63098d63fc8c0c6cf8e21217aec47b50cf20c4463d29d8d577af4f2d2c20d6c`  
		Last Modified: Thu, 02 Nov 2023 02:04:18 GMT  
		Size: 13.9 MB (13853684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6622038a32074d9fdf984cf9f40c2e278097885a0eaa4437ed8dd03315f55090`  
		Last Modified: Thu, 02 Nov 2023 02:04:17 GMT  
		Size: 4.4 MB (4399275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
