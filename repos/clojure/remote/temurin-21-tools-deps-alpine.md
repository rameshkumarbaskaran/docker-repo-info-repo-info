## `clojure:temurin-21-tools-deps-alpine`

```console
$ docker pull clojure@sha256:6ca15dae3937dcc3be55d87df8d1b21941ba9d7538e84adce4577c9f886fa766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-21-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:f25d45be2a8bf4d65a591accc9096a8a3eb96e7e69a6badf845b46a8462f0688
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197306563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c024dff9a5092263b21da95bd5d36575b00762af4b0c6f03b114c49631442f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Fri, 13 Oct 2023 01:39:15 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:39:15 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:39:20 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 13 Oct 2023 01:39:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:39:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:39:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:39:21 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:bdb4247ba4e0d2d947a4801bff8f6533e1ad8d7d1c2d8353947e8e9921654f72`  
		Last Modified: Fri, 13 Oct 2023 01:52:10 GMT  
		Size: 27.0 MB (26996093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20cf45c8b17fc48c85142b40d9249b0914f8ca71036766d44a0e7a6f6cc70b`  
		Last Modified: Fri, 13 Oct 2023 01:52:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c5b8922cc40224742db6fccee4674d6509c7b79c27b40d3c7fb40199d7528d`  
		Last Modified: Fri, 13 Oct 2023 01:52:07 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
