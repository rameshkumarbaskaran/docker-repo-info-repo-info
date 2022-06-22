## `clojure:temurin-18-tools-deps-1.11.1.1149-alpine`

```console
$ docker pull clojure@sha256:81a50e17cc0d1268df3b5d03b835372f56271015e21e7a66898874fa6e8c6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-tools-deps-1.11.1.1149-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:59a4192f9fa88d02ace88ba0fd40880e819152415420ff2f2324789739aa95da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226380366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52ac09f473292699d0ea89ca5fd68650fb4a72a01b3df398423d8fb0c2984d`
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
# Tue, 21 Jun 2022 20:23:43 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 21 Jun 2022 20:23:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ab72b28e1ce896e6b11e2b362c12c36007ebe9963d8954bc11e637be1f024dfe';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 21 Jun 2022 20:23:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jun 2022 20:23:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 21 Jun 2022 20:23:58 GMT
CMD ["jshell"]
# Wed, 22 Jun 2022 20:26:48 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Wed, 22 Jun 2022 20:26:48 GMT
WORKDIR /tmp
# Wed, 22 Jun 2022 20:26:55 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 22 Jun 2022 20:26:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Jun 2022 20:26:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Jun 2022 20:26:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Jun 2022 20:26:55 GMT
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
	-	`sha256:4ce063f20f3f48aa654699a8e40506412bceb1e805998d7959dd66d4b521af4b`  
		Last Modified: Tue, 21 Jun 2022 20:28:44 GMT  
		Size: 192.9 MB (192862501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0092728308d3b3e20f1e4fe1a4d2d7df28e4aaf1cf6c3e284e846452de11b684`  
		Last Modified: Tue, 21 Jun 2022 20:28:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457269c2373413f9ceb1b961dd138191185555557af671fc67d65f4d2d760354`  
		Last Modified: Wed, 22 Jun 2022 20:32:37 GMT  
		Size: 30.2 MB (30240034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b58cc8c93183683fca019135de802254f363152c8369028bb2e241e93e1eff`  
		Last Modified: Wed, 22 Jun 2022 20:32:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03a7d12ff3363651caaf568445afa7e4c0247bd465e7a311db1e5c1001ceda`  
		Last Modified: Wed, 22 Jun 2022 20:32:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
