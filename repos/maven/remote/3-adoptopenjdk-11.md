## `maven:3-adoptopenjdk-11`

```console
$ docker pull maven@sha256:d8c1b900ec7d68fcd7cb2dc1d8e42e99e684df246ec3a6fec1f1f4c278bad5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-adoptopenjdk-11` - linux; amd64

```console
$ docker pull maven@sha256:1d4c8d01b77eebfe8c8fd2786d55285dcd8e15bcc8a4dff62cbcfd5527e3ea0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274273263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9848db14bce553b5768f52679c449bdb58ac4cfa21f55c811bf33f06d2d01803`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:10:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 25 Sep 2020 23:11:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:11:51 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Fri, 25 Sep 2020 23:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 25 Sep 2020 23:12:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Sep 2020 23:12:02 GMT
CMD ["jshell"]
# Sat, 26 Sep 2020 03:32:11 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 26 Sep 2020 03:32:11 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Sep 2020 03:32:12 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 26 Sep 2020 03:32:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 26 Sep 2020 03:32:23 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:32:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 26 Sep 2020 03:32:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Sep 2020 03:32:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Sep 2020 03:32:25 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 26 Sep 2020 03:32:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 26 Sep 2020 03:32:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Sep 2020 03:32:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4d4e9526b1adecc10515315b09e75d88526e75fba0552b3fbb933f40d293e9`  
		Last Modified: Fri, 25 Sep 2020 23:16:31 GMT  
		Size: 13.9 MB (13875646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fc1ae9a8123ef615b5a4cfe87484bfac83d0ec89c22fed22b5f81fda1c6bb1`  
		Last Modified: Fri, 25 Sep 2020 23:17:29 GMT  
		Size: 194.3 MB (194266367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeaea30268f56b60d5c532d085c2a4d9ff99843856ef26fbd3c802cad8b5898`  
		Last Modified: Sat, 26 Sep 2020 03:34:49 GMT  
		Size: 29.8 MB (29846207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5685f1046ce0fd50bd4e533339b78c2780058954e3e252f88374e069de9bee8c`  
		Last Modified: Sat, 26 Sep 2020 03:34:45 GMT  
		Size: 9.6 MB (9581206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426eacd02056e4f48c7f769208c0e55defbd1ca4e1eb1b21596b86d73d6140ad`  
		Last Modified: Sat, 26 Sep 2020 03:34:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd192f5bdc22f2e88e15039b548901ae19ed0a6521d9d2a51623f6731fd96207`  
		Last Modified: Sat, 26 Sep 2020 03:34:44 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-adoptopenjdk-11` - linux; arm variant v7

```console
$ docker pull maven@sha256:ce465685b2d4c1a089f940629febd42696cd8a06c634ba7453d71c318419abde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261686145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24841b48cb77ff1258892cf66a9de92ce8585e59216c0410bdf76f5b819257f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Oct 2020 18:16:23 GMT
ADD file:7eef4725b8e0594e6d033da471b98f508fde3df29100aa6cdc33180d4524cf62 in / 
# Fri, 23 Oct 2020 18:16:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:16:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:16:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:16:30 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:57:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 17:58:03 GMT
ENV JAVA_VERSION=jdk-11.0.9+11
# Wed, 28 Oct 2020 17:58:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f90c6f941a95e20e305870700328804e5b48acb69d4928dc9c4627b3c755ae8a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9_11.tar.gz';          ;;        armhf|armv7l)          ESUM='082a13a9a5fbcf7ca45e67ab39e9682a9ef9e3779395e37aa0bf235e42a8eaf5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5c619e9acc182b0e40391c8c378ede120bb4ef7b8f0312d582d7aa1ecc684bd6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9_11.tar.gz';          ;;        s390x)          ESUM='e5cf6026a37db22133c671e4643e9735f8a9e8b85aa5a30f0dbeac8367d0a6a7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9_11.tar.gz';          ;;        amd64|x86_64)          ESUM='a3c52b73a76bed0f113604165eb4f2020b767e188704d8cc0bfc8bc4eb596712';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 28 Oct 2020 17:58:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 17:58:24 GMT
CMD ["jshell"]
# Wed, 28 Oct 2020 18:59:56 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 28 Oct 2020 18:59:57 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Oct 2020 18:59:58 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 28 Oct 2020 18:59:59 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 28 Oct 2020 19:00:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 19:00:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 28 Oct 2020 19:00:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Oct 2020 19:00:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Oct 2020 19:00:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 28 Oct 2020 19:00:49 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 28 Oct 2020 19:00:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Oct 2020 19:00:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b3c478921ca13a317a5584d4f9ec27e1688931fcc71a74949622ecd0dca63baa`  
		Last Modified: Mon, 12 Oct 2020 16:20:05 GMT  
		Size: 24.0 MB (24039636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98985506b7e726afa2b8d178a88ffec8b51c3ae9d7f6f11279e5000c808761e`  
		Last Modified: Fri, 23 Oct 2020 18:17:41 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd88c4be5a76e00881f4097c47a3db7ea802048fb9e329475381f78c0ce82767`  
		Last Modified: Fri, 23 Oct 2020 18:17:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b32800feb068752db1ddbe364b95691e153ec4ddc17b7cea4f6502255a829b`  
		Last Modified: Wed, 28 Oct 2020 18:00:39 GMT  
		Size: 14.9 MB (14905244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b33478ddbf1e7fd9ec2e388b3a075c0503708b1efd9b56db2294669b8eeccaa`  
		Last Modified: Wed, 28 Oct 2020 18:01:08 GMT  
		Size: 183.8 MB (183829720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7acf019677417e4c93b67b57923b7d913db0c5d2ff061bcb172364435012c4`  
		Last Modified: Wed, 28 Oct 2020 19:03:40 GMT  
		Size: 29.3 MB (29328086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986243adb9ab4e7693c7609e11d9953a860638c561acaf549e2143683d782615`  
		Last Modified: Wed, 28 Oct 2020 19:03:31 GMT  
		Size: 9.6 MB (9581203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25b1626f1c0c339ebb06adb67cc330b46a3759a54d8a9460c8b7241eba5b39d`  
		Last Modified: Wed, 28 Oct 2020 19:03:28 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac0fc6d437f067ee5113b6d7cd1f2e62455521a318e7fc89b70a189f1424143`  
		Last Modified: Wed, 28 Oct 2020 19:03:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-adoptopenjdk-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:40db39b7daad604734cf3ee0b38917ff351453087e84bffb52b6835a4f099633
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278257227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136499dc41be5c5ed17f7c2f670e37de65343630d5f73f625020b1600cdb99ce`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Oct 2020 18:19:38 GMT
ADD file:83fb716eb29f83f9e0ea0422f76e651689972d98764d3e19e4017bbd3fe9d6e4 in / 
# Fri, 23 Oct 2020 18:19:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:19:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:19:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:19:45 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:39:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 17:40:36 GMT
ENV JAVA_VERSION=jdk-11.0.9+11
# Wed, 28 Oct 2020 17:40:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f90c6f941a95e20e305870700328804e5b48acb69d4928dc9c4627b3c755ae8a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9_11.tar.gz';          ;;        armhf|armv7l)          ESUM='082a13a9a5fbcf7ca45e67ab39e9682a9ef9e3779395e37aa0bf235e42a8eaf5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5c619e9acc182b0e40391c8c378ede120bb4ef7b8f0312d582d7aa1ecc684bd6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9_11.tar.gz';          ;;        s390x)          ESUM='e5cf6026a37db22133c671e4643e9735f8a9e8b85aa5a30f0dbeac8367d0a6a7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9_11.tar.gz';          ;;        amd64|x86_64)          ESUM='a3c52b73a76bed0f113604165eb4f2020b767e188704d8cc0bfc8bc4eb596712';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 28 Oct 2020 17:40:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 17:40:53 GMT
CMD ["jshell"]
# Wed, 28 Oct 2020 18:59:54 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 28 Oct 2020 18:59:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Oct 2020 18:59:55 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 28 Oct 2020 18:59:56 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 28 Oct 2020 19:00:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 19:00:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 28 Oct 2020 19:00:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Oct 2020 19:00:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Oct 2020 19:00:41 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 28 Oct 2020 19:00:42 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 28 Oct 2020 19:00:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Oct 2020 19:00:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:00f57adb053c38c53d0655dee1ba47ed4cbd78cade062cf0e00f4b9790c7ed36`  
		Last Modified: Thu, 08 Oct 2020 08:25:26 GMT  
		Size: 27.2 MB (27163834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235828e8d75b4f9129ec8b0a00d4e3f1c4d100eedb3f00696a2ec78862082f6`  
		Last Modified: Fri, 23 Oct 2020 18:20:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b606b1b8abdd386d8de6d1ce374b4dcdd4f7bcb4d68db64f09c03520fa5bf5`  
		Last Modified: Fri, 23 Oct 2020 18:20:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a951fec6a8b3a6343c6c0eef63817beea922df0909420fda024ca78942b25040`  
		Last Modified: Wed, 28 Oct 2020 17:50:59 GMT  
		Size: 15.9 MB (15898160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902024df57f00fa010eac8d30a0e285a4dd2d5bdfaed8ead7a9febff0a7bc5c7`  
		Last Modified: Wed, 28 Oct 2020 17:52:11 GMT  
		Size: 192.3 MB (192279204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518eb8894659bca8caa2003f65ce17d969be518458283150f5992a529891a60f`  
		Last Modified: Wed, 28 Oct 2020 19:04:34 GMT  
		Size: 33.3 MB (33332526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868bf314d7b4e2c19f9739b756592b43c2e06bfefa20ac1ebf1e3deeae16c5b9`  
		Last Modified: Wed, 28 Oct 2020 19:04:25 GMT  
		Size: 9.6 MB (9581251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06135e0a7bac5a771814d06545903e25c6eee7d9b82bdfd3c05ae3411cf9464`  
		Last Modified: Wed, 28 Oct 2020 19:04:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaa950f7fd2c23d123a53c5d0b248e7f29c371df89798ac2b9caa335ab55cf4`  
		Last Modified: Wed, 28 Oct 2020 19:04:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-adoptopenjdk-11` - linux; ppc64le

```console
$ docker pull maven@sha256:336195ebcf275f36e8af08f9ebb48916a287b282870859faaa5694be25088386
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269096981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818a23a00ca61d9f55c98c78a2118a5ecd80d8457a75a9dcd8f0d30d5d1cead6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:37:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Sep 2020 03:39:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:40:37 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Sat, 26 Sep 2020 03:41:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fb27ea52ed901c14c9fe8ad2fc10b338b8cf47d6762571be1fe3fb7c426bab7c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.8_10.tar.gz';          ;;        armhf|armv7l)          ESUM='d00370967e4657e137cc511e81d6accbfdb08dba91e6268abef8219e735fbfc5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.8_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d206a63cd719b65717f7f20ee3fe49f0b8b2db922986b4811c828db57212699e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.8_10.tar.gz';          ;;        s390x)          ESUM='5619e1437c7cd400169eb7f1c831c2635fdb2776a401147a2fc1841b01f83ed6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.8_10.tar.gz';          ;;        amd64|x86_64)          ESUM='6e4cead158037cb7747ca47416474d4f408c9126be5b96f9befd532e0a762b47';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 26 Sep 2020 03:41:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Sep 2020 03:41:17 GMT
CMD ["jshell"]
# Sat, 26 Sep 2020 05:19:48 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 26 Sep 2020 05:19:50 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Sep 2020 05:19:52 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 26 Sep 2020 05:19:54 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 26 Sep 2020 05:20:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 05:21:04 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 26 Sep 2020 05:21:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Sep 2020 05:21:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Sep 2020 05:21:08 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 26 Sep 2020 05:21:08 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 26 Sep 2020 05:21:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Sep 2020 05:21:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f274fd8d44c41b563fd8be80792424906ae7f32bacbb53d3fc872271889baf`  
		Last Modified: Sat, 26 Sep 2020 03:54:38 GMT  
		Size: 14.5 MB (14518670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bfcd61713facb3b38a41ef76b536740fc2dbb64e2544457bfbc1bb73a9fa`  
		Last Modified: Sat, 26 Sep 2020 03:56:31 GMT  
		Size: 177.3 MB (177275863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0575916a5da1f70a5ae95ebf4bd62558e067758c6e5cea2abd937c96e93f180`  
		Last Modified: Sat, 26 Sep 2020 05:29:08 GMT  
		Size: 37.3 MB (37310499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559e9a905007431b81df69856e83fec2e29ea19bedc3b7bfeeb93962bedf1f6`  
		Last Modified: Sat, 26 Sep 2020 05:29:01 GMT  
		Size: 9.6 MB (9581198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54de673190d387066a54bcf951a68fd28bf44dd9755d3fbd6aba25b1a9406a6`  
		Last Modified: Sat, 26 Sep 2020 05:29:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1732eb129b305f7c01a09ad64c06be653a77e0f00a6dec86d6356356b0aef1`  
		Last Modified: Sat, 26 Sep 2020 05:28:59 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-adoptopenjdk-11` - linux; s390x

```console
$ docker pull maven@sha256:4159f63536d94e8c876aaab89b44123f2749ed464baeb5762342eca2ddaef0fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255906077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d379adfb3b53bddbeb8d0e3616ccfccd5b3112fe518d24a5e263cc23dd90685`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Oct 2020 19:09:19 GMT
ADD file:9b934c86e9ab1dd29cef318d8dd9cd1228b9d92124f434c50ad7d03ede1a5c76 in / 
# Fri, 23 Oct 2020 19:09:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:09:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:09:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:09:27 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:41:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:41:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 17:42:10 GMT
ENV JAVA_VERSION=jdk-11.0.9+11
# Wed, 28 Oct 2020 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f90c6f941a95e20e305870700328804e5b48acb69d4928dc9c4627b3c755ae8a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.9_11.tar.gz';          ;;        armhf|armv7l)          ESUM='082a13a9a5fbcf7ca45e67ab39e9682a9ef9e3779395e37aa0bf235e42a8eaf5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_arm_linux_hotspot_11.0.9_11.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5c619e9acc182b0e40391c8c378ede120bb4ef7b8f0312d582d7aa1ecc684bd6';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.9_11.tar.gz';          ;;        s390x)          ESUM='e5cf6026a37db22133c671e4643e9735f8a9e8b85aa5a30f0dbeac8367d0a6a7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.9_11.tar.gz';          ;;        amd64|x86_64)          ESUM='a3c52b73a76bed0f113604165eb4f2020b767e188704d8cc0bfc8bc4eb596712';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11.1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.9_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 28 Oct 2020 17:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 17:42:26 GMT
CMD ["jshell"]
# Wed, 28 Oct 2020 18:43:47 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 28 Oct 2020 18:43:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Oct 2020 18:43:48 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 28 Oct 2020 18:43:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 28 Oct 2020 18:44:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 18:44:15 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 28 Oct 2020 18:44:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Oct 2020 18:44:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Oct 2020 18:44:16 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 28 Oct 2020 18:44:16 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 28 Oct 2020 18:44:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Oct 2020 18:44:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d3e8e1a5d50716d6aabb0cef46599f9e7a722a560910d6f724737aaef0a7d6c3`  
		Last Modified: Mon, 12 Oct 2020 16:45:31 GMT  
		Size: 27.2 MB (27224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04282efaafb3c9b53bba677fc3c06c478dc1613c1f21939bfa2c113aeef2f99c`  
		Last Modified: Fri, 23 Oct 2020 19:10:20 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6269ae100536d7559ae6ebe6606b4405ebb706c3d963926c5568b6e7fd954582`  
		Last Modified: Fri, 23 Oct 2020 19:10:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cd8065d26d8f90607b2debf915de6242befbe898f8fb305dbd99dc8df92d3a`  
		Last Modified: Wed, 28 Oct 2020 17:59:30 GMT  
		Size: 15.8 MB (15772935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cac7c75b6930521a2df30b21ecf8c0a0d8835892732acd7cdf76a5464299a5c`  
		Last Modified: Wed, 28 Oct 2020 18:00:09 GMT  
		Size: 170.1 MB (170085834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e0c588f2c584a83a4b5b481097cc73af1113b641025ad72212bddd15ada228`  
		Last Modified: Wed, 28 Oct 2020 18:46:19 GMT  
		Size: 33.2 MB (33239457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b9ee86bcbb94e44fd2db4197623e838cab6c029930c38379d46b8b503bc9d1`  
		Last Modified: Wed, 28 Oct 2020 18:46:14 GMT  
		Size: 9.6 MB (9581206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f601bb257076229dea623e16a98c11045dcc8e8fcdcd6a27a62da707c2aebe`  
		Last Modified: Wed, 28 Oct 2020 18:46:14 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd18ead3a13770f1f82a6e91e4fd2a325c628cfc6c4d7eb1808eb8c1838f2ac`  
		Last Modified: Wed, 28 Oct 2020 18:46:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
