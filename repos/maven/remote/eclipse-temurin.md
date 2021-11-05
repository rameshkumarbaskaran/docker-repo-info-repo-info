## `maven:eclipse-temurin`

```console
$ docker pull maven@sha256:593c5c6ce01e5a8abbd55ffed41fddfd4abb0a3af3d2e0a48d10ab8e86e65f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:eclipse-temurin` - linux; amd64

```console
$ docker pull maven@sha256:af8068725ab22efc4f46dee1740684a7108dca39824aeaf8dd97b2176016d175
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281573432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0e99dc64e1fa3605a7743e9d14761ae4772bf60ce63170b531b3575fc7aa01`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:45:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:21:12 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:21:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:21:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:21:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:21:24 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 19:53:20 GMT
ARG MAVEN_VERSION=3.8.3
# Fri, 05 Nov 2021 19:53:20 GMT
ARG USER_HOME_DIR=/root
# Fri, 05 Nov 2021 19:53:20 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Fri, 05 Nov 2021 19:53:20 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Fri, 05 Nov 2021 19:53:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:53:42 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 05 Nov 2021 19:53:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 05 Nov 2021 19:53:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 05 Nov 2021 19:53:42 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 05 Nov 2021 19:53:42 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 05 Nov 2021 19:53:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 05 Nov 2021 19:53:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1fba688e4817fa2b044e9fc220607825d6d823866f99050e9f3321efdfa28d`  
		Last Modified: Sat, 16 Oct 2021 02:48:44 GMT  
		Size: 19.8 MB (19776863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3df373e15f054e24e0d95fa17206269e55fba11786b331b7b714252967596b`  
		Last Modified: Fri, 05 Nov 2021 19:25:26 GMT  
		Size: 192.9 MB (192948668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0264cf7a54d1c1d5f04aea163d6217e75a85afa86c618ce8f2668c622c5743`  
		Last Modified: Fri, 05 Nov 2021 19:25:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8894e602bfdf7e5f791098527cd6c924f25faba63b3df29cc53b0ebf9c2fcff1`  
		Last Modified: Fri, 05 Nov 2021 19:55:48 GMT  
		Size: 31.2 MB (31173784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96579c5a6feeafc846ab109b1bbf60bc1c9789556c6756f7ef5d28c8ca26394`  
		Last Modified: Fri, 05 Nov 2021 19:55:44 GMT  
		Size: 9.1 MB (9105640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d731f986f3a197ba33de8b812bde2f365806a42df75624d84372ae1b31d3aad1`  
		Last Modified: Fri, 05 Nov 2021 19:55:43 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a077d63aa39fac6028402db5092034fe9315c7a29d21e8c6f73f62a2da8b8e`  
		Last Modified: Fri, 05 Nov 2021 19:55:43 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; arm variant v7

```console
$ docker pull maven@sha256:88edaea15e56c84ee833f484a531cdd42995bb03acb6bc27f5128a8915ce04fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269609057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0ff09cc2606f61656094ae6701420ca3473a6c0b112045610cb164b295e54b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:38:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:41:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:41:49 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 02:42:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 02:42:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 02:42:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 02:42:15 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 04:01:15 GMT
ARG MAVEN_VERSION=3.8.3
# Sat, 16 Oct 2021 04:01:16 GMT
ARG USER_HOME_DIR=/root
# Sat, 16 Oct 2021 04:01:16 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Sat, 16 Oct 2021 04:01:17 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Sat, 16 Oct 2021 04:01:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 04:01:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 16 Oct 2021 04:01:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 16 Oct 2021 04:01:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 16 Oct 2021 04:01:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 16 Oct 2021 04:01:49 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 16 Oct 2021 04:01:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 16 Oct 2021 04:01:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73092bd78be324813f4a4bdc7c75343bcc4753cf3a97145d91d7c8d8ae1ec9e`  
		Last Modified: Sat, 16 Oct 2021 02:47:09 GMT  
		Size: 19.2 MB (19196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064c13554afddb973cfd835b83cd228df95d30d6d0fece99cddbe8c945c7357`  
		Last Modified: Sat, 16 Oct 2021 02:48:11 GMT  
		Size: 189.9 MB (189942672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ee8a7d282cdb18249ff177cae80de70c5e3edb97c727bf4d5c02cc66710c8`  
		Last Modified: Sat, 16 Oct 2021 02:46:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2bed739e26e96919d91158c88e44fceaef431cd2fb4fafb7681f27617a764`  
		Last Modified: Sat, 16 Oct 2021 04:06:11 GMT  
		Size: 27.3 MB (27298503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17eabb5105dab8e0d16ddd4f7056ef9074c42921cc746d84690700e813a1e33`  
		Last Modified: Sat, 16 Oct 2021 04:05:56 GMT  
		Size: 9.1 MB (9105609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9670486e0b9a3ea1ad87e1bb9ebd38ed95d263f54e25bd95238163f54720b05`  
		Last Modified: Sat, 16 Oct 2021 04:05:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144a0ee82600bba5f2b57dbb67d8b643c894d60d487f28c7cad2ff39e7eab877`  
		Last Modified: Sat, 16 Oct 2021 04:05:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f4cb959c099674d59eb3089e9e8e2827f25e69c58fcdb7210e17ac3becda79fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277606246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d684db70b0a7fb0ac3d92faf9f613ee1458745ce1d9b591dc7214c1f22d68de`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 03:28:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:41:17 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:41:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:41:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:41:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:41:30 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 20:06:28 GMT
ARG MAVEN_VERSION=3.8.3
# Fri, 05 Nov 2021 20:06:29 GMT
ARG USER_HOME_DIR=/root
# Fri, 05 Nov 2021 20:06:30 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Fri, 05 Nov 2021 20:06:31 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Fri, 05 Nov 2021 20:06:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 20:07:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 05 Nov 2021 20:07:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 05 Nov 2021 20:07:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 05 Nov 2021 20:07:07 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 05 Nov 2021 20:07:08 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 05 Nov 2021 20:07:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 05 Nov 2021 20:07:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d246d72cf3fa2492fcec79d12e7ddff4b26bc404f31671d0b6b45956f4659e21`  
		Last Modified: Sat, 16 Oct 2021 03:34:39 GMT  
		Size: 20.5 MB (20497588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c62fe607b6fbf978dd8aaefc8e820909f5b0e2e258a1f46ebcc1ce0db722d48`  
		Last Modified: Fri, 05 Nov 2021 19:45:38 GMT  
		Size: 189.9 MB (189863235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f1465365f2502f4fd118d1a6f7d79cf1f35b46c55815e828aedb5905afac59`  
		Last Modified: Fri, 05 Nov 2021 19:45:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5082f69f49d0a23effffd17657ae40ff46744efddbcea3aa8c8ca19c17a8e5`  
		Last Modified: Fri, 05 Nov 2021 20:10:47 GMT  
		Size: 31.0 MB (30967603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915729bd40e210b9173cf111094cce50d176002687bd29b37d475c94593614bd`  
		Last Modified: Fri, 05 Nov 2021 20:10:43 GMT  
		Size: 9.1 MB (9105577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e21465a1ffc6073ff492f2da360698402b2beabf276ed645a4eba95faefc40f`  
		Last Modified: Fri, 05 Nov 2021 20:10:42 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a71c77db632ef2600ada9f1b823cd190ee36a4a162db2a0eaf1fbc92087524`  
		Last Modified: Fri, 05 Nov 2021 20:10:42 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; ppc64le

```console
$ docker pull maven@sha256:edf352482a70fe6213c51345ee50dda34527782d2091c7fc6342bfee49441292
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291007125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bb51c468076fda86439b670b74a3f64e7fd2b708e7efa664288bd33cd12dc0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:59:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:00:40 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 01:01:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 01:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 01:01:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 01:01:22 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 03:18:34 GMT
ARG MAVEN_VERSION=3.8.3
# Sat, 16 Oct 2021 03:18:36 GMT
ARG USER_HOME_DIR=/root
# Sat, 16 Oct 2021 03:18:41 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Sat, 16 Oct 2021 03:18:43 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Sat, 16 Oct 2021 03:19:39 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:19:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 16 Oct 2021 03:19:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 16 Oct 2021 03:19:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 16 Oct 2021 03:19:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 16 Oct 2021 03:19:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 16 Oct 2021 03:19:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 16 Oct 2021 03:20:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c039cd0909346123aad04b02731eff4b76a8183bac5eb82e2d477f9e3ecd1260`  
		Last Modified: Sat, 16 Oct 2021 01:05:05 GMT  
		Size: 21.7 MB (21691370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfd2de7d19685e6fa2fd563f642aee9263750b7eb94c5192fdbab6ded0ce3c9`  
		Last Modified: Sat, 16 Oct 2021 01:06:02 GMT  
		Size: 188.6 MB (188550881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c694d366736b5f652319c576193e51d7f7b576fb0a76cb475d3c252f808f2183`  
		Last Modified: Sat, 16 Oct 2021 01:05:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9076bc223eb832a5104f09d7e384c1f3a4f8299203859bd165736bc11a3dfe6e`  
		Last Modified: Sat, 16 Oct 2021 03:25:51 GMT  
		Size: 38.4 MB (38370640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870ace11f370337a09433b00469eb5da530892bdb2c2d9faa50d67b653cc08a1`  
		Last Modified: Sat, 16 Oct 2021 03:25:44 GMT  
		Size: 9.1 MB (9105622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d49191d099d0ac3f9947a4e0e5de8e250d27554a56e957f9ee4a05f99883ee`  
		Last Modified: Sat, 16 Oct 2021 03:25:43 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504b97d1011e17b3b50c49fcfd3f3ceeac776beff19481af28717e8c37b6f1d8`  
		Last Modified: Sat, 16 Oct 2021 03:25:43 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; s390x

```console
$ docker pull maven@sha256:8b3bf1c494cea05c501b5e011b0dcaf2226e845bde110d055fad4b0fae656079
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266518753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870a968b653a2ac077782f252e64b08ebe003f9f4f2dac86fd0187762ade89ba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:59:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:41:48 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:41:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:42:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:42:03 GMT
CMD ["jshell"]
# Fri, 05 Nov 2021 20:19:33 GMT
ARG MAVEN_VERSION=3.8.3
# Fri, 05 Nov 2021 20:19:33 GMT
ARG USER_HOME_DIR=/root
# Fri, 05 Nov 2021 20:19:33 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Fri, 05 Nov 2021 20:19:33 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Fri, 05 Nov 2021 20:19:42 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 20:19:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 05 Nov 2021 20:19:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 05 Nov 2021 20:19:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 05 Nov 2021 20:19:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 05 Nov 2021 20:19:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 05 Nov 2021 20:19:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 05 Nov 2021 20:19:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d62f01df0df55e65f1037a428195076b6423d10d10ef3ae844e054d6a82597a`  
		Last Modified: Sat, 16 Oct 2021 01:01:35 GMT  
		Size: 19.2 MB (19236649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f67bf6b3f189ec83683427932c226f1aaf749d054122b356911a116386c3d21`  
		Last Modified: Fri, 05 Nov 2021 19:43:21 GMT  
		Size: 180.4 MB (180365428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956023a06e5d3dcf52d3d70db75ac254e5901921c10a51620866d519476d00`  
		Last Modified: Fri, 05 Nov 2021 19:43:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee4e3f8c0e2c4fdcbebceb92331828119b43568927ef59e6252e3b20630a7b`  
		Last Modified: Fri, 05 Nov 2021 20:21:00 GMT  
		Size: 30.7 MB (30688827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10af7a2d9d7735aa2e910ccf8859f111716c989106dd86554de3172bed76e109`  
		Last Modified: Fri, 05 Nov 2021 20:20:57 GMT  
		Size: 9.1 MB (9105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b4ce0a5dd01afbe9c554ede44519409d59096fb27dd107c0a1b39251fe65cf`  
		Last Modified: Fri, 05 Nov 2021 20:20:56 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7f6c6e2624c9ff0b96927628644fca9f3e3c4c7ea6d45abe2f195d8dd78e6e`  
		Last Modified: Fri, 05 Nov 2021 20:20:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
