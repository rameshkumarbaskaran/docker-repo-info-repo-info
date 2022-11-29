## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:1d62faf876f3ff84f131c4f9ede0974e4753666c5efc151e1456ea6f6c075e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e742eee4037b842d1b2049cb994b4972159ea840f45054bda029a4094cca40ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57159082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c8cb26605c3c01b22ed309b944ac0d48ed01ffa1c10bb97152f0e711c967b5`
-	Default Command: `["\/bin\/sh"]`

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
# Tue, 29 Nov 2022 20:19:50 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 29 Nov 2022 20:20:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f4a4a3c092d8cca171fc36003ac82e2f3d8d768bd6f530a20e2a4caf79bdb9e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:20:40 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:331e6c1bb9983c62f745ed6bcc264a9ed8610ea5d8b31a1f235b04ded14aa4b7`  
		Last Modified: Tue, 29 Nov 2022 20:27:04 GMT  
		Size: 41.8 MB (41768111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070739a0415b3b38b7395424bebff29a1243c2b0b2c289db5ab17f0453cbec99`  
		Last Modified: Tue, 29 Nov 2022 20:26:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
