## `clojure:temurin-17-lein-2.10.0-alpine`

```console
$ docker pull clojure@sha256:b09c11eae03eb5cf33bbf7c368f104ca4beba9cf54e607293d8e49f5f011ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-lein-2.10.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:7b0c87d401aac7bbb35f8e714b5b32e8f2e7c55cf3f7b3c8bd6e6da544afed8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172734397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab71be687efd8aefa138e19614980c353b2da3b9eb3890bb02570ead369ef73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 19:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 19:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 19:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Aug 2023 18:09:08 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 14 Aug 2023 18:10:34 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Mon, 14 Aug 2023 18:10:44 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='90eb413eeed9cc2813f7d66d348c35475148c0cdc41c8f9ef2f26d51078e287e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 14 Aug 2023 18:10:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:10:47 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:10:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 18:10:47 GMT
CMD ["jshell"]
# Mon, 14 Aug 2023 20:10:24 GMT
ENV LEIN_VERSION=2.10.0
# Mon, 14 Aug 2023 20:10:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 14 Aug 2023 20:10:24 GMT
WORKDIR /tmp
# Mon, 14 Aug 2023 20:10:33 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Mon, 14 Aug 2023 20:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Aug 2023 20:10:33 GMT
ENV LEIN_ROOT=1
# Mon, 14 Aug 2023 20:10:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Mon, 14 Aug 2023 20:10:35 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Mon, 14 Aug 2023 20:10:36 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Aug 2023 20:10:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994e83f716a0db024fb37caf707eae5af27172a0fffb691c6e7b53bb7fc5b3ab`  
		Last Modified: Mon, 14 Aug 2023 18:13:07 GMT  
		Size: 9.3 MB (9276497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dcebe8dfc82ba6d7ef1c3aba301f87bfcf69a05c6e9fcc26d2b3725d82d1f7`  
		Last Modified: Mon, 14 Aug 2023 18:16:48 GMT  
		Size: 144.1 MB (144105063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920d29c34aa30c6d8a6a682852c76d9ea24a83c8bab5c459a908997c84c6f60a`  
		Last Modified: Mon, 14 Aug 2023 18:16:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6024980cb8b498b9a2ef4e378a9cfe55c4dbd7a0f6c623e73c5fb8dfab5b394b`  
		Last Modified: Mon, 14 Aug 2023 18:16:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e09ff25e327b558c6e5b14484c4ee4297072fd217e9d2f84f8ef61dcd011975`  
		Last Modified: Mon, 14 Aug 2023 20:19:51 GMT  
		Size: 11.6 MB (11550664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f31bbcac6a17cd0d8d815cf53421172f559c99eac861b21cde5e2d805e802f`  
		Last Modified: Mon, 14 Aug 2023 20:19:50 GMT  
		Size: 4.4 MB (4399244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19643b18b76d305039adf0692968ad524951a348908025006308a7c0d041a913`  
		Last Modified: Mon, 14 Aug 2023 20:19:50 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
