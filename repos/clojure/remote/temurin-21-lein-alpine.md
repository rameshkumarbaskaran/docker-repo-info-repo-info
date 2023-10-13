## `clojure:temurin-21-lein-alpine`

```console
$ docker pull clojure@sha256:4ddd047b02fbbefa7269436154dbded24b533be5c678701fa5de367437b67df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-21-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:070acda921a5394f408bbf2835f2f49efe1bd8228d90ac9c26328d44c365ddd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186259706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa70d5f448ecc9008fa548b20315822ead668ff00a4e8b0000ca36a45837169`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Sep 2023 23:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 23:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Sep 2023 23:24:25 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 11 Oct 2023 18:09:20 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 18:09:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3f8e5b0447d2dd711f12edda611ed1cf9aab4ca53c8fe32fca8fb1e6fee41c12';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21_35.tar.gz';          ;;        amd64|x86_64)          ESUM='4fd74f93f0b1a94d8471e0ed801fe9d938f7471f6efe8791880c85e7716c943f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 11 Oct 2023 18:09:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 18:09:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 11 Oct 2023 18:09:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Oct 2023 18:09:33 GMT
CMD ["jshell"]
# Fri, 13 Oct 2023 01:37:11 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:37:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:37:11 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:37:18 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Fri, 13 Oct 2023 01:37:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:37:18 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:37:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:37:22 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:37:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:37:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4092d737c5d0c601ddadd8d075b756e55cc717065ae83683571965c2117a9`  
		Last Modified: Thu, 28 Sep 2023 23:28:20 GMT  
		Size: 9.3 MB (9276514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15de4e91b4ea2bb2143d98dec470476fe69008037a626991da945af66ff8b9`  
		Last Modified: Wed, 11 Oct 2023 18:12:45 GMT  
		Size: 157.6 MB (157630049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57006341305b6b066a0078ba7cc1b938820d7008118025c4873bfd0efac05c23`  
		Last Modified: Wed, 11 Oct 2023 18:12:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0f8d9e2d3f3ae2db5bd1c8a0c85b7b197dc7ab45c6a2797eebc228fe69a3f`  
		Last Modified: Wed, 11 Oct 2023 18:12:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c656a4cc3cb2cdf02578551e00a70e1cc76be0b15358b9bd293b271df28e70ae`  
		Last Modified: Fri, 13 Oct 2023 01:50:07 GMT  
		Size: 11.6 MB (11550649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a27ecccb100c783d1dcde80c9b0197849fd9c3517ea17d1252ed3daaadbb34`  
		Last Modified: Fri, 13 Oct 2023 01:50:06 GMT  
		Size: 4.4 MB (4399209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb5395604e2b9f66f989015d2ec4823c1505d2a268bf9f38fd1d8a92230a35`  
		Last Modified: Fri, 13 Oct 2023 01:50:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
