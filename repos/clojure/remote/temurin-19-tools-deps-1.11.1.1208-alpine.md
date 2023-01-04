## `clojure:temurin-19-tools-deps-1.11.1.1208-alpine`

```console
$ docker pull clojure@sha256:031fa624dbb21783662844aaa992f0623f45a2220999ee7f99284a6d554f4bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-19-tools-deps-1.11.1.1208-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:8e7806e7556cfb13585e84adc870dedd09b83ddf5b3942d74cd06a516953848d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243000677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1057f29d32bdeb4c6c782f4e9c3fcf4b2e0cc81c2473229ac01d5e3d2a505dfc`
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
# Tue, 29 Nov 2022 20:23:03 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 29 Nov 2022 20:23:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76cfcdf47cdf24331b51939fd2840fd387cf62471da99e4718e2e42b486a9270';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:23:27 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 29 Nov 2022 20:23:27 GMT
CMD ["jshell"]
# Wed, 04 Jan 2023 19:26:44 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 19:26:44 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:26:50 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 04 Jan 2023 19:26:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:26:50 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 19:26:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 19:26:50 GMT
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
	-	`sha256:eeb257bdcbcd975e9e493219f6dd7220ab6e1c8bcce4128755b8ae59018a8707`  
		Last Modified: Tue, 29 Nov 2022 20:30:53 GMT  
		Size: 200.3 MB (200303543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fef00b4aa6e0e9007248b2d1c189b91d9057213910cc481afd6024e001eaeb9`  
		Last Modified: Tue, 29 Nov 2022 20:30:38 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf68585f1e7554dde55fff7f5497936525775d433b479e3b7ddeadc1d59eaab5`  
		Last Modified: Wed, 04 Jan 2023 19:34:58 GMT  
		Size: 27.3 MB (27305116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f1eb526c4c21b4e8a689416683866d2ec359391112c254421ccfeff1adf615`  
		Last Modified: Wed, 04 Jan 2023 19:34:55 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf69496a71c8c7e31e558d217eeb6fe12467c8fea398cfc72a2ec51670310ee5`  
		Last Modified: Wed, 04 Jan 2023 19:34:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
