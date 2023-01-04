## `clojure:latest`

```console
$ docker pull clojure@sha256:e6e88e5c70c4711227bfe9777a6d5c94c4b6aed4950e8835338af52092125909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:79ddc924550e8926e166210214630eecc643bf36e3a2cbd29de68e380093ef30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365352252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142d27b9a2a8139d57649bf2e40eaa1a250e3fd39bd1c292ecca94caf7151b91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:45:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:45:54 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 01:46:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='e7c81596f67b6325036e9182d012f2266ced5663c5d4b0de0540ce62dcc67718';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 01:46:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 01:46:05 GMT
CMD ["jshell"]
# Fri, 09 Dec 2022 06:31:57 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 09 Dec 2022 06:31:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 09 Dec 2022 06:31:57 GMT
WORKDIR /tmp
# Fri, 09 Dec 2022 06:32:03 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 09 Dec 2022 06:32:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 09 Dec 2022 06:32:04 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 09 Dec 2022 06:32:23 GMT
RUN boot
# Wed, 04 Jan 2023 19:20:01 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 04 Jan 2023 19:20:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 04 Jan 2023 19:20:01 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:20:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 04 Jan 2023 19:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Wed, 04 Jan 2023 19:20:36 GMT
ENV LEIN_ROOT=1
# Wed, 04 Jan 2023 19:20:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 04 Jan 2023 19:20:40 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 19:20:40 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:21:13 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 04 Jan 2023 19:21:13 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:21:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 19:21:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 19:21:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8d923227d8dc300e1ddab1b65c83c0eff7f4a7105d958420872f7138b79735`  
		Last Modified: Fri, 09 Dec 2022 01:52:47 GMT  
		Size: 17.0 MB (16973851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda8241fd25fe52c584da502f21cef5b5067551f7bcfcca58e9a630238f7f558`  
		Last Modified: Fri, 09 Dec 2022 01:52:59 GMT  
		Size: 192.4 MB (192440274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dccabde73de58115ed8db691bd335b82d91b6961c0d1af77691b368b0a8253`  
		Last Modified: Fri, 09 Dec 2022 01:52:45 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148121fc704bb9099b79e763a806168b49359b573b00459f771f2c7ca8b0dd11`  
		Last Modified: Fri, 09 Dec 2022 06:51:20 GMT  
		Size: 338.6 KB (338641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c92aad1413a44259eaba0c2f8362eb7028955fd0469fc64329319f485b23a1`  
		Last Modified: Fri, 09 Dec 2022 06:51:23 GMT  
		Size: 58.8 MB (58820443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9049d5bc225e0964b08b809077d76bffc618aa8901506d0487748b4cf6877d27`  
		Last Modified: Wed, 04 Jan 2023 19:30:37 GMT  
		Size: 12.0 MB (11973921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbfb0ab67b53e5a3339880b124caaa17faffa923e8ac614fbc32cff2c344c10`  
		Last Modified: Wed, 04 Jan 2023 19:30:37 GMT  
		Size: 4.4 MB (4399408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbc97af7c66a505943902dcb3a7b07f96d3d285559a5cc68ee774424443d486`  
		Last Modified: Wed, 04 Jan 2023 19:30:43 GMT  
		Size: 50.0 MB (49975809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe09c129251f7267571b536ce08fc309ed850b07222a84420289cfdcc8cf076f`  
		Last Modified: Wed, 04 Jan 2023 19:30:36 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b792475b042f7209c1a45cd2bb0a1ff6d6d89bf44dadcd100cc52e26a9151a`  
		Last Modified: Wed, 04 Jan 2023 19:30:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31124fe3abe6c44425d20908216ff0062902c04ab1c8341c0a6434b32070e557
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.5 MB (363474386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7beb0bad5b51144c00b544a57a6d1a36bfed078c5c672e1d4054973e2cf32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:57 GMT
ADD file:429a55a11d4bcd15647d1316d9debd9ead4b4ab5c0b9146894d07c39aa814290 in / 
# Fri, 09 Dec 2022 01:46:57 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:39:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:39:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:39:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:42:00 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:42:00 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 03:42:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='e7c81596f67b6325036e9182d012f2266ced5663c5d4b0de0540ce62dcc67718';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 03:42:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 03:42:10 GMT
CMD ["jshell"]
# Fri, 09 Dec 2022 05:00:18 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 09 Dec 2022 05:00:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 09 Dec 2022 05:00:18 GMT
WORKDIR /tmp
# Fri, 09 Dec 2022 05:00:23 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 09 Dec 2022 05:00:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 09 Dec 2022 05:00:23 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 09 Dec 2022 05:00:42 GMT
RUN boot
# Wed, 04 Jan 2023 18:39:40 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 04 Jan 2023 18:39:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 04 Jan 2023 18:39:40 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:40:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 04 Jan 2023 18:40:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Wed, 04 Jan 2023 18:40:22 GMT
ENV LEIN_ROOT=1
# Wed, 04 Jan 2023 18:40:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 04 Jan 2023 18:40:26 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 18:40:26 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:41:02 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 04 Jan 2023 18:41:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 18:41:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 18:41:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 18:41:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10175de2f0c4f7d306f660ee073bce12b824c8012dd19b3c140aae053fabd1cc`  
		Last Modified: Thu, 08 Dec 2022 18:50:01 GMT  
		Size: 28.4 MB (28384475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f2e5e37e706412c1481b71d2240df4fe659ef83ae4d2932a8ddfe42b0d3d20`  
		Last Modified: Fri, 09 Dec 2022 03:48:04 GMT  
		Size: 18.4 MB (18400373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8f048f32cc8c2c10e668e5de4da2c2fb6f21410107ed5a233a7c25cc6994ed`  
		Last Modified: Fri, 09 Dec 2022 03:48:14 GMT  
		Size: 191.2 MB (191223696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3effab4d2ab2ce23b6966dd48f71c31d3bb34d4a41170bdbff42e9ce9b49bc4`  
		Last Modified: Fri, 09 Dec 2022 03:48:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a488f94fa54978f2b3733169c60f61c0ff2007a8a29a0a0f98bcf9b98a0d78fd`  
		Last Modified: Fri, 09 Dec 2022 05:16:21 GMT  
		Size: 340.0 KB (339979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0338614401f6796095723b0a7adea160b41de7e86cbb164525648c99996181`  
		Last Modified: Fri, 09 Dec 2022 05:16:23 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aeae89d0e9a4c06526f72be7730424087b03f1cf5f3345a0fea1badbe30572`  
		Last Modified: Wed, 04 Jan 2023 18:48:58 GMT  
		Size: 12.0 MB (11973828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088900267f41091ea1d7ee3aab9523b40a73045622902bcfe59a9a9815c79eb9`  
		Last Modified: Wed, 04 Jan 2023 18:48:57 GMT  
		Size: 4.4 MB (4399440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3d7751c38d80e904dc6b1cabe49a3bca00ee61ecffdb5702f645af9c73cb5`  
		Last Modified: Wed, 04 Jan 2023 18:49:03 GMT  
		Size: 49.9 MB (49930932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c532fe94bce9b64f265c4df25f42c66e14b89f2d9111cc6a3432d46cd3c0307`  
		Last Modified: Wed, 04 Jan 2023 18:48:57 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7d85e8e149ea90afda873f926d0a63992c8b33f9dcc5222dc58d1ddba0eb8e`  
		Last Modified: Wed, 04 Jan 2023 18:48:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
