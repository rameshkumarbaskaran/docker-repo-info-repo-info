## `clojure:temurin-19-tools-deps`

```console
$ docker pull clojure@sha256:60dac38b313049a28e26e9c8883d25fea9c6d1303bc02d861651889b4adc0795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:e8eaa7bc37b7e347d8685f735f1ab3023f56af1575fb33d076744523633075aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302688402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc42689ada68abd20a2655c4231525dabff8290432def368ce3b7acaebf1b1d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:46:23 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 02 Nov 2022 18:46:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 18:46:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 18:46:40 GMT
CMD ["jshell"]
# Wed, 02 Nov 2022 20:19:49 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:19:50 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:20:03 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:20:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:20:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:20:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:20:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fa72e018dd1c616d4bdb23d6fbb735820db9a943b470a787973556d4ee24e`  
		Last Modified: Wed, 02 Nov 2022 18:50:22 GMT  
		Size: 17.0 MB (16986189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be68af618289efb6a189cb5adf042aeb201cc90dc568832de1d22bf09c28239`  
		Last Modified: Wed, 02 Nov 2022 18:51:22 GMT  
		Size: 200.9 MB (200852998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe61642fd50a00b1e64bb99d83f68065ea661478fb56e5b682b868401aeda8`  
		Last Modified: Wed, 02 Nov 2022 18:51:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8776dcca8c6caf3cfaf2072f77aea5a8c88bf1282403ccd184ffa2d52807b48c`  
		Last Modified: Wed, 02 Nov 2022 20:31:28 GMT  
		Size: 54.4 MB (54422413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad6c9997633c9d5f6b6c4614b5352a94d79401598f914ed5a326f8d49a8bce9`  
		Last Modified: Wed, 02 Nov 2022 20:31:21 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18953e5b0047daaabfbe159109597d2820126e7222ce1d57eaf736205db2a347`  
		Last Modified: Wed, 02 Nov 2022 20:31:21 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e922e04749905b30c3a31214fd160181fa97bddd8335f4d5da87c95da66bdc3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300775830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4296a5973c21b262a7aeceaf029ac4f574528c9d9389ab39a991af5dda76df9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:45:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:46:27 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 02 Nov 2022 19:46:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 19:46:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 19:46:44 GMT
CMD ["jshell"]
# Wed, 02 Nov 2022 20:54:13 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:54:13 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:54:24 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:54:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:54:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:54:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:54:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8d9c230ad7b20621780183623ce76b7c296e1db90d16a51deeb03f19e2493c`  
		Last Modified: Wed, 02 Nov 2022 19:49:51 GMT  
		Size: 18.4 MB (18416178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad0c2cd6437a19e827e089c26dc673cb9b759584447394ca75a59d7262cbbc`  
		Last Modified: Wed, 02 Nov 2022 19:50:48 GMT  
		Size: 199.6 MB (199589982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7bc6d25e82c611ff8eda9d3d6ce3092c1680a8f792973b0f5a9b5d1775da39`  
		Last Modified: Wed, 02 Nov 2022 19:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64daed00f85b8ba5344909d178b9491999c53865e0efa806c53fff739ea1d90b`  
		Last Modified: Wed, 02 Nov 2022 21:05:07 GMT  
		Size: 54.4 MB (54386325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616090b076640cb1a518fa6847db41e387e4d5de7709670896b6c842deeda83`  
		Last Modified: Wed, 02 Nov 2022 21:05:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b689dfa47e5682b99d3323da0c88035e076b9c6bb87fed86c79746494ad31490`  
		Last Modified: Wed, 02 Nov 2022 21:05:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
