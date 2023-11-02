## `clojure:temurin-8-tools-deps-1.11.1.1413-alpine`

```console
$ docker pull clojure@sha256:7d733c0181e2aef9c19771930716bef63a971ad1079aeda0cc445ab5930aa9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-tools-deps-1.11.1.1413-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:efafa4fa253e628e8b9ac8a3bd13143487e0f6f88b7a34ab97224f5bd082a0e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141183778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe1222aca5b072889a10a68de89f817eaee7d82baf289700eb2f332e02ea717`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
# Thu, 02 Nov 2023 01:55:32 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 01:55:32 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:55:37 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 02 Nov 2023 01:55:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 01:55:37 GMT
CMD ["clj"]
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
	-	`sha256:f8f72f037e3b4675e352f1758250aced2cf91f0c3ad4770e4d6e5a826f12839e`  
		Last Modified: Thu, 02 Nov 2023 02:05:36 GMT  
		Size: 27.0 MB (26996082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f370823b7ed6b50f8ba2c0df53b030506ad9c1c264781ee77f3851fc0504fc95`  
		Last Modified: Thu, 02 Nov 2023 02:05:34 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
