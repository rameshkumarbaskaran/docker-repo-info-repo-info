## `clojure:temurin-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:7b22137d9e6bf4c828bbebb60af5fc3350acf52e14d89ea3e182a337eaf80ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:80de7a955558981cf8a91d213252d16ca68a152774de04bf001c9bd94f15a1a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225327094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3d346a7658738b6c47a6d7a88847c140b83e31cee7b8c03bf5ad6a812cca46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 21 Jun 2022 20:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jun 2022 20:21:36 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 21 Jun 2022 20:22:54 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 21 Jun 2022 20:23:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5cbaece6aec44f6d3911cfa3c5a8659889e85042aff214c944c5fa1b5938a5fc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 21 Jun 2022 20:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jun 2022 20:23:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 21 Jun 2022 20:23:19 GMT
CMD ["jshell"]
# Wed, 22 Jun 2022 20:26:06 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Wed, 22 Jun 2022 20:26:06 GMT
WORKDIR /tmp
# Wed, 22 Jun 2022 20:26:12 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 22 Jun 2022 20:26:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Jun 2022 20:26:12 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Jun 2022 20:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Jun 2022 20:26:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4177d2591259bff2bae6f43f12721dbe4ed5aac24fb0991377a3d27cdd534e`  
		Last Modified: Tue, 21 Jun 2022 20:26:07 GMT  
		Size: 477.8 KB (477755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192e69d5289dec2e5bbf3ed1456166acafdc67b3e657981604fa21df9ae64084`  
		Last Modified: Tue, 21 Jun 2022 20:27:54 GMT  
		Size: 191.8 MB (191809195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbdc495bee83415cd6c7ddec5b7a12d388962b684278496d8d5798a5a13cd90`  
		Last Modified: Tue, 21 Jun 2022 20:27:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8887e430f3e7b22de46e4b10e5b30561148bff9604044894467257fd38db17`  
		Last Modified: Wed, 22 Jun 2022 20:31:48 GMT  
		Size: 30.2 MB (30240066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e95c82a2562f95a8b569167629a1d53d22e8410b239830ac917ba2f515dfd39`  
		Last Modified: Wed, 22 Jun 2022 20:31:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76592961a53a15bb20f0715bf65142513b0bd1a31082e6464db38bd0540de2c`  
		Last Modified: Wed, 22 Jun 2022 20:31:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
