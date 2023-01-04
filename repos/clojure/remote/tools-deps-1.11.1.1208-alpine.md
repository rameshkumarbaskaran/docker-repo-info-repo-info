## `clojure:tools-deps-1.11.1.1208-alpine`

```console
$ docker pull clojure@sha256:e7b41fb0312474c5de1491da89b7688585d32853ebcab8729b9aa220713e7df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:tools-deps-1.11.1.1208-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:690b82b988dbdf04acf371d3562d8fe619c157d709443b0cb0ab4dcec63a24f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234434299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77224ac42a5dbd48f3532b60fa219357662c8945c1e1351f061aaf139d9b93d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 20:19:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Nov 2022 20:19:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:19:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Nov 2022 20:19:50 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 29 Nov 2022 20:21:56 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Tue, 29 Nov 2022 20:22:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='cb154396ff3bfb6a9082e3640c564643d31ecae1792fab0956149ed5258ad84b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:22:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 29 Nov 2022 20:22:17 GMT
CMD ["jshell"]
# Wed, 04 Jan 2023 19:25:28 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 19:25:28 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:25:34 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 04 Jan 2023 19:25:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:25:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 19:25:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 19:25:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e5acd5897d762b9a83758d4ceae374df7b8b0367a48cc14b8a00e33998b3bf`  
		Last Modified: Tue, 29 Nov 2022 20:26:18 GMT  
		Size: 12.0 MB (12020105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bcc6f5e5f8e69448effa45d4b03eac01070f88ec1d9ae7cab0af6c8dde9849`  
		Last Modified: Tue, 29 Nov 2022 20:29:25 GMT  
		Size: 191.7 MB (191737165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358f8ac5ae5526207bb9c8ebbdd5433407beca88514dd520906468e70c8a83b6`  
		Last Modified: Tue, 29 Nov 2022 20:29:11 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e92d767707e56481e8d65a5155dd5552ebe5886f0bf9602cc3d132c8a9e48`  
		Last Modified: Wed, 04 Jan 2023 19:33:43 GMT  
		Size: 27.3 MB (27305115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65382689570a41327986e8332798023511df0ce2d4e3f4b3c37ca815b1368ac`  
		Last Modified: Wed, 04 Jan 2023 19:33:31 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cdd8519c263f87761f6ea7f3edfa3717930d159b4e8a05679766fa5943911c`  
		Last Modified: Wed, 04 Jan 2023 19:33:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
