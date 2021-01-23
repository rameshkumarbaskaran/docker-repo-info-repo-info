## `gradle:jdk`

```console
$ docker pull gradle@sha256:9f01be794c09a9f1e69e3ae63bef5480f0b520f5136648f3ec4d295387d3a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jdk` - linux; amd64

```console
$ docker pull gradle@sha256:ea20cad7ee3d3529344ebac713f33e7397365fdc7ca3b51da8635bf21a13871e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322665487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596aa3136005fc82a9b35fc9d02ace9a6ce5907c3f54060edfea9c381af15f4c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 00:39:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 26 Nov 2020 00:39:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 00:39:43 GMT
ENV JAVA_VERSION=jdk8u275-b01
# Thu, 26 Nov 2020 00:39:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='aeade06192ce4544f998b4957cd2c0ed3f9f8eac08b0de5d2ed55c55283364af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u275b01.tar.gz';          ;;        armhf|armv7l)          ESUM='e2e41a8705061dfcc766bfb6b7edd4c699e94aac68e4deeb28c8e76734a46fb7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u275b01.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a7b1c803e581f226216f73aca878bfd1b149c422b63e42e64eeeecda78c2253b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u275b01.tar.gz';          ;;        s390x)          ESUM='f513b895d28bdc2011b698e4a9ee3ea524d0e7bb62d87b0f53814a326573ec04';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_s390x_linux_hotspot_8u275b01.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='06fb04075ed503013beb12ab87963b2ca36abe9e397a0c298a57c1d822467c29';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u275b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 26 Nov 2020 00:39:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Jan 2021 09:28:33 GMT
CMD ["gradle"]
# Wed, 13 Jan 2021 09:28:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Jan 2021 09:28:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 13 Jan 2021 09:28:34 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Jan 2021 09:28:35 GMT
WORKDIR /home/gradle
# Wed, 13 Jan 2021 09:29:21 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 13 Jan 2021 09:29:21 GMT
ENV GRADLE_VERSION=6.8
# Wed, 13 Jan 2021 09:29:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=e2774e6fb77c43657decde25542dea710aafd78c4022d19b196e7e78d79d8c6c
# Wed, 13 Jan 2021 09:29:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e2774e6fb77c43657decde25542dea710aafd78c4022d19b196e7e78d79d8c6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c07f69a5e5c1c84cfd4566011622ffa52b8d00336abda1dd767c51718498628`  
		Last Modified: Thu, 26 Nov 2020 00:56:19 GMT  
		Size: 16.0 MB (16032786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5111f7fe9d0903a336bfe977abbff66d20dcb912d54f5b3c388fd55c8354ff61`  
		Last Modified: Thu, 26 Nov 2020 00:56:26 GMT  
		Size: 104.6 MB (104619280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91e2cdf561b4c3c2af2bfa8f735f5239b0088b93281ab00c29c007100ebb419`  
		Last Modified: Wed, 13 Jan 2021 09:36:04 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ddf85377d7dae389d6d2680070c898b787099c75de9ee5c61f26adc1aa2680`  
		Last Modified: Wed, 13 Jan 2021 09:36:20 GMT  
		Size: 65.6 MB (65583890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40883e272809703c8e14e6d3c66519b9985f4b633249ec0475b8ac13cb7f508`  
		Last Modified: Wed, 13 Jan 2021 09:36:17 GMT  
		Size: 107.9 MB (107860920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk` - linux; arm variant v7

```console
$ docker pull gradle@sha256:0a2a5f044b2b050e37b9c7a8fbd023f9e3624d044ea13327960c594b61263123
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281642539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f791489bbfed259267b4c2c8a2d0f5617a29177d2b3d8fbe9ad3522c2f2e36a3`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 25 Sep 2020 23:04:32 GMT
ADD file:0ddc5fefae097a5be4c925fdfc09e4a637b74627a8981f0e6fb9890580adc875 in / 
# Fri, 25 Sep 2020 23:04:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:04:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:04:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:04:40 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:23:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 25 Sep 2020 23:23:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 20 Oct 2020 17:00:24 GMT
ENV JAVA_VERSION=jdk8u265-b01
# Tue, 20 Oct 2020 17:00:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='87d16dac293d2a9abbb559a277bfaded702f28d1bfdc526f8613bb9cfed84a12';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u265b01.tar.gz';          ;;        armhf|armv7l)          ESUM='dc3405aab81f422b7721f665c76371bd7b03c291eea89cd110a82d8bcf07809a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u265b01.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7bbb9d76458ee29bc5e2458b32a91b8c032ecffe6cb8500734ca41d2d8f5c9f3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u265b01.tar.gz';          ;;        s390x)          ESUM='aca50f02d59169cb428d54501846b518edc9fff6a6f428459c72b4faa2b4abb0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_s390x_linux_hotspot_8u265b01.tar.gz';          ;;        amd64|x86_64)          ESUM='1285da6278f2d38a790a21148d7e683f20de0799c44b937043830ef6b57f58c4';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u265b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 20 Oct 2020 17:00:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Oct 2020 18:58:36 GMT
CMD ["gradle"]
# Wed, 21 Oct 2020 18:58:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Oct 2020 18:58:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 21 Oct 2020 18:58:55 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Oct 2020 18:58:56 GMT
WORKDIR /home/gradle
# Wed, 11 Nov 2020 00:59:59 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 20:57:55 GMT
ENV GRADLE_VERSION=6.7.1
# Tue, 17 Nov 2020 20:57:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Tue, 17 Nov 2020 20:58:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:20e126218ac644f56ef7147c3363108a0814d921e6016af54a1b4c964159f1a9`  
		Last Modified: Fri, 25 Sep 2020 23:06:39 GMT  
		Size: 22.3 MB (22279517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d156c2b31482935ec0363b6e3f1cb6fc56da57e61fc80078914918fe53f8fa5`  
		Last Modified: Fri, 25 Sep 2020 23:06:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1a0dbe2162972438aa89d4f90dca5db0e4cee58819ba354ea1c0031101b7a`  
		Last Modified: Fri, 25 Sep 2020 23:06:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b333d1b8f5fe5303d427301eecab31e2fb825ddfe9ed1f96b70bc80a74f9fa44`  
		Last Modified: Fri, 25 Sep 2020 23:27:19 GMT  
		Size: 12.8 MB (12817173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98cd0e06d4aa392d4642f2ac01a346abecad7b77a0d7f57f0e619dfbe5599d3`  
		Last Modified: Tue, 20 Oct 2020 17:03:25 GMT  
		Size: 98.2 MB (98179329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f609d81c490355ea84093ac1ddae49eb6680e0df52f909030ce66d02f9a653bb`  
		Last Modified: Wed, 21 Oct 2020 19:06:24 GMT  
		Size: 4.5 KB (4524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329d1f762f60657829ea9e53e40f8cd0dbc960352bab777d36785267f1e23b37`  
		Last Modified: Wed, 11 Nov 2020 01:08:05 GMT  
		Size: 45.5 MB (45509529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf5ce505c18d4d7ba80b05aa91304c4b1a224f7b7024a32fad41ff6005ee083`  
		Last Modified: Tue, 17 Nov 2020 21:01:42 GMT  
		Size: 102.9 MB (102851429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:40a5714e734d755b855c084a33841cdd3521e85c70030d7ea6e26ba590db130c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315295634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645a8ccd948dbf66ccd11d228a3c7e09f6f4ee1292feec8fb67095487236c75c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:16:34 GMT
ENV JAVA_VERSION=jdk8u275-b01
# Thu, 21 Jan 2021 05:16:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='aeade06192ce4544f998b4957cd2c0ed3f9f8eac08b0de5d2ed55c55283364af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u275b01.tar.gz';          ;;        armhf|armv7l)          ESUM='e2e41a8705061dfcc766bfb6b7edd4c699e94aac68e4deeb28c8e76734a46fb7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u275b01.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a7b1c803e581f226216f73aca878bfd1b149c422b63e42e64eeeecda78c2253b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u275b01.tar.gz';          ;;        s390x)          ESUM='f513b895d28bdc2011b698e4a9ee3ea524d0e7bb62d87b0f53814a326573ec04';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_s390x_linux_hotspot_8u275b01.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='06fb04075ed503013beb12ab87963b2ca36abe9e397a0c298a57c1d822467c29';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u275b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 05:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Jan 2021 23:42:09 GMT
CMD ["gradle"]
# Fri, 22 Jan 2021 23:42:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Jan 2021 23:42:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 22 Jan 2021 23:42:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Jan 2021 23:42:14 GMT
WORKDIR /home/gradle
# Fri, 22 Jan 2021 23:42:55 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Jan 2021 23:42:58 GMT
ENV GRADLE_VERSION=6.7.1
# Fri, 22 Jan 2021 23:42:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Fri, 22 Jan 2021 23:43:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eb1c97ba788e270b378124267517bf53f4c0ff1c878458a207cd3d91bf7e6d`  
		Last Modified: Thu, 21 Jan 2021 05:20:39 GMT  
		Size: 104.1 MB (104058940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8284a4907e4bae67ee57ee246fea5e5ce973907009530995744dccde5e56c9e`  
		Last Modified: Fri, 22 Jan 2021 23:49:19 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc4c50b2ad8ea83d860667bc0b3b75295ff93173c4c17d9c3a472b400e14650`  
		Last Modified: Fri, 22 Jan 2021 23:49:38 GMT  
		Size: 65.3 MB (65301897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6950cdc9ca596f95ddbfbe4ec823837a5a9a69c0bd29953915bb3222e9e5e883`  
		Last Modified: Fri, 22 Jan 2021 23:49:30 GMT  
		Size: 102.9 MB (102851402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:0ca57b9024f5b1a3b2f93f6ce1823c4b1d1b8061cdaf3cf9fc28980f80f85ef3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334551513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996b1a60e7d09555d003e12abca4121dfa4a506f50b69f16847b030fde6db846`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 25 Nov 2020 22:22:45 GMT
ADD file:349669e872fc8d76ff551a3eb05bb336a7d13ef8d99dc4f7604d54fc263a1a40 in / 
# Wed, 25 Nov 2020 22:23:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:23:19 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:23:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:23:34 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:44:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 25 Nov 2020 22:46:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:46:22 GMT
ENV JAVA_VERSION=jdk8u275-b01
# Wed, 25 Nov 2020 22:46:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='aeade06192ce4544f998b4957cd2c0ed3f9f8eac08b0de5d2ed55c55283364af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u275b01.tar.gz';          ;;        armhf|armv7l)          ESUM='e2e41a8705061dfcc766bfb6b7edd4c699e94aac68e4deeb28c8e76734a46fb7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u275b01.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a7b1c803e581f226216f73aca878bfd1b149c422b63e42e64eeeecda78c2253b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u275b01.tar.gz';          ;;        s390x)          ESUM='f513b895d28bdc2011b698e4a9ee3ea524d0e7bb62d87b0f53814a326573ec04';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_s390x_linux_hotspot_8u275b01.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='06fb04075ed503013beb12ab87963b2ca36abe9e397a0c298a57c1d822467c29';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u275b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 25 Nov 2020 22:46:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Jan 2021 10:22:41 GMT
CMD ["gradle"]
# Wed, 13 Jan 2021 10:22:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Jan 2021 10:23:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 13 Jan 2021 10:23:09 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Jan 2021 10:23:12 GMT
WORKDIR /home/gradle
# Wed, 13 Jan 2021 10:26:11 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Wed, 13 Jan 2021 10:26:29 GMT
ENV GRADLE_VERSION=6.8
# Wed, 13 Jan 2021 10:26:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=e2774e6fb77c43657decde25542dea710aafd78c4022d19b196e7e78d79d8c6c
# Wed, 13 Jan 2021 10:27:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=e2774e6fb77c43657decde25542dea710aafd78c4022d19b196e7e78d79d8c6c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:0162c086f3047a91e0409b0f80e741887de3c5e5490b9be62d74a5c054c7d6b0`  
		Last Modified: Mon, 09 Nov 2020 19:03:51 GMT  
		Size: 33.3 MB (33278639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61108ece12882b4998d113ea62b7f4d286877fef610d4aae5b2d2f17d68bf8a4`  
		Last Modified: Wed, 25 Nov 2020 22:27:34 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92bd8a59839464b3f3c73564e77cb7f1868ac3e96fcc07c1a77b85c51ba1b1`  
		Last Modified: Wed, 25 Nov 2020 22:27:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0126056f0b80e5735fc6cef6d439c93c998a81a55e09f213e73e6a7ef1f8cca6`  
		Last Modified: Wed, 25 Nov 2020 23:16:22 GMT  
		Size: 17.2 MB (17210167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96aa886bb59ed9df147ab66f0ab1814cf56ae24409757022efd9d18a0d57bbf`  
		Last Modified: Wed, 25 Nov 2020 23:16:32 GMT  
		Size: 102.2 MB (102196112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f968479bd23339abf16ae7e85777603459f37e4d9ebbdc83c3cb8c4c0a8be9c`  
		Last Modified: Wed, 13 Jan 2021 11:12:35 GMT  
		Size: 4.4 KB (4371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a79629b73efe321034f9f2c6fab50237c33a20cf6f63b506959cd8c894b77bc`  
		Last Modified: Wed, 13 Jan 2021 11:13:50 GMT  
		Size: 74.0 MB (74000289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279a6f96d2fcfa53f8c241ef15d0f76fd95c19feb1dfb428f7b6675be05e5a80`  
		Last Modified: Wed, 13 Jan 2021 11:13:03 GMT  
		Size: 107.9 MB (107860892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jdk` - linux; s390x

```console
$ docker pull gradle@sha256:6ef0f7814d34f15b45ce1d67e7c7121bba4fbfdf6c39b1408e9ccbc5db173469
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310758113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f37e348acc6b1bde46b184b70f3da52b88be40714e5a535c327dbd40f8e5ab2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 21 Jan 2021 04:01:09 GMT
ADD file:563ee3423282dfe85d6f542f5274f4fbfb35eabdc30f82580c427458890f099a in / 
# Thu, 21 Jan 2021 04:01:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 04:01:17 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 04:01:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 04:01:20 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:43:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 04:43:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:43:36 GMT
ENV JAVA_VERSION=jdk8u275-b01
# Thu, 21 Jan 2021 04:43:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='aeade06192ce4544f998b4957cd2c0ed3f9f8eac08b0de5d2ed55c55283364af';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_aarch64_linux_hotspot_8u275b01.tar.gz';          ;;        armhf|armv7l)          ESUM='e2e41a8705061dfcc766bfb6b7edd4c699e94aac68e4deeb28c8e76734a46fb7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_arm_linux_hotspot_8u275b01.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a7b1c803e581f226216f73aca878bfd1b149c422b63e42e64eeeecda78c2253b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u275b01.tar.gz';          ;;        s390x)          ESUM='f513b895d28bdc2011b698e4a9ee3ea524d0e7bb62d87b0f53814a326573ec04';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_s390x_linux_hotspot_8u275b01.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='06fb04075ed503013beb12ab87963b2ca36abe9e397a0c298a57c1d822467c29';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_hotspot_8u275b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Jan 2021 04:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Jan 2021 23:41:37 GMT
CMD ["gradle"]
# Fri, 22 Jan 2021 23:41:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 Jan 2021 23:41:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 22 Jan 2021 23:41:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 Jan 2021 23:41:40 GMT
WORKDIR /home/gradle
# Fri, 22 Jan 2021 23:42:14 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Jan 2021 23:42:20 GMT
ENV GRADLE_VERSION=6.7.1
# Fri, 22 Jan 2021 23:42:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
# Fri, 22 Jan 2021 23:42:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3239b5ed86c3838a37d983ac100573f64c1f3fd8e1eb6c89fa5f9529b5ec091d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:413f11bd9d503955ec346fcc33cde226866284d10513c27bbbe8a1831e2649a9`  
		Last Modified: Thu, 21 Jan 2021 04:03:37 GMT  
		Size: 27.2 MB (27192128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8381373ef0ee1bc73cf24bd5471bd1d13cf3a5812c2f179d4fe27c969fdffa6`  
		Last Modified: Thu, 21 Jan 2021 04:03:32 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91bc19693304e44a85f335f09c970702b6985f60b1aef345ff1de9a951e89d`  
		Last Modified: Thu, 21 Jan 2021 04:03:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc824387b487764c99064d9c5a4131afb03651d6f120304f7bb31a1d339e9ec2`  
		Last Modified: Thu, 21 Jan 2021 05:07:22 GMT  
		Size: 15.7 MB (15749235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46fc18d13b02f1ded47ce97dd9a95017ce6506efd4a2483698a20b59664b5ec`  
		Last Modified: Thu, 21 Jan 2021 05:07:27 GMT  
		Size: 99.7 MB (99727592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63ac82ed154f050fd846fce85c1aed884297c3fd9a2fca9e77fc0b384981c0c`  
		Last Modified: Fri, 22 Jan 2021 23:53:50 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cbf017f2d17d8d1af5eec6fea2f21d46aed3756051bce98d31074020093629`  
		Last Modified: Fri, 22 Jan 2021 23:54:00 GMT  
		Size: 65.2 MB (65232360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157e90e8ad66c75b3399640ac5b27d59f798e7aecdbaaffd309175de1efb7d61`  
		Last Modified: Fri, 22 Jan 2021 23:53:56 GMT  
		Size: 102.9 MB (102851398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
