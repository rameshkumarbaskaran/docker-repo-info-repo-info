## `maven:eclipse-temurin`

```console
$ docker pull maven@sha256:11f1cedd958bd4a4933d46cfc44a24e16edb58f85237db1f891d07474a4f51e3
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
$ docker pull maven@sha256:d62c08edc0808c713c819b37f5826cfbcb8785077fc7d562d3facb0d89d3e6ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281577090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044a93ed22f4eb70db682a6d919c5dd349dc046edddfb180dd3ca1d52b780e00`
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
# Tue, 23 Nov 2021 01:03:36 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 23 Nov 2021 01:03:36 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 Nov 2021 01:03:36 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 23 Nov 2021 01:03:36 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 23 Nov 2021 01:03:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:03:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 23 Nov 2021 01:03:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 Nov 2021 01:03:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 Nov 2021 01:03:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 23 Nov 2021 01:03:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 23 Nov 2021 01:03:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 Nov 2021 01:03:56 GMT
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
	-	`sha256:51e6e19af04ed68b7c85e7d23dac26a4d82e492463ffe64b0216390d22368560`  
		Last Modified: Tue, 23 Nov 2021 01:11:36 GMT  
		Size: 31.2 MB (31173281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107af274f391e05fca1a9634fdebd5fd05854c100b6235bfe4f91d09882cb582`  
		Last Modified: Tue, 23 Nov 2021 01:11:26 GMT  
		Size: 9.1 MB (9109803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f5993768bee7e2a808335fbe805cb60470b30b6f8ee744670900ab719ea4df`  
		Last Modified: Tue, 23 Nov 2021 01:11:25 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550483a745dc68ed589abcf74193ff6d329b438676258e5419c30eb38e224f15`  
		Last Modified: Tue, 23 Nov 2021 01:11:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; arm variant v7

```console
$ docker pull maven@sha256:eaa8ac06b73367b4c235915efbd2c1802809243586a60cecff9f114c864b385c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269645937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc49b3e76c022f9bba398964a1b103cbb0b6961f91bccc7ada18a25977641bed`
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
# Fri, 05 Nov 2021 18:59:51 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:00:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:00:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:00:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:00:17 GMT
CMD ["jshell"]
# Tue, 23 Nov 2021 01:51:11 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 23 Nov 2021 01:51:11 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 Nov 2021 01:51:12 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 23 Nov 2021 01:51:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 23 Nov 2021 01:51:34 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:51:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 23 Nov 2021 01:51:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 Nov 2021 01:51:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 Nov 2021 01:51:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 23 Nov 2021 01:51:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 23 Nov 2021 01:51:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 Nov 2021 01:51:47 GMT
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
	-	`sha256:05d5ca3812ed21fcbc8f27c1c9bad8ad703bea957d7656151319326fbe03b130`  
		Last Modified: Fri, 05 Nov 2021 19:06:06 GMT  
		Size: 190.0 MB (189974985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0477169fff55c8b2f84b205c0339e6a962cde1e454925b5e859a3aa07a28639`  
		Last Modified: Fri, 05 Nov 2021 19:04:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4ac4d2fa15f88bbfcfa983738cd716adee768d350f115e93d020948d8068a6`  
		Last Modified: Tue, 23 Nov 2021 01:55:24 GMT  
		Size: 27.3 MB (27298859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1383785ecb02aad24c2acbba33aa9a014cfe9b2f7497fd623a19b89ce3fc3f2`  
		Last Modified: Tue, 23 Nov 2021 01:55:12 GMT  
		Size: 9.1 MB (9109820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9175d8c5b2525a2394c9cc89af5fdfb89ab75b74dd8497840c8caac0ee65b0f`  
		Last Modified: Tue, 23 Nov 2021 01:55:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b1ed58fd57a5b57a71a73ac8c737257e283aea015f994439afbb87aa13fd2`  
		Last Modified: Tue, 23 Nov 2021 01:55:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9df095e0e5f95d6f099c16837c3bffde5a95febbb7043f99e192e5cab3cf2e4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286498139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551ee76e7f564034fbcb1a5cf69569d2635483d2bca92717c52a9b21c8cf71bd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:41:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:42:22 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Mon, 29 Nov 2021 19:42:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 19:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 19:42:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 19:42:35 GMT
CMD ["jshell"]
# Mon, 29 Nov 2021 21:00:17 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 29 Nov 2021 21:00:18 GMT
ARG USER_HOME_DIR=/root
# Mon, 29 Nov 2021 21:00:19 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 29 Nov 2021 21:00:20 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 29 Nov 2021 21:00:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 21:00:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 29 Nov 2021 21:00:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 29 Nov 2021 21:00:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 29 Nov 2021 21:00:53 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 29 Nov 2021 21:00:54 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 29 Nov 2021 21:00:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 29 Nov 2021 21:00:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc7e92316b9d4dee98cf60f4fcb0995823e001fcc5448df92e5fb76485370a`  
		Last Modified: Mon, 29 Nov 2021 19:45:52 GMT  
		Size: 29.4 MB (29377186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d180b2dc1c1c285d6e2b151165c27dfd9d9be3b7b441f2e63cebd618fb21cd`  
		Last Modified: Mon, 29 Nov 2021 19:46:39 GMT  
		Size: 189.9 MB (189863189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba9302b1d1d2223c79e74b1bc37844906cf1abe5d734079f9344f3db9d462ba`  
		Last Modified: Mon, 29 Nov 2021 19:46:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac0f8b6f87664cfd5c98ab7d87868df0f33a4871c68c60bfcf1dfa57b89f588`  
		Last Modified: Mon, 29 Nov 2021 21:04:51 GMT  
		Size: 31.0 MB (30975760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8cd94bfd9b07d9b167ffb664e3bdaec1abfd73381aa4f646d677034ae3e124`  
		Last Modified: Mon, 29 Nov 2021 21:04:47 GMT  
		Size: 9.1 MB (9109763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8e2aaf870d29ed227e0ea2750ffceb33d0be9915c3a7df5bcebea84e415116`  
		Last Modified: Mon, 29 Nov 2021 21:04:46 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d598a84bc120ef3d4747bb42ce680101f04a6ce937cc44770f855b675c21881`  
		Last Modified: Mon, 29 Nov 2021 21:04:46 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; ppc64le

```console
$ docker pull maven@sha256:87dd9baa1117344e7e8d06c249054aa6915103565929e6a0cb80e3079a7a1a5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291029703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938c3ea6e1b5ece39a7d9b5fe30b91c93d7ed8e2145f611ea36d9c7298f2e5b7`
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
# Fri, 05 Nov 2021 20:43:51 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 20:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 20:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 20:44:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 20:44:47 GMT
CMD ["jshell"]
# Tue, 23 Nov 2021 00:42:57 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 23 Nov 2021 00:42:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 Nov 2021 00:43:02 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 23 Nov 2021 00:43:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 23 Nov 2021 00:44:00 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:44:08 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 23 Nov 2021 00:44:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 Nov 2021 00:44:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 Nov 2021 00:44:14 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 23 Nov 2021 00:44:14 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 23 Nov 2021 00:44:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 Nov 2021 00:44:17 GMT
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
	-	`sha256:48d5707e4ca588107d0eae15a1051576b45aba1169c1e6ef17942bdbce6d1e22`  
		Last Modified: Fri, 05 Nov 2021 20:49:49 GMT  
		Size: 188.6 MB (188569215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2627127fbafb8346fd2e7dbb08ad5219f53183753f65008a92fa35c88221f081`  
		Last Modified: Fri, 05 Nov 2021 20:49:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86edcc62c6f34df6e38fd5e6a9f25c29142c1405d4829e9d058c01146db60432`  
		Last Modified: Tue, 23 Nov 2021 00:48:24 GMT  
		Size: 38.4 MB (38370688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8d05e3c52555ebc0d3ba815614463e4e688da20580fedde819c7268f4414c5`  
		Last Modified: Tue, 23 Nov 2021 00:48:17 GMT  
		Size: 9.1 MB (9109819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5218bea8a4bbc360e6aa495788ff69e93704d7764d43d24eb8dada38652a99b`  
		Last Modified: Tue, 23 Nov 2021 00:48:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75933ccc97deadcb9a846c4189cbc87090596dca78842e972164e053dd0227`  
		Last Modified: Tue, 23 Nov 2021 00:48:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:eclipse-temurin` - linux; s390x

```console
$ docker pull maven@sha256:bd9e8f55ba467dc786a1f08efb38862a98376f64da8775a46ebff61c0c007015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275234834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d355b1a7784965fe89ee9862ccad6f44c99f94f018a456730aafa197c45a067`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:45:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:45:46 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Mon, 29 Nov 2021 19:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f23d482b2b4ada08166201d1a0e299e3e371fdca5cd7288dcbd81ae82f3a75e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='f5945a39929384235e7cb1c57df071b8c7e49274632e2a54e54b2bad05de21a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd65d4e8ecc4236924ae34d2075b956799abca594021e1b40c36aa08a0d610b0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dcc17e6ef28984656e997b6b8a6a31c89f45aff87a56b5d3819137c8f1050bef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6ea18c276dcbb8522feeebcfc3a4b5cb7c7e7368ba8590d3326c6c3efc5448b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 19:45:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 19:45:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Nov 2021 19:45:58 GMT
CMD ["jshell"]
# Mon, 29 Nov 2021 20:13:32 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 29 Nov 2021 20:13:32 GMT
ARG USER_HOME_DIR=/root
# Mon, 29 Nov 2021 20:13:32 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 29 Nov 2021 20:13:32 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 29 Nov 2021 20:13:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:13:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 29 Nov 2021 20:13:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 29 Nov 2021 20:13:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 29 Nov 2021 20:13:52 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 29 Nov 2021 20:13:52 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 29 Nov 2021 20:13:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 29 Nov 2021 20:13:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dd1b67c19cd65073e039ddb0ad0478e4ebeff4ccfb02e00bde920aefe11b4b`  
		Last Modified: Mon, 29 Nov 2021 19:47:48 GMT  
		Size: 27.9 MB (27940770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3564f1f4aa560c08eb901fe777d34220aed6913c442b7b14e94e2ed9bbf5e4d9`  
		Last Modified: Mon, 29 Nov 2021 19:48:18 GMT  
		Size: 180.4 MB (180365429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e5594c887f1de34e7a6518cb7c4c336269ff428a1b4bed0409ca5fcffbb4c`  
		Last Modified: Mon, 29 Nov 2021 19:48:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4db9b26694c1fe2218b5bb7b74eb5b66db5ebd2c1736414c613bc1293b4809`  
		Last Modified: Mon, 29 Nov 2021 20:16:00 GMT  
		Size: 30.7 MB (30696594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a5e64ecd67de0a3b1b20772f77a5a214b9b656da35d86116dcc76ac80ca590`  
		Last Modified: Mon, 29 Nov 2021 20:15:57 GMT  
		Size: 9.1 MB (9109812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e35ccc108adbc9ae4de9d4a5c36950752921fc612e0fc6fe8f6164bcdd331f9`  
		Last Modified: Mon, 29 Nov 2021 20:15:56 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c88a3ebdefae2f08aa1697f68b2d8d6bba4e49c38a4b359632fa5ea3e238d14`  
		Last Modified: Mon, 29 Nov 2021 20:15:56 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
