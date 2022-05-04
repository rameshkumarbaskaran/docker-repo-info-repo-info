## `clojure:boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:dc455079ce8f94b5a36d36f42af2255e7dd0e2604f1a2981597e9340b32fdcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:645cc4265f1425975f75cd679cd2f680b8136a8bf7f14ee0791464f783b2146e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254725445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32c155db02901ffd3b105c8ee1797c45ba8f57c90376fa8b2e6bd611a4f2b26`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:55:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 10:55:44 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Wed, 27 Apr 2022 18:21:21 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 27 Apr 2022 18:21:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5cbaece6aec44f6d3911cfa3c5a8659889e85042aff214c944c5fa1b5938a5fc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Apr 2022 18:21:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 18:21:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:21:39 GMT
CMD ["jshell"]
# Wed, 04 May 2022 18:44:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 04 May 2022 18:44:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 04 May 2022 18:44:53 GMT
WORKDIR /tmp
# Wed, 04 May 2022 18:44:55 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 04 May 2022 18:44:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 04 May 2022 18:44:55 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 04 May 2022 18:45:44 GMT
RUN boot
# Wed, 04 May 2022 18:45:44 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 04 May 2022 18:45:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 May 2022 18:45:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3277e9a7631c57d573722746688faad867a5b43dda77316e369e08ba94b713d`  
		Last Modified: Tue, 05 Apr 2022 10:59:33 GMT  
		Size: 430.5 KB (430455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f2c97071093dd704b77dd1cbdca2551f0a13717597393d821bb8be2ea237ae`  
		Last Modified: Wed, 27 Apr 2022 18:26:33 GMT  
		Size: 191.8 MB (191809196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28060bb0256d21647977bfabfba0e316b3bd27e40a6e549ac2b825bb11610312`  
		Last Modified: Wed, 27 Apr 2022 18:26:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacacb7608e0270001cd3ffba65cd0ada1bc6f823d73fba280dd0287f100cbb6`  
		Last Modified: Wed, 04 May 2022 18:51:04 GMT  
		Size: 849.6 KB (849618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c4f1c67d6c47b4799c575e89b7282ca47af94afec823cdde9020e4f8a0cd93`  
		Last Modified: Wed, 04 May 2022 18:51:07 GMT  
		Size: 58.8 MB (58821052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e552cf2ea0e253a1a14db96c6be81241c512f20824efce1d023ea36cb951670`  
		Last Modified: Wed, 04 May 2022 18:51:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
