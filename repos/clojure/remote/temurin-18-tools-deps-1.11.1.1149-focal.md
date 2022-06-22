## `clojure:temurin-18-tools-deps-1.11.1.1149-focal`

```console
$ docker pull clojure@sha256:1b196808e37edf8b40518ee48ee581805851d79179970e6d343bfbc05bf93162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-tools-deps-1.11.1.1149-focal` - linux; amd64

```console
$ docker pull clojure@sha256:49c50912058851e6af0bd12d6ff1899274a1c4d1ef911fa78b740c10a1f1a9f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304648744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3b263db8f54db2c91b6dc59b7972ff2a187387f1fb9a74b80405caeb9f61d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:16:35 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 00:16:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:16:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:16:49 GMT
CMD ["jshell"]
# Wed, 22 Jun 2022 20:26:58 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Wed, 22 Jun 2022 20:26:58 GMT
WORKDIR /tmp
# Wed, 22 Jun 2022 20:27:14 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 22 Jun 2022 20:27:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Jun 2022 20:27:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Jun 2022 20:27:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Jun 2022 20:27:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32598539a8f0b55be77078c6637866fc4128a4213ea59e9993662a310a2b711`  
		Last Modified: Tue, 07 Jun 2022 00:22:05 GMT  
		Size: 19.8 MB (19773881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab1e3bdf3dcc14af31e9535f736da5c91bb9add2ad5a162cd3e86d867ab634a`  
		Last Modified: Tue, 07 Jun 2022 00:23:46 GMT  
		Size: 193.5 MB (193544180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59651909abe6d6a31a9aa05a896765e01e80010d983522cbbce07891da8c499f`  
		Last Modified: Tue, 07 Jun 2022 00:23:32 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a502c7e012a2d13b9622ea795f59d1744e09e56a70a52503d93f0816565a15a`  
		Last Modified: Wed, 22 Jun 2022 20:32:58 GMT  
		Size: 62.8 MB (62756867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef5f29e611e900aa540a73426b48be139e4604e9ed0d1adf91f8dbbfeb367b9`  
		Last Modified: Wed, 22 Jun 2022 20:32:50 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f7dfb22551ae2c6f1863d652c376d58b91f87ba9acc071ede1730105918bc7`  
		Last Modified: Wed, 22 Jun 2022 20:32:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-tools-deps-1.11.1.1149-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfca0e9dd67a59d7b431d96d6baf2aadd335de8d5975e2848728449670d95605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302712889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b72e91faca6a6086ee8099c845a9c58b00a358cdd0f789a70f6b80288daca1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:06:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:38:11 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 07 Jun 2022 06:38:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37ceaf232a85cce46bcccfd71839854e8b14bf3160e7ef72a676b9cae45ee8af';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='0ddec3c165ab0b662a57a845db3fdaeb840660b493f164696b03df76aadf61c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_arm_linux_hotspot_18.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7c3376b4eb14a58d27816776e965f1b214c17c4c2e918dc9e996a0f30e76550e';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='236dc78e698c21f258078661ab5c74b8cc7d38a1febb7aa7a6598bd3b999c0dc';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='16b1d9d75f22c157af04a1fd9c664324c7f4b5163c022b382a2f2e8897c1b0a2';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:38:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:38:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:38:34 GMT
CMD ["jshell"]
# Wed, 22 Jun 2022 19:46:15 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Wed, 22 Jun 2022 19:46:15 GMT
WORKDIR /tmp
# Wed, 22 Jun 2022 19:46:35 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Wed, 22 Jun 2022 19:46:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Jun 2022 19:46:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Jun 2022 19:46:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Jun 2022 19:46:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e4a04805fb472806936ea1417715c9eeb219259a6a6fc44afc367c1d8c5b69`  
		Last Modified: Tue, 07 Jun 2022 05:12:45 GMT  
		Size: 20.5 MB (20500981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3d4679a6436fe2be8e2bda89d2d54beb2fecd90141b4b8ede039b1d5f3eb58`  
		Last Modified: Tue, 07 Jun 2022 06:46:45 GMT  
		Size: 192.4 MB (192377859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba499b2f2a5aac9a2ce65281d0a813ac33150364d7c9a3cd77bcc0bd09d525d`  
		Last Modified: Tue, 07 Jun 2022 06:46:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1f3f91e3a236735c861f7d6115867f0718c4b42a877079fa927a53d450ea1f`  
		Last Modified: Wed, 22 Jun 2022 19:53:45 GMT  
		Size: 62.6 MB (62641691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd94d63e8bb872454c0e043e42b84aef29a818e0eccf1f9d8a36930fc664903`  
		Last Modified: Wed, 22 Jun 2022 19:53:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2238e214685952250bdae4b8fb9d81159601fa359beaf1b270cb1b0e8ae4515`  
		Last Modified: Wed, 22 Jun 2022 19:53:36 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
