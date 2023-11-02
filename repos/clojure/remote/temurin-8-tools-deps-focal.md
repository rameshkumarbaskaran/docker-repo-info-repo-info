## `clojure:temurin-8-tools-deps-focal`

```console
$ docker pull clojure@sha256:cb47d0e9b9ffd1ffef10742b36e2ac721d587915cc156a1e801f884b6a7d72af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-focal` - linux; amd64

```console
$ docker pull clojure@sha256:83d318947487bf1c306919b0e2d6fbd35d86508f981f87a62dc582217c608347
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212287129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f240bf3b0e6dfba78af17889c504f57155791672631c93e30b8a0ca6f682b107`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:50:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:50:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:50:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:23:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 01:11:10 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 02 Nov 2023 01:11:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='9e574cff0b8dba29930e38eeec4cb4350a77a56a27d03fa316fa6b2383eeef9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Nov 2023 01:11:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 02 Nov 2023 01:11:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 02 Nov 2023 01:11:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 Nov 2023 01:57:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 01:57:19 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:57:54 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 01:57:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 01:57:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa209e79be14e7f0a79b6018ffeb98dfc7ace47267179474d49f3f047b1552e`  
		Last Modified: Mon, 30 Oct 2023 23:32:31 GMT  
		Size: 16.9 MB (16919533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0b4e468a39325a6d99749259c34c536e8b8496b4dee2000ab93d8ed9f8031`  
		Last Modified: Thu, 02 Nov 2023 01:15:07 GMT  
		Size: 103.6 MB (103597480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ecb78fcd9f3ce161c70e58c1af1052a1d2f0b42c6465938be5b82458ce7a5`  
		Last Modified: Thu, 02 Nov 2023 01:14:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc94b2148e8d5e1e692cee1f915b5a580f4db215031881ca0755958089644d7`  
		Last Modified: Thu, 02 Nov 2023 01:14:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a1ccc5d84ee2c7a446966a8a8900451ee6b173de27d0d2c1baf65fbeadadd0`  
		Last Modified: Thu, 02 Nov 2023 02:07:18 GMT  
		Size: 63.2 MB (63187911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16afea1700a2c4cc0bd55328850a23b110aca5e364993a3c728695b5b492c8db`  
		Last Modified: Thu, 02 Nov 2023 02:07:11 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b33f4bdbb3bc9c8286198824eefc4f9ebec9191075bf55c3afd78c2d28188565
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210008090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc91ea3b92ada92bfe861faaf67b688761ae86aaa4e0a4e5965e5c68559db6f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:40:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 01:37:02 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 02 Nov 2023 01:37:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='9e574cff0b8dba29930e38eeec4cb4350a77a56a27d03fa316fa6b2383eeef9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 02 Nov 2023 01:37:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 02 Nov 2023 01:37:09 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 02 Nov 2023 01:37:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 Nov 2023 03:34:21 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 03:34:21 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:34:42 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 03:34:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 03:34:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2717b88e02799c1309e24243b581cd227d05944a061c0c57d1cac69369a47533`  
		Last Modified: Mon, 30 Oct 2023 23:48:05 GMT  
		Size: 16.8 MB (16768205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9230c133032cdba3e025da7552e52b96a4a66440a6857811dec47f8fefcd13fb`  
		Last Modified: Thu, 02 Nov 2023 01:39:45 GMT  
		Size: 102.7 MB (102707036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fbe668e143ba26fe901c3be5f730c439e2ef59ba1f1cd3d8715b97acd1d860`  
		Last Modified: Thu, 02 Nov 2023 01:39:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cde7e1a52dcb7c3cbbd573f44bd0d7ed4aed234fd29b7567176954412b43b5`  
		Last Modified: Thu, 02 Nov 2023 01:39:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff689979ae7c104def0f749702369de3e2c6c3a7f380cf2b02f3af1974bf5c`  
		Last Modified: Thu, 02 Nov 2023 03:41:59 GMT  
		Size: 63.3 MB (63331825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bb1059c424fa9bfc70338cc268594768fd28e904472e826aaec1fd37a80f66`  
		Last Modified: Thu, 02 Nov 2023 03:41:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
