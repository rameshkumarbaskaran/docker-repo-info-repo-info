## `clojure:temurin-21-lein-alpine`

```console
$ docker pull clojure@sha256:dea96e620804afad0ad00b3abf8bc029fb45d43ba56757048e74ce11e6849ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-21-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:012be47a0d98b819c6728c3598e90666baa748cf441bf9d85564451f899be2c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186259673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd705c8142a040fc1ec6c97ba6de563e9dc2a77051f70692969f58bf31c9d675`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Thu, 19 Oct 2023 02:50:17 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 19 Oct 2023 02:53:10 GMT
ENV JAVA_VERSION=jdk-21+35
# Thu, 19 Oct 2023 02:53:22 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3f8e5b0447d2dd711f12edda611ed1cf9aab4ca53c8fe32fca8fb1e6fee41c12';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21_35.tar.gz';          ;;        amd64|x86_64)          ESUM='4fd74f93f0b1a94d8471e0ed801fe9d938f7471f6efe8791880c85e7716c943f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:53:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:53:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:53:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 02:53:24 GMT
CMD ["jshell"]
# Thu, 19 Oct 2023 07:09:21 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 19 Oct 2023 07:09:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 19 Oct 2023 07:09:21 GMT
WORKDIR /tmp
# Thu, 19 Oct 2023 07:09:28 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 19 Oct 2023 07:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Oct 2023 07:09:29 GMT
ENV LEIN_ROOT=1
# Thu, 19 Oct 2023 07:09:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 19 Oct 2023 07:09:32 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 19 Oct 2023 07:09:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 19 Oct 2023 07:09:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42efc8ffaa989c4197765e315c7d229fc40528c139b6be6a50e459fab1b640e`  
		Last Modified: Thu, 19 Oct 2023 02:55:23 GMT  
		Size: 9.3 MB (9276490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf76d6f40cd7ca863a644a0ca98e4600f322786a73de7a9bf1c175d6d95785b2`  
		Last Modified: Thu, 19 Oct 2023 02:59:40 GMT  
		Size: 157.6 MB (157630052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c035f235584ff3c6cb322faae306b071925722bfb8f2748f8ce3aaa2919be110`  
		Last Modified: Thu, 19 Oct 2023 02:59:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0f3b1ff9d2c30fd49b405bac85864ddd3cac27c25cd99c361aa77fb8a13466`  
		Last Modified: Thu, 19 Oct 2023 02:59:26 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b33e65b4929d2c6658b27c6226c1e54229a4381e6c12c96c81b510a7f2b670f`  
		Last Modified: Thu, 19 Oct 2023 07:14:24 GMT  
		Size: 11.6 MB (11550644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dbfdb353256d2938fff7df965b5a216cffebde6ad689dcd8db7e79ebfd689`  
		Last Modified: Thu, 19 Oct 2023 07:14:22 GMT  
		Size: 4.4 MB (4399205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e91a956894a5ae385edaa136805f68871567d71676946273b8636c5a7e137c4`  
		Last Modified: Thu, 19 Oct 2023 07:14:22 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
