## `clojure:temurin-18-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:4e3d71a93e7fe64b6e1b36c765e7d295c033e8da25737f82392d6df8341230ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b45e0c40eb718abf520efc669839c0204737a3d6c1347842d7e7dde5ad3a7a81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255778298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007b7b99b5fff508de051e403d9f7455813c6dacf6b80c9039aa6042fa1b423`
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
# Wed, 04 May 2022 18:21:40 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Wed, 04 May 2022 18:21:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ab72b28e1ce896e6b11e2b362c12c36007ebe9963d8954bc11e637be1f024dfe';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 04 May 2022 18:21:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 May 2022 18:21:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 04 May 2022 18:21:56 GMT
CMD ["jshell"]
# Wed, 04 May 2022 18:46:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 04 May 2022 18:46:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 04 May 2022 18:46:52 GMT
WORKDIR /tmp
# Wed, 04 May 2022 18:46:53 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 04 May 2022 18:46:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 04 May 2022 18:46:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 04 May 2022 18:47:20 GMT
RUN boot
# Wed, 04 May 2022 18:47:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 04 May 2022 18:47:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 May 2022 18:47:20 GMT
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
	-	`sha256:591c4b43fb353060ea281fcc411207e2b4b9fa7dd3d86f30a00f135509dc4e4c`  
		Last Modified: Wed, 04 May 2022 18:24:33 GMT  
		Size: 192.9 MB (192862515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b9bbec352ef122ab09d03fbcfaaf8423125a8ab33824f274c08c1697d665bb`  
		Last Modified: Wed, 04 May 2022 18:24:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3da12c981d32593f8b30d218797adb8bbca4b21bfa9ff141d7ef6355b8b81a`  
		Last Modified: Wed, 04 May 2022 18:52:57 GMT  
		Size: 849.6 KB (849625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487e406083d2b084ea1ac904baab0f1245f16ca5628d115a7a16d3a5060b8523`  
		Last Modified: Wed, 04 May 2022 18:53:00 GMT  
		Size: 58.8 MB (58820583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0f654837275c2a35504bbdb7edc4193b7fb9ed7d4212e6bf40321feff49be`  
		Last Modified: Wed, 04 May 2022 18:52:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
