<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jruby`

-	[`jruby:9`](#jruby9)
-	[`jruby:9-jdk`](#jruby9-jdk)
-	[`jruby:9-jdk8`](#jruby9-jdk8)
-	[`jruby:9.2`](#jruby92)
-	[`jruby:9.2-jdk`](#jruby92-jdk)
-	[`jruby:9.2-jdk11`](#jruby92-jdk11)
-	[`jruby:9.2-jdk17`](#jruby92-jdk17)
-	[`jruby:9.2-jdk8`](#jruby92-jdk8)
-	[`jruby:9.2-jre`](#jruby92-jre)
-	[`jruby:9.2-jre11`](#jruby92-jre11)
-	[`jruby:9.2-jre8`](#jruby92-jre8)
-	[`jruby:9.2-onbuild`](#jruby92-onbuild)
-	[`jruby:9.2.21`](#jruby9221)
-	[`jruby:9.2.21-jdk`](#jruby9221-jdk)
-	[`jruby:9.2.21-jdk11`](#jruby9221-jdk11)
-	[`jruby:9.2.21-jdk17`](#jruby9221-jdk17)
-	[`jruby:9.2.21-jdk8`](#jruby9221-jdk8)
-	[`jruby:9.2.21-jre`](#jruby9221-jre)
-	[`jruby:9.2.21-jre11`](#jruby9221-jre11)
-	[`jruby:9.2.21-jre8`](#jruby9221-jre8)
-	[`jruby:9.2.21-onbuild`](#jruby9221-onbuild)
-	[`jruby:9.2.21.0`](#jruby92210)
-	[`jruby:9.2.21.0-jdk`](#jruby92210-jdk)
-	[`jruby:9.2.21.0-jdk11`](#jruby92210-jdk11)
-	[`jruby:9.2.21.0-jdk17`](#jruby92210-jdk17)
-	[`jruby:9.2.21.0-jdk8`](#jruby92210-jdk8)
-	[`jruby:9.2.21.0-jre`](#jruby92210-jre)
-	[`jruby:9.2.21.0-jre11`](#jruby92210-jre11)
-	[`jruby:9.2.21.0-jre8`](#jruby92210-jre8)
-	[`jruby:9.2.21.0-onbuild`](#jruby92210-onbuild)
-	[`jruby:9.3`](#jruby93)
-	[`jruby:9.3-jdk`](#jruby93-jdk)
-	[`jruby:9.3-jdk11`](#jruby93-jdk11)
-	[`jruby:9.3-jdk17`](#jruby93-jdk17)
-	[`jruby:9.3-jdk8`](#jruby93-jdk8)
-	[`jruby:9.3-jre`](#jruby93-jre)
-	[`jruby:9.3-jre11`](#jruby93-jre11)
-	[`jruby:9.3-jre8`](#jruby93-jre8)
-	[`jruby:9.3.6`](#jruby936)
-	[`jruby:9.3.6-jdk`](#jruby936-jdk)
-	[`jruby:9.3.6-jdk11`](#jruby936-jdk11)
-	[`jruby:9.3.6-jdk17`](#jruby936-jdk17)
-	[`jruby:9.3.6-jdk8`](#jruby936-jdk8)
-	[`jruby:9.3.6-jre`](#jruby936-jre)
-	[`jruby:9.3.6-jre11`](#jruby936-jre11)
-	[`jruby:9.3.6-jre8`](#jruby936-jre8)
-	[`jruby:9.3.6.0`](#jruby9360)
-	[`jruby:9.3.6.0-jdk`](#jruby9360-jdk)
-	[`jruby:9.3.6.0-jdk11`](#jruby9360-jdk11)
-	[`jruby:9.3.6.0-jdk17`](#jruby9360-jdk17)
-	[`jruby:9.3.6.0-jdk8`](#jruby9360-jdk8)
-	[`jruby:9.3.6.0-jre`](#jruby9360-jre)
-	[`jruby:9.3.6.0-jre11`](#jruby9360-jre11)
-	[`jruby:9.3.6.0-jre8`](#jruby9360-jre8)
-	[`jruby:latest`](#jrubylatest)

## `jruby:9`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9-jdk8`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk`

```console
$ docker pull jruby@sha256:bbf0d7a8e5cf901db6f5a4a4e4b01419f010f8fd9ba98dacfb8fa8b13a5da407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:83bd46bc5ad4e2e8465d55508b02a42b34fccbfa4f16ed42d6c63ce1d09cea0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9580643193cce88981f5b7423f5e20db6fe641a67055c0815a1e1ede4559cb2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk11`

```console
$ docker pull jruby@sha256:06fea99bd971e1dd002c15ace2983a3c590f7b4669c83f57ed29f11664c0ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:cf22407424c3e3bcf0758de3dabab8d5ebe9ed64757e165185f0a3fd3d470d82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275021069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e6b29f1e98dd2659463d7d16d4d38b17571ade217b3caf954093760568bf1c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:48 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:20 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:16 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:17 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:18 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:19 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:28 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2e6d883cf01d8e0aeb6c47ad7b199a5767baced34436206516ac656a6cb9ec`  
		Last Modified: Thu, 28 Jul 2022 16:25:58 GMT  
		Size: 194.6 MB (194596372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a91c929b0df6dce394e88b82b4d965bc5ff1924ef7852a4af933c6e3f10ac2`  
		Last Modified: Thu, 28 Jul 2022 16:25:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a001865da21fbb93727fbdda8150bb6dc8fa56314bfc149e38582c85cff87`  
		Last Modified: Thu, 28 Jul 2022 18:57:03 GMT  
		Size: 6.9 MB (6919206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d161e4bcce7e61fdae09c0e7c4df084820670f721f4f9666988c2a0b0e8ea8`  
		Last Modified: Thu, 28 Jul 2022 18:57:53 GMT  
		Size: 27.8 MB (27844776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ce1b23464b3650d4d145376a5061de80e1029f815eb2e5e5d03959708f2db`  
		Last Modified: Thu, 28 Jul 2022 18:57:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7547d01b72d7631005528d705c6e3b22c13e3734bb9997c8a69d6f45bb6d95f`  
		Last Modified: Thu, 28 Jul 2022 18:57:51 GMT  
		Size: 1.1 MB (1057725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cee7c189b13d7419bccdfcab1bb58863044059952ef8bf59fb56cb27745a6`  
		Last Modified: Thu, 28 Jul 2022 18:57:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk17`

```console
$ docker pull jruby@sha256:741b57345db5c93b9a4b568d8e64dd389af86f0c85d1a9aca3fe03c343578fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:12a60dbcc66ac564923b84b5fc3965ab41dcd04bf3c87db1077f34e5eb8678ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276318983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0fce4af66619bab6ac82747a43593592d6b327eff2179a04f2e77ecad9e40a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:18 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:40 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:33 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:33 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:36 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:44 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:45 GMT
CMD ["irb"]
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
	-	`sha256:33710839ca3af3d6a583c0b8b9091270cf89851f5c03fc9d15f43645e5745551`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 192.1 MB (192148048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63208a3f8de08e4ec3b0e482f7b081a286a8a9f77ab1193c240a27a76e1df5cb`  
		Last Modified: Thu, 28 Jul 2022 16:28:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a02878cb7ad506085ffbc02c445a230fe1ac5526133ab9c3bac12d40952ca`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 6.9 MB (6921399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd6c32c9b486464b36832d56da33035f2d5f3d34ad470aa08a11ec0cfbca16`  
		Last Modified: Thu, 28 Jul 2022 18:58:08 GMT  
		Size: 27.8 MB (27844769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e34d7c48f719bec1f7e5bed843465657e657e7cb524e2022d9cfadb0c99ef1b`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8f16e7c7718402d347a3dbafd48bb5ec711f405578d3699468acc39b4705f`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 1.1 MB (1057691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c30b7e84b22a21137c15dbbaffcea112371c596d5bcdf682bbe287c9b64c13`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk8`

```console
$ docker pull jruby@sha256:bbf0d7a8e5cf901db6f5a4a4e4b01419f010f8fd9ba98dacfb8fa8b13a5da407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:83bd46bc5ad4e2e8465d55508b02a42b34fccbfa4f16ed42d6c63ce1d09cea0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9580643193cce88981f5b7423f5e20db6fe641a67055c0815a1e1ede4559cb2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre11`

```console
$ docker pull jruby@sha256:2063b708daa5643b3c8ff4c6f5609925dad1db285dd420035a2963b66eb79885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:21cbf603d78dc5b90665dbfc7a502aaa7b5437f8d80f5eeb3bb2647bf08fd46f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123941539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87fb51980bc7078908986366884539ec56f786d2e48e206f369b386c6358305`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:53:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:00 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:00 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:11 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae92f358c70d8fd806258a568ab6bb0581b12b2639e6e623506e2162f7900e`  
		Last Modified: Thu, 28 Jul 2022 16:27:27 GMT  
		Size: 43.5 MB (43516900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc8255dbec5821a13865484e05618c120f38a534deecf3bd28da1262315c41c`  
		Last Modified: Thu, 28 Jul 2022 16:27:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b321cf2d70fe77791d06b01472db4261d8f61c04367911cbf028e5c0eb8c2`  
		Last Modified: Thu, 28 Jul 2022 18:56:48 GMT  
		Size: 6.9 MB (6919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feabf082c9ce501d3f7a884cd8b183728764984a7b1222f1e8c6852353e7096b`  
		Last Modified: Thu, 28 Jul 2022 18:57:38 GMT  
		Size: 27.8 MB (27844725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c856a7aa119c79ba75a579ed4f6f968f53ed107bde4f91524b080d8ad15ae`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0fa72ef1f408f4905d4dcdc4a91931a44986f85192fc5e0aaeaa604c3d319`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 1.1 MB (1057713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a9661a11a7dfb8904ff3e30767edddc22f4d9ca1196c06e88d0d3cf0b90673`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jre8`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-onbuild`

```console
$ docker pull jruby@sha256:f80ab6c6a30153a08a9e144c18f413938c041aa7ed445e89ad9c95cf8b5c2036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:e5f0a76892beb8711e7ace1469a7a7b6e7f723383ada9cc3cd638325c94db94f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e8aea948061d7f961d07a6e636660ec09ce933887a9b43e00bbfbdfbd4625`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
# Thu, 30 Jun 2022 19:10:32 GMT
RUN mkdir -p /usr/src/app
# Thu, 30 Jun 2022 19:10:32 GMT
WORKDIR /usr/src/app
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD RUN bundle install --system
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d4e53e1452baf4ee408a11a0a71725d724d4bc29b327efce66f109e93d235`  
		Last Modified: Thu, 30 Jun 2022 19:15:34 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk`

```console
$ docker pull jruby@sha256:bbf0d7a8e5cf901db6f5a4a4e4b01419f010f8fd9ba98dacfb8fa8b13a5da407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:83bd46bc5ad4e2e8465d55508b02a42b34fccbfa4f16ed42d6c63ce1d09cea0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9580643193cce88981f5b7423f5e20db6fe641a67055c0815a1e1ede4559cb2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk11`

```console
$ docker pull jruby@sha256:06fea99bd971e1dd002c15ace2983a3c590f7b4669c83f57ed29f11664c0ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:cf22407424c3e3bcf0758de3dabab8d5ebe9ed64757e165185f0a3fd3d470d82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275021069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e6b29f1e98dd2659463d7d16d4d38b17571ade217b3caf954093760568bf1c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:48 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:20 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:16 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:17 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:18 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:19 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:28 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2e6d883cf01d8e0aeb6c47ad7b199a5767baced34436206516ac656a6cb9ec`  
		Last Modified: Thu, 28 Jul 2022 16:25:58 GMT  
		Size: 194.6 MB (194596372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a91c929b0df6dce394e88b82b4d965bc5ff1924ef7852a4af933c6e3f10ac2`  
		Last Modified: Thu, 28 Jul 2022 16:25:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a001865da21fbb93727fbdda8150bb6dc8fa56314bfc149e38582c85cff87`  
		Last Modified: Thu, 28 Jul 2022 18:57:03 GMT  
		Size: 6.9 MB (6919206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d161e4bcce7e61fdae09c0e7c4df084820670f721f4f9666988c2a0b0e8ea8`  
		Last Modified: Thu, 28 Jul 2022 18:57:53 GMT  
		Size: 27.8 MB (27844776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ce1b23464b3650d4d145376a5061de80e1029f815eb2e5e5d03959708f2db`  
		Last Modified: Thu, 28 Jul 2022 18:57:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7547d01b72d7631005528d705c6e3b22c13e3734bb9997c8a69d6f45bb6d95f`  
		Last Modified: Thu, 28 Jul 2022 18:57:51 GMT  
		Size: 1.1 MB (1057725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cee7c189b13d7419bccdfcab1bb58863044059952ef8bf59fb56cb27745a6`  
		Last Modified: Thu, 28 Jul 2022 18:57:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk17`

```console
$ docker pull jruby@sha256:741b57345db5c93b9a4b568d8e64dd389af86f0c85d1a9aca3fe03c343578fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:12a60dbcc66ac564923b84b5fc3965ab41dcd04bf3c87db1077f34e5eb8678ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276318983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0fce4af66619bab6ac82747a43593592d6b327eff2179a04f2e77ecad9e40a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:18 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:40 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:33 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:33 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:36 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:44 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:45 GMT
CMD ["irb"]
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
	-	`sha256:33710839ca3af3d6a583c0b8b9091270cf89851f5c03fc9d15f43645e5745551`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 192.1 MB (192148048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63208a3f8de08e4ec3b0e482f7b081a286a8a9f77ab1193c240a27a76e1df5cb`  
		Last Modified: Thu, 28 Jul 2022 16:28:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a02878cb7ad506085ffbc02c445a230fe1ac5526133ab9c3bac12d40952ca`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 6.9 MB (6921399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd6c32c9b486464b36832d56da33035f2d5f3d34ad470aa08a11ec0cfbca16`  
		Last Modified: Thu, 28 Jul 2022 18:58:08 GMT  
		Size: 27.8 MB (27844769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e34d7c48f719bec1f7e5bed843465657e657e7cb524e2022d9cfadb0c99ef1b`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8f16e7c7718402d347a3dbafd48bb5ec711f405578d3699468acc39b4705f`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 1.1 MB (1057691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c30b7e84b22a21137c15dbbaffcea112371c596d5bcdf682bbe287c9b64c13`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk8`

```console
$ docker pull jruby@sha256:bbf0d7a8e5cf901db6f5a4a4e4b01419f010f8fd9ba98dacfb8fa8b13a5da407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:83bd46bc5ad4e2e8465d55508b02a42b34fccbfa4f16ed42d6c63ce1d09cea0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9580643193cce88981f5b7423f5e20db6fe641a67055c0815a1e1ede4559cb2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jre`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jre11`

```console
$ docker pull jruby@sha256:2063b708daa5643b3c8ff4c6f5609925dad1db285dd420035a2963b66eb79885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:21cbf603d78dc5b90665dbfc7a502aaa7b5437f8d80f5eeb3bb2647bf08fd46f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123941539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87fb51980bc7078908986366884539ec56f786d2e48e206f369b386c6358305`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:53:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:00 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:00 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:11 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae92f358c70d8fd806258a568ab6bb0581b12b2639e6e623506e2162f7900e`  
		Last Modified: Thu, 28 Jul 2022 16:27:27 GMT  
		Size: 43.5 MB (43516900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc8255dbec5821a13865484e05618c120f38a534deecf3bd28da1262315c41c`  
		Last Modified: Thu, 28 Jul 2022 16:27:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b321cf2d70fe77791d06b01472db4261d8f61c04367911cbf028e5c0eb8c2`  
		Last Modified: Thu, 28 Jul 2022 18:56:48 GMT  
		Size: 6.9 MB (6919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feabf082c9ce501d3f7a884cd8b183728764984a7b1222f1e8c6852353e7096b`  
		Last Modified: Thu, 28 Jul 2022 18:57:38 GMT  
		Size: 27.8 MB (27844725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c856a7aa119c79ba75a579ed4f6f968f53ed107bde4f91524b080d8ad15ae`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0fa72ef1f408f4905d4dcdc4a91931a44986f85192fc5e0aaeaa604c3d319`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 1.1 MB (1057713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a9661a11a7dfb8904ff3e30767edddc22f4d9ca1196c06e88d0d3cf0b90673`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jre8`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-onbuild`

```console
$ docker pull jruby@sha256:f80ab6c6a30153a08a9e144c18f413938c041aa7ed445e89ad9c95cf8b5c2036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:e5f0a76892beb8711e7ace1469a7a7b6e7f723383ada9cc3cd638325c94db94f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e8aea948061d7f961d07a6e636660ec09ce933887a9b43e00bbfbdfbd4625`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
# Thu, 30 Jun 2022 19:10:32 GMT
RUN mkdir -p /usr/src/app
# Thu, 30 Jun 2022 19:10:32 GMT
WORKDIR /usr/src/app
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD RUN bundle install --system
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d4e53e1452baf4ee408a11a0a71725d724d4bc29b327efce66f109e93d235`  
		Last Modified: Thu, 30 Jun 2022 19:15:34 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk`

```console
$ docker pull jruby@sha256:bbf0d7a8e5cf901db6f5a4a4e4b01419f010f8fd9ba98dacfb8fa8b13a5da407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:83bd46bc5ad4e2e8465d55508b02a42b34fccbfa4f16ed42d6c63ce1d09cea0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9580643193cce88981f5b7423f5e20db6fe641a67055c0815a1e1ede4559cb2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk11`

```console
$ docker pull jruby@sha256:06fea99bd971e1dd002c15ace2983a3c590f7b4669c83f57ed29f11664c0ee15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:cf22407424c3e3bcf0758de3dabab8d5ebe9ed64757e165185f0a3fd3d470d82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275021069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e6b29f1e98dd2659463d7d16d4d38b17571ade217b3caf954093760568bf1c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:48 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:20 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:16 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:17 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:18 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:19 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:28 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2e6d883cf01d8e0aeb6c47ad7b199a5767baced34436206516ac656a6cb9ec`  
		Last Modified: Thu, 28 Jul 2022 16:25:58 GMT  
		Size: 194.6 MB (194596372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a91c929b0df6dce394e88b82b4d965bc5ff1924ef7852a4af933c6e3f10ac2`  
		Last Modified: Thu, 28 Jul 2022 16:25:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a001865da21fbb93727fbdda8150bb6dc8fa56314bfc149e38582c85cff87`  
		Last Modified: Thu, 28 Jul 2022 18:57:03 GMT  
		Size: 6.9 MB (6919206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d161e4bcce7e61fdae09c0e7c4df084820670f721f4f9666988c2a0b0e8ea8`  
		Last Modified: Thu, 28 Jul 2022 18:57:53 GMT  
		Size: 27.8 MB (27844776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ce1b23464b3650d4d145376a5061de80e1029f815eb2e5e5d03959708f2db`  
		Last Modified: Thu, 28 Jul 2022 18:57:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7547d01b72d7631005528d705c6e3b22c13e3734bb9997c8a69d6f45bb6d95f`  
		Last Modified: Thu, 28 Jul 2022 18:57:51 GMT  
		Size: 1.1 MB (1057725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cee7c189b13d7419bccdfcab1bb58863044059952ef8bf59fb56cb27745a6`  
		Last Modified: Thu, 28 Jul 2022 18:57:50 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk17`

```console
$ docker pull jruby@sha256:741b57345db5c93b9a4b568d8e64dd389af86f0c85d1a9aca3fe03c343578fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:12a60dbcc66ac564923b84b5fc3965ab41dcd04bf3c87db1077f34e5eb8678ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276318983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0fce4af66619bab6ac82747a43593592d6b327eff2179a04f2e77ecad9e40a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:18 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:40 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:33 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:33 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:35 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:35 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:36 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:44 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:44 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:45 GMT
CMD ["irb"]
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
	-	`sha256:33710839ca3af3d6a583c0b8b9091270cf89851f5c03fc9d15f43645e5745551`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 192.1 MB (192148048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63208a3f8de08e4ec3b0e482f7b081a286a8a9f77ab1193c240a27a76e1df5cb`  
		Last Modified: Thu, 28 Jul 2022 16:28:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a02878cb7ad506085ffbc02c445a230fe1ac5526133ab9c3bac12d40952ca`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 6.9 MB (6921399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd6c32c9b486464b36832d56da33035f2d5f3d34ad470aa08a11ec0cfbca16`  
		Last Modified: Thu, 28 Jul 2022 18:58:08 GMT  
		Size: 27.8 MB (27844769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e34d7c48f719bec1f7e5bed843465657e657e7cb524e2022d9cfadb0c99ef1b`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc8f16e7c7718402d347a3dbafd48bb5ec711f405578d3699468acc39b4705f`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 1.1 MB (1057691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c30b7e84b22a21137c15dbbaffcea112371c596d5bcdf682bbe287c9b64c13`  
		Last Modified: Thu, 28 Jul 2022 18:58:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk8`

```console
$ docker pull jruby@sha256:bbf0d7a8e5cf901db6f5a4a4e4b01419f010f8fd9ba98dacfb8fa8b13a5da407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:83bd46bc5ad4e2e8465d55508b02a42b34fccbfa4f16ed42d6c63ce1d09cea0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9580643193cce88981f5b7423f5e20db6fe641a67055c0815a1e1ede4559cb2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jre`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jre11`

```console
$ docker pull jruby@sha256:2063b708daa5643b3c8ff4c6f5609925dad1db285dd420035a2963b66eb79885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:21cbf603d78dc5b90665dbfc7a502aaa7b5437f8d80f5eeb3bb2647bf08fd46f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123941539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87fb51980bc7078908986366884539ec56f786d2e48e206f369b386c6358305`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:53:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:55:00 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 28 Jul 2022 18:55:00 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 28 Jul 2022 18:55:02 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:55:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:03 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:55:11 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:55:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:55:12 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:55:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:55:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae92f358c70d8fd806258a568ab6bb0581b12b2639e6e623506e2162f7900e`  
		Last Modified: Thu, 28 Jul 2022 16:27:27 GMT  
		Size: 43.5 MB (43516900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc8255dbec5821a13865484e05618c120f38a534deecf3bd28da1262315c41c`  
		Last Modified: Thu, 28 Jul 2022 16:27:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b321cf2d70fe77791d06b01472db4261d8f61c04367911cbf028e5c0eb8c2`  
		Last Modified: Thu, 28 Jul 2022 18:56:48 GMT  
		Size: 6.9 MB (6919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feabf082c9ce501d3f7a884cd8b183728764984a7b1222f1e8c6852353e7096b`  
		Last Modified: Thu, 28 Jul 2022 18:57:38 GMT  
		Size: 27.8 MB (27844725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c856a7aa119c79ba75a579ed4f6f968f53ed107bde4f91524b080d8ad15ae`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a0fa72ef1f408f4905d4dcdc4a91931a44986f85192fc5e0aaeaa604c3d319`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 1.1 MB (1057713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a9661a11a7dfb8904ff3e30767edddc22f4d9ca1196c06e88d0d3cf0b90673`  
		Last Modified: Thu, 28 Jul 2022 18:57:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jre8`

```console
$ docker pull jruby@sha256:ded8f2c5812ae73bfdf9aa0fda6da0c6ea7c6c7de2fac9733c110dea2777cf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:7a18aab25b73f3aeb95de0931c2f287bd81a4d2e36bb883578e63d3afed056b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37e4d1beb7d8ee87727b42506b1ab698ea628efce47ae3a8870503e38ab0891`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:21 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:23 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:23 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:24 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:31 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c9bb876cf7a8f32e06f0e5b860a6f0d5f3b6cd1a6551012fccd9ed06a9172d`  
		Last Modified: Thu, 30 Jun 2022 19:13:43 GMT  
		Size: 27.8 MB (27844750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8197e77bd1ef985ffea72146a6164f507b798460dc5a76c32cfb8fbe02d0a`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9fe08a5f76813e4b83967f45e47362ca0d2c5e83b49d1586d591af391b557`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 1.1 MB (1053874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587c94f5aa8e602c61d52ac75da0d9eb5faf9cb68cbaab6852920efcf6b1c4b`  
		Last Modified: Thu, 30 Jun 2022 19:13:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-onbuild`

```console
$ docker pull jruby@sha256:f80ab6c6a30153a08a9e144c18f413938c041aa7ed445e89ad9c95cf8b5c2036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-onbuild` - linux; amd64

```console
$ docker pull jruby@sha256:e5f0a76892beb8711e7ace1469a7a7b6e7f723383ada9cc3cd638325c94db94f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183922202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e8aea948061d7f961d07a6e636660ec09ce933887a9b43e00bbfbdfbd4625`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:35 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:36 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:37 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:38 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:38 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:45 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:46 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:46 GMT
CMD ["irb"]
# Thu, 30 Jun 2022 19:10:32 GMT
RUN mkdir -p /usr/src/app
# Thu, 30 Jun 2022 19:10:32 GMT
WORKDIR /usr/src/app
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD Gemfile /usr/src/app/
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD Gemfile.lock /usr/src/app/
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD RUN bundle install --system
# Thu, 30 Jun 2022 19:10:32 GMT
ONBUILD ADD . /usr/src/app
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc98dcff1acc47c4040f9e99adf817aae08d9eb750fbf87e16019e94a47624`  
		Last Modified: Thu, 30 Jun 2022 19:14:19 GMT  
		Size: 27.8 MB (27844682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2efef13db13d11a623d5bb2de738ea6310a4c83547b7bac7aa6aa45a10eb28f`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043207aadfc65e4ec94448819f84aa8d708cdc3d0079a850d3fa432ee564933`  
		Last Modified: Thu, 30 Jun 2022 19:14:18 GMT  
		Size: 1.1 MB (1053884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb81d817dbf5dfa94b67f4a1f11ceb3a5e905654fcf857239e5e820c48fc0d1`  
		Last Modified: Thu, 30 Jun 2022 19:14:17 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d4e53e1452baf4ee408a11a0a71725d724d4bc29b327efce66f109e93d235`  
		Last Modified: Thu, 30 Jun 2022 19:15:34 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk11`

```console
$ docker pull jruby@sha256:9adca99934adf9c243a675bc08fa0b83c806582b525c5d4422ce2d3e8abe1633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:6a4cb954416341cc00867fa5d2dc4638ef637bf6980c35d3b247cefceda8bcde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274960066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d67a0675036cffc211928183823977344b4a05395f9948018bef1899f63ab8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:48 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:20 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:54:20 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:54:20 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:54:22 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:54:22 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:23 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2e6d883cf01d8e0aeb6c47ad7b199a5767baced34436206516ac656a6cb9ec`  
		Last Modified: Thu, 28 Jul 2022 16:25:58 GMT  
		Size: 194.6 MB (194596372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a91c929b0df6dce394e88b82b4d965bc5ff1924ef7852a4af933c6e3f10ac2`  
		Last Modified: Thu, 28 Jul 2022 16:25:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a001865da21fbb93727fbdda8150bb6dc8fa56314bfc149e38582c85cff87`  
		Last Modified: Thu, 28 Jul 2022 18:57:03 GMT  
		Size: 6.9 MB (6919206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d71338f9e9dddf2f405c2a7aa0a01008251f76ec18c2b6c3616b07240b35b`  
		Last Modified: Thu, 28 Jul 2022 18:57:04 GMT  
		Size: 27.8 MB (27783657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e6e4e8dd92f329c0fc99a0be84fb3e9019ef73b09ef7fe2e7cc8ec0d63179`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15beb835c34d47f3d196cb2345b4ea03eedb9b25b5dc58cd71cb06f523ca5b33`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 1.1 MB (1057842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0717b9cd9f6fcaab7bb642b9f2f0c583aaa4cab60f2856956de4cf3733a032`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:85186602d4fe3bc8a54405d259bade7f7271e3b51e584f5b6b8a3ff6dfbec12f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268921251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bb53fe47d9203b55ddc75f2836cde199c4d9417b4509fb30c59956d1dda12a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:40:28 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:40:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:40:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:40:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:40:51 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:26:17 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:26:17 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:26:18 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:26:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:26:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:26:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:26:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:26:35 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:26:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6506e159034fee1c9c5a8ab6169a498314a95d33040238322509ba026455e06`  
		Last Modified: Thu, 28 Jul 2022 15:47:18 GMT  
		Size: 191.3 MB (191349052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5c7c2568d079761556493212537d33a0c5187879187be6fbfef1cd81092f5`  
		Last Modified: Thu, 28 Jul 2022 15:47:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52541c5689068c98b03333e1e8274eb7dc41c49e625fee4969f1a0be3bcc315b`  
		Last Modified: Thu, 28 Jul 2022 18:28:41 GMT  
		Size: 5.6 MB (5643407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ad62424d62b3b0617b95cd06d0ef7401d12b13047d7a5fad788c4abed0aa7f`  
		Last Modified: Thu, 28 Jul 2022 18:28:43 GMT  
		Size: 27.8 MB (27782138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312093d126504ccf4985e51964f12d2448bc121ad6cc90f76cc9c8c4b501e49b`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e3a46a46207ef9373c51050383d134179ef403233ea79e033051f47c9c44b`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 1.1 MB (1056678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148ad7acdf6e77f8710e757db8409987f12ebd33033917cb5303a87eb345d11c`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:014fb82234ce34f0ae3d0ccc86ea6f3c5bfaa0655315cf7a99fa8c6b38e842eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:486c1fb4b643acd67adff255365398ba28f7c2901f1cb36c3be4437ffd82edca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6107f5b59c98052d56ef0afd2d8804c875ca9fb3c883f7b45076d753351ed8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:18 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:40 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:54:40 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:54:40 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:54:42 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:54:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:43 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:52 GMT
CMD ["irb"]
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
	-	`sha256:33710839ca3af3d6a583c0b8b9091270cf89851f5c03fc9d15f43645e5745551`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 192.1 MB (192148048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63208a3f8de08e4ec3b0e482f7b081a286a8a9f77ab1193c240a27a76e1df5cb`  
		Last Modified: Thu, 28 Jul 2022 16:28:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a02878cb7ad506085ffbc02c445a230fe1ac5526133ab9c3bac12d40952ca`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 6.9 MB (6921399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd14a8c7b8e38988642fac076db7ffd708356ee75530e977eee4ecfc05d43764`  
		Last Modified: Thu, 28 Jul 2022 18:57:18 GMT  
		Size: 27.8 MB (27783639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7775abc81c7590b45e7481a004af1510b5afc8a67dbf321bb224963f719aaec`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2130237871d98660e4f0ec91d2c864afaa4a8960395f7ed503c690559659a29f`  
		Last Modified: Thu, 28 Jul 2022 18:57:16 GMT  
		Size: 1.1 MB (1057815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f766c0f7f3606a609b946230700ef5d81a35a5e7e044149a00079d0fc44eb9`  
		Last Modified: Thu, 28 Jul 2022 18:57:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:89012e28407558eb48306f97c5ac8aad97e8271203ef7f929f9deafb793496fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273083831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f98b82087cafff3783d57b255d7c2091e6591b9c24cd66001966b99a8aab6a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:06:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:42:26 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 15:42:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:42:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:42:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:42:43 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:26:51 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:26:52 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:26:53 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:26:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:26:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:57 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:27:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:27:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:27:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:27:09 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:27:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:27:11 GMT
CMD ["irb"]
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
	-	`sha256:c6f7993b64acbce351829c6e6a27b6e4a9d233c87677bc1888b559919f2c3ef0`  
		Last Modified: Thu, 28 Jul 2022 15:49:53 GMT  
		Size: 190.9 MB (190907077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f84f0e84ea8ee0a99694b37caca7c57efa0e20ab74cfdaf72ecdee6e0af1c4`  
		Last Modified: Thu, 28 Jul 2022 15:49:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377403c626d6dea12c7be7a25fee3cbaf145852fbf551a789312e57be3612610`  
		Last Modified: Thu, 28 Jul 2022 18:28:58 GMT  
		Size: 5.6 MB (5645306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df750d180b9ef6ef244839de2b289d7570a5b1f552bfb39a450f81b874507230`  
		Last Modified: Thu, 28 Jul 2022 18:29:00 GMT  
		Size: 27.8 MB (27782103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c2e8cb7cdf3a91e2b6d2670f94bec5f72a14b74c7dc4f074cb90500794ef79`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959b9460898145a4ca4117ccacb5774ef314a1b24e7c36bc8d7ca197f39d17cb`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 1.1 MB (1056683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28b3e4f9290bd836dea77f85c11df28e3ce9916f00fe48cf1379a43adf64d66`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk8`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre11`

```console
$ docker pull jruby@sha256:8c0fa63b01ca40075c1416e7569f79d7d4e7aba78ce38df1c16095441734db51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:2185f434305756941ca6e894c6fbb4a5170635e8b22fb42506e8bdfd67e489b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123880539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0173f3a956e44fcdc7ac98e2659c40e0aee1502cf003270b8b59ad775b8ebc`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:53:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:53:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:53:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:53:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:53:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:09 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae92f358c70d8fd806258a568ab6bb0581b12b2639e6e623506e2162f7900e`  
		Last Modified: Thu, 28 Jul 2022 16:27:27 GMT  
		Size: 43.5 MB (43516900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc8255dbec5821a13865484e05618c120f38a534deecf3bd28da1262315c41c`  
		Last Modified: Thu, 28 Jul 2022 16:27:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b321cf2d70fe77791d06b01472db4261d8f61c04367911cbf028e5c0eb8c2`  
		Last Modified: Thu, 28 Jul 2022 18:56:48 GMT  
		Size: 6.9 MB (6919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29f95a5af7ec22468bca73b4e5a1c242481b60d7b7554e412548ebf32b6d95d`  
		Last Modified: Thu, 28 Jul 2022 18:56:49 GMT  
		Size: 27.8 MB (27783615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f91076c950f202fad3fe5f0690995a1e0ba0b864f1cf6139c6f974d9a03c4`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda039f6be64c2cf18f6a2a4dc38b2fd55edd44f47ac6d75bda1606e3518aa67`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 1.1 MB (1057824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd99ae721f03e5be60281d72991e6829cf3423d224dd88f1737a3877de7bdbb`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:e3ee8ca2776f988158f6908731065a97af4bcf204e368b2654d62c5bbdd64907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119418771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae17aefbc9a1c019419748c63f2a8464558bb8d595e552cd1459634e50a325`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:40:28 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:41:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:41:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:25:39 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:25:40 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:25:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:25:43 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:25:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:25:55 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:25:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:25:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:25:57 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:25:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:25:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417e8638aad07f61e7c9047910d97970c246439035ead3a991fab7760e489b8`  
		Last Modified: Thu, 28 Jul 2022 15:48:51 GMT  
		Size: 41.8 MB (41846560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c060d7aa2dde1ab42563f6114cc26f12f075abcf4159fa4c0a3db98287c701`  
		Last Modified: Thu, 28 Jul 2022 15:48:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781cdbf7395858245a361b3f499b94d67201d2578f61954177d6f2d36f41ffaf`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 5.6 MB (5643403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4a6a243373d326b702e2f36a58fa5ec01315d6cdae00b009cc48f11932ca9a`  
		Last Modified: Thu, 28 Jul 2022 18:28:25 GMT  
		Size: 27.8 MB (27782127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85acf0a98ce53abb9571a69a0b06de9f8f2a03da0969f9105a4a0d4770d1652`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4b9ce72335676149f5ca6049ad402e0153aede52bffc3c1135ec36cdbd739a`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 1.1 MB (1056702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad241adc57c31cb2b7fded82b022a42a0b29868c7717a97e3e65c0b2d66bdf0f`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jre8`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jdk`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jdk11`

```console
$ docker pull jruby@sha256:9adca99934adf9c243a675bc08fa0b83c806582b525c5d4422ce2d3e8abe1633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:6a4cb954416341cc00867fa5d2dc4638ef637bf6980c35d3b247cefceda8bcde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274960066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d67a0675036cffc211928183823977344b4a05395f9948018bef1899f63ab8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:48 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:20 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:54:20 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:54:20 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:54:22 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:54:22 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:23 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2e6d883cf01d8e0aeb6c47ad7b199a5767baced34436206516ac656a6cb9ec`  
		Last Modified: Thu, 28 Jul 2022 16:25:58 GMT  
		Size: 194.6 MB (194596372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a91c929b0df6dce394e88b82b4d965bc5ff1924ef7852a4af933c6e3f10ac2`  
		Last Modified: Thu, 28 Jul 2022 16:25:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a001865da21fbb93727fbdda8150bb6dc8fa56314bfc149e38582c85cff87`  
		Last Modified: Thu, 28 Jul 2022 18:57:03 GMT  
		Size: 6.9 MB (6919206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d71338f9e9dddf2f405c2a7aa0a01008251f76ec18c2b6c3616b07240b35b`  
		Last Modified: Thu, 28 Jul 2022 18:57:04 GMT  
		Size: 27.8 MB (27783657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e6e4e8dd92f329c0fc99a0be84fb3e9019ef73b09ef7fe2e7cc8ec0d63179`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15beb835c34d47f3d196cb2345b4ea03eedb9b25b5dc58cd71cb06f523ca5b33`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 1.1 MB (1057842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0717b9cd9f6fcaab7bb642b9f2f0c583aaa4cab60f2856956de4cf3733a032`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:85186602d4fe3bc8a54405d259bade7f7271e3b51e584f5b6b8a3ff6dfbec12f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268921251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bb53fe47d9203b55ddc75f2836cde199c4d9417b4509fb30c59956d1dda12a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:40:28 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:40:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:40:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:40:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:40:51 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:26:17 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:26:17 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:26:18 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:26:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:26:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:26:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:26:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:26:35 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:26:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6506e159034fee1c9c5a8ab6169a498314a95d33040238322509ba026455e06`  
		Last Modified: Thu, 28 Jul 2022 15:47:18 GMT  
		Size: 191.3 MB (191349052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5c7c2568d079761556493212537d33a0c5187879187be6fbfef1cd81092f5`  
		Last Modified: Thu, 28 Jul 2022 15:47:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52541c5689068c98b03333e1e8274eb7dc41c49e625fee4969f1a0be3bcc315b`  
		Last Modified: Thu, 28 Jul 2022 18:28:41 GMT  
		Size: 5.6 MB (5643407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ad62424d62b3b0617b95cd06d0ef7401d12b13047d7a5fad788c4abed0aa7f`  
		Last Modified: Thu, 28 Jul 2022 18:28:43 GMT  
		Size: 27.8 MB (27782138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312093d126504ccf4985e51964f12d2448bc121ad6cc90f76cc9c8c4b501e49b`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e3a46a46207ef9373c51050383d134179ef403233ea79e033051f47c9c44b`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 1.1 MB (1056678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148ad7acdf6e77f8710e757db8409987f12ebd33033917cb5303a87eb345d11c`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jdk17`

```console
$ docker pull jruby@sha256:014fb82234ce34f0ae3d0ccc86ea6f3c5bfaa0655315cf7a99fa8c6b38e842eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:486c1fb4b643acd67adff255365398ba28f7c2901f1cb36c3be4437ffd82edca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6107f5b59c98052d56ef0afd2d8804c875ca9fb3c883f7b45076d753351ed8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:18 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:40 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:54:40 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:54:40 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:54:42 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:54:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:43 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:52 GMT
CMD ["irb"]
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
	-	`sha256:33710839ca3af3d6a583c0b8b9091270cf89851f5c03fc9d15f43645e5745551`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 192.1 MB (192148048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63208a3f8de08e4ec3b0e482f7b081a286a8a9f77ab1193c240a27a76e1df5cb`  
		Last Modified: Thu, 28 Jul 2022 16:28:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a02878cb7ad506085ffbc02c445a230fe1ac5526133ab9c3bac12d40952ca`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 6.9 MB (6921399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd14a8c7b8e38988642fac076db7ffd708356ee75530e977eee4ecfc05d43764`  
		Last Modified: Thu, 28 Jul 2022 18:57:18 GMT  
		Size: 27.8 MB (27783639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7775abc81c7590b45e7481a004af1510b5afc8a67dbf321bb224963f719aaec`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2130237871d98660e4f0ec91d2c864afaa4a8960395f7ed503c690559659a29f`  
		Last Modified: Thu, 28 Jul 2022 18:57:16 GMT  
		Size: 1.1 MB (1057815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f766c0f7f3606a609b946230700ef5d81a35a5e7e044149a00079d0fc44eb9`  
		Last Modified: Thu, 28 Jul 2022 18:57:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:89012e28407558eb48306f97c5ac8aad97e8271203ef7f929f9deafb793496fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273083831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f98b82087cafff3783d57b255d7c2091e6591b9c24cd66001966b99a8aab6a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:06:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:42:26 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 15:42:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:42:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:42:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:42:43 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:26:51 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:26:52 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:26:53 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:26:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:26:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:57 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:27:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:27:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:27:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:27:09 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:27:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:27:11 GMT
CMD ["irb"]
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
	-	`sha256:c6f7993b64acbce351829c6e6a27b6e4a9d233c87677bc1888b559919f2c3ef0`  
		Last Modified: Thu, 28 Jul 2022 15:49:53 GMT  
		Size: 190.9 MB (190907077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f84f0e84ea8ee0a99694b37caca7c57efa0e20ab74cfdaf72ecdee6e0af1c4`  
		Last Modified: Thu, 28 Jul 2022 15:49:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377403c626d6dea12c7be7a25fee3cbaf145852fbf551a789312e57be3612610`  
		Last Modified: Thu, 28 Jul 2022 18:28:58 GMT  
		Size: 5.6 MB (5645306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df750d180b9ef6ef244839de2b289d7570a5b1f552bfb39a450f81b874507230`  
		Last Modified: Thu, 28 Jul 2022 18:29:00 GMT  
		Size: 27.8 MB (27782103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c2e8cb7cdf3a91e2b6d2670f94bec5f72a14b74c7dc4f074cb90500794ef79`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959b9460898145a4ca4117ccacb5774ef314a1b24e7c36bc8d7ca197f39d17cb`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 1.1 MB (1056683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28b3e4f9290bd836dea77f85c11df28e3ce9916f00fe48cf1379a43adf64d66`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jdk8`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jre`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jre` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jre11`

```console
$ docker pull jruby@sha256:8c0fa63b01ca40075c1416e7569f79d7d4e7aba78ce38df1c16095441734db51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:2185f434305756941ca6e894c6fbb4a5170635e8b22fb42506e8bdfd67e489b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123880539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0173f3a956e44fcdc7ac98e2659c40e0aee1502cf003270b8b59ad775b8ebc`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:53:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:53:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:53:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:53:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:53:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:09 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae92f358c70d8fd806258a568ab6bb0581b12b2639e6e623506e2162f7900e`  
		Last Modified: Thu, 28 Jul 2022 16:27:27 GMT  
		Size: 43.5 MB (43516900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc8255dbec5821a13865484e05618c120f38a534deecf3bd28da1262315c41c`  
		Last Modified: Thu, 28 Jul 2022 16:27:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b321cf2d70fe77791d06b01472db4261d8f61c04367911cbf028e5c0eb8c2`  
		Last Modified: Thu, 28 Jul 2022 18:56:48 GMT  
		Size: 6.9 MB (6919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29f95a5af7ec22468bca73b4e5a1c242481b60d7b7554e412548ebf32b6d95d`  
		Last Modified: Thu, 28 Jul 2022 18:56:49 GMT  
		Size: 27.8 MB (27783615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f91076c950f202fad3fe5f0690995a1e0ba0b864f1cf6139c6f974d9a03c4`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda039f6be64c2cf18f6a2a4dc38b2fd55edd44f47ac6d75bda1606e3518aa67`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 1.1 MB (1057824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd99ae721f03e5be60281d72991e6829cf3423d224dd88f1737a3877de7bdbb`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:e3ee8ca2776f988158f6908731065a97af4bcf204e368b2654d62c5bbdd64907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119418771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae17aefbc9a1c019419748c63f2a8464558bb8d595e552cd1459634e50a325`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:40:28 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:41:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:41:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:25:39 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:25:40 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:25:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:25:43 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:25:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:25:55 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:25:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:25:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:25:57 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:25:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:25:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417e8638aad07f61e7c9047910d97970c246439035ead3a991fab7760e489b8`  
		Last Modified: Thu, 28 Jul 2022 15:48:51 GMT  
		Size: 41.8 MB (41846560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c060d7aa2dde1ab42563f6114cc26f12f075abcf4159fa4c0a3db98287c701`  
		Last Modified: Thu, 28 Jul 2022 15:48:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781cdbf7395858245a361b3f499b94d67201d2578f61954177d6f2d36f41ffaf`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 5.6 MB (5643403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4a6a243373d326b702e2f36a58fa5ec01315d6cdae00b009cc48f11932ca9a`  
		Last Modified: Thu, 28 Jul 2022 18:28:25 GMT  
		Size: 27.8 MB (27782127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85acf0a98ce53abb9571a69a0b06de9f8f2a03da0969f9105a4a0d4770d1652`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4b9ce72335676149f5ca6049ad402e0153aede52bffc3c1135ec36cdbd739a`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 1.1 MB (1056702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad241adc57c31cb2b7fded82b022a42a0b29868c7717a97e3e65c0b2d66bdf0f`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jre8`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jdk`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jdk11`

```console
$ docker pull jruby@sha256:9adca99934adf9c243a675bc08fa0b83c806582b525c5d4422ce2d3e8abe1633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:6a4cb954416341cc00867fa5d2dc4638ef637bf6980c35d3b247cefceda8bcde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274960066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d67a0675036cffc211928183823977344b4a05395f9948018bef1899f63ab8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:20:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:20:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:20:48 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:20 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:54:20 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:54:20 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:54:22 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:54:22 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:23 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:31 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:32 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:32 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2e6d883cf01d8e0aeb6c47ad7b199a5767baced34436206516ac656a6cb9ec`  
		Last Modified: Thu, 28 Jul 2022 16:25:58 GMT  
		Size: 194.6 MB (194596372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a91c929b0df6dce394e88b82b4d965bc5ff1924ef7852a4af933c6e3f10ac2`  
		Last Modified: Thu, 28 Jul 2022 16:25:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a001865da21fbb93727fbdda8150bb6dc8fa56314bfc149e38582c85cff87`  
		Last Modified: Thu, 28 Jul 2022 18:57:03 GMT  
		Size: 6.9 MB (6919206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d71338f9e9dddf2f405c2a7aa0a01008251f76ec18c2b6c3616b07240b35b`  
		Last Modified: Thu, 28 Jul 2022 18:57:04 GMT  
		Size: 27.8 MB (27783657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e6e4e8dd92f329c0fc99a0be84fb3e9019ef73b09ef7fe2e7cc8ec0d63179`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15beb835c34d47f3d196cb2345b4ea03eedb9b25b5dc58cd71cb06f523ca5b33`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 1.1 MB (1057842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0717b9cd9f6fcaab7bb642b9f2f0c583aaa4cab60f2856956de4cf3733a032`  
		Last Modified: Thu, 28 Jul 2022 18:57:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:85186602d4fe3bc8a54405d259bade7f7271e3b51e584f5b6b8a3ff6dfbec12f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268921251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bb53fe47d9203b55ddc75f2836cde199c4d9417b4509fb30c59956d1dda12a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:40:28 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:40:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:40:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:40:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:40:51 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:26:17 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:26:17 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:26:18 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:26:21 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:26:21 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:22 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:26:33 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:26:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:26:35 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:26:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6506e159034fee1c9c5a8ab6169a498314a95d33040238322509ba026455e06`  
		Last Modified: Thu, 28 Jul 2022 15:47:18 GMT  
		Size: 191.3 MB (191349052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5c7c2568d079761556493212537d33a0c5187879187be6fbfef1cd81092f5`  
		Last Modified: Thu, 28 Jul 2022 15:47:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52541c5689068c98b03333e1e8274eb7dc41c49e625fee4969f1a0be3bcc315b`  
		Last Modified: Thu, 28 Jul 2022 18:28:41 GMT  
		Size: 5.6 MB (5643407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ad62424d62b3b0617b95cd06d0ef7401d12b13047d7a5fad788c4abed0aa7f`  
		Last Modified: Thu, 28 Jul 2022 18:28:43 GMT  
		Size: 27.8 MB (27782138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312093d126504ccf4985e51964f12d2448bc121ad6cc90f76cc9c8c4b501e49b`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e3a46a46207ef9373c51050383d134179ef403233ea79e033051f47c9c44b`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 1.1 MB (1056678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148ad7acdf6e77f8710e757db8409987f12ebd33033917cb5303a87eb345d11c`  
		Last Modified: Thu, 28 Jul 2022 18:28:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jdk17`

```console
$ docker pull jruby@sha256:014fb82234ce34f0ae3d0ccc86ea6f3c5bfaa0655315cf7a99fa8c6b38e842eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:486c1fb4b643acd67adff255365398ba28f7c2901f1cb36c3be4437ffd82edca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276257976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6107f5b59c98052d56ef0afd2d8804c875ca9fb3c883f7b45076d753351ed8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:22:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:22:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:18 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:54:40 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:54:40 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:54:40 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:54:42 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:54:42 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:43 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:51 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:51 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:52 GMT
CMD ["irb"]
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
	-	`sha256:33710839ca3af3d6a583c0b8b9091270cf89851f5c03fc9d15f43645e5745551`  
		Last Modified: Thu, 28 Jul 2022 16:28:52 GMT  
		Size: 192.1 MB (192148048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63208a3f8de08e4ec3b0e482f7b081a286a8a9f77ab1193c240a27a76e1df5cb`  
		Last Modified: Thu, 28 Jul 2022 16:28:38 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28a02878cb7ad506085ffbc02c445a230fe1ac5526133ab9c3bac12d40952ca`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 6.9 MB (6921399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd14a8c7b8e38988642fac076db7ffd708356ee75530e977eee4ecfc05d43764`  
		Last Modified: Thu, 28 Jul 2022 18:57:18 GMT  
		Size: 27.8 MB (27783639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7775abc81c7590b45e7481a004af1510b5afc8a67dbf321bb224963f719aaec`  
		Last Modified: Thu, 28 Jul 2022 18:57:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2130237871d98660e4f0ec91d2c864afaa4a8960395f7ed503c690559659a29f`  
		Last Modified: Thu, 28 Jul 2022 18:57:16 GMT  
		Size: 1.1 MB (1057815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f766c0f7f3606a609b946230700ef5d81a35a5e7e044149a00079d0fc44eb9`  
		Last Modified: Thu, 28 Jul 2022 18:57:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:89012e28407558eb48306f97c5ac8aad97e8271203ef7f929f9deafb793496fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273083831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f98b82087cafff3783d57b255d7c2091e6591b9c24cd66001966b99a8aab6a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:06:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:42:26 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 15:42:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:42:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:42:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 15:42:43 GMT
CMD ["jshell"]
# Thu, 28 Jul 2022 18:26:51 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:26:52 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:26:53 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:26:55 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:26:56 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:26:57 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:27:07 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:27:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:27:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:27:09 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:27:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:27:11 GMT
CMD ["irb"]
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
	-	`sha256:c6f7993b64acbce351829c6e6a27b6e4a9d233c87677bc1888b559919f2c3ef0`  
		Last Modified: Thu, 28 Jul 2022 15:49:53 GMT  
		Size: 190.9 MB (190907077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f84f0e84ea8ee0a99694b37caca7c57efa0e20ab74cfdaf72ecdee6e0af1c4`  
		Last Modified: Thu, 28 Jul 2022 15:49:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377403c626d6dea12c7be7a25fee3cbaf145852fbf551a789312e57be3612610`  
		Last Modified: Thu, 28 Jul 2022 18:28:58 GMT  
		Size: 5.6 MB (5645306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df750d180b9ef6ef244839de2b289d7570a5b1f552bfb39a450f81b874507230`  
		Last Modified: Thu, 28 Jul 2022 18:29:00 GMT  
		Size: 27.8 MB (27782103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c2e8cb7cdf3a91e2b6d2670f94bec5f72a14b74c7dc4f074cb90500794ef79`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959b9460898145a4ca4117ccacb5774ef314a1b24e7c36bc8d7ca197f39d17cb`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 1.1 MB (1056683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28b3e4f9290bd836dea77f85c11df28e3ce9916f00fe48cf1379a43adf64d66`  
		Last Modified: Thu, 28 Jul 2022 18:28:57 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jdk8`

```console
$ docker pull jruby@sha256:09c4ec5f98c4143f6cd505177456bc85cb28fc774daef0a2e958ea1b330816ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jdk8` - linux; amd64

```console
$ docker pull jruby@sha256:bf5d713b2695fde38bc9a0b1bc5d45f4065f2cea446cc3f2869f7d156c729241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183860871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4512240013b3587af7c6baf1f56618ac4dd59bf315e144c926cadda846509aca`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:13:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:13:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:57 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:08 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d20e7eb18a115970d8e31de2a9c872267288773da6497427d9599ed831514d`  
		Last Modified: Tue, 07 Jun 2022 00:19:27 GMT  
		Size: 103.5 MB (103506651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a9defeaf1a778a43eb061f02eeadbcbcce20f07a55826c3018270b45f0a20a`  
		Last Modified: Tue, 07 Jun 2022 00:19:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d92f3a94ccace9619d3b1a66fbe1faace96740d9f76c03f2cbcd5a1e53ac691`  
		Last Modified: Thu, 30 Jun 2022 19:12:17 GMT  
		Size: 6.9 MB (6913829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393e3d7e1eb17041da08c96b1eb936ca82d65926871d8817150a7002d0cf85fb`  
		Last Modified: Thu, 30 Jun 2022 19:12:18 GMT  
		Size: 27.8 MB (27783413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07697d4dcc2d1ed496860d91c5ef81914a297e0a18d55b2d963220c2bf67e9d`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3949f3d1288230c8ffe2dadfdb3ef318eb43f4e87bc87cae08ed6a41f7f50`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5164d295240b685b4719e9f45fd85011c36958a5c5edaf94803bf4fa7e34d49`  
		Last Modified: Thu, 30 Jun 2022 19:12:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jdk8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:8bfea66fd963afea11a38f43d60d2d470120074610cee9450aba7711aac7b0f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180159788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440acbf82936e27fd64b5ebb29eeac9c702510ff5c38e04761a8c51b634cacc3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d10efb2afad3ed3d7bac9d3249cea77928aca6acb973cac0f90a2dd3606a3533';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='c914250a736e620c12f9fe65fcd94ffa1acdacc5323e5aaff611a33a37cd158f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='1df8c12fd97e76c388d64e4df16893f4285e000e6ff837d1e39969e5428aafa0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='adc13a0a0540d77f0a3481b48f10d61eb203e5ad4914507d489c2de3bd3d83da';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:34:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:09:09 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:09 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:10 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:13 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:13 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:14 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:09:25 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:09:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:09:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcece0580e10c416c1e7046a5470a31a642ce59eaf3a03ef9b31073f0fd3e91`  
		Last Modified: Tue, 07 Jun 2022 06:41:49 GMT  
		Size: 102.6 MB (102596127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c91f4a49be859828f6df357cf0f1808e1f6d00041b47ecc2e772bd926e536`  
		Last Modified: Tue, 07 Jun 2022 06:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660982d3c7e8c497f54bb855f8c5051ca4cdc3da55f3d23582ac4a1ec8ed5992`  
		Last Modified: Thu, 30 Jun 2022 20:13:05 GMT  
		Size: 5.6 MB (5638974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1eab6c0d1be9126f007b81d59151e392328216fb7c11124c37bca62313be5c`  
		Last Modified: Thu, 30 Jun 2022 20:13:06 GMT  
		Size: 27.8 MB (27781917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70132f7bfde1520dc8b92bf5c479764dd663a0b68c5aa5c4553123c9a6a8202`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93618464469473af7166a14faa06ea0ea9c7e459e9ecb93072566572f93087`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 1.1 MB (1052791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a8bb4caab52b79c2b80f12d4e597f61438b07bf0abb423e59c2474ab3cd5e8`  
		Last Modified: Thu, 30 Jun 2022 20:13:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jre`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jre` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jre` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jre11`

```console
$ docker pull jruby@sha256:8c0fa63b01ca40075c1416e7569f79d7d4e7aba78ce38df1c16095441734db51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:2185f434305756941ca6e894c6fbb4a5170635e8b22fb42506e8bdfd67e489b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123880539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0173f3a956e44fcdc7ac98e2659c40e0aee1502cf003270b8b59ad775b8ebc`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:53:56 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:53:57 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:53:57 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:53:59 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:53:59 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:00 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:54:08 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:54:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:54:09 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:54:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:54:09 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ae92f358c70d8fd806258a568ab6bb0581b12b2639e6e623506e2162f7900e`  
		Last Modified: Thu, 28 Jul 2022 16:27:27 GMT  
		Size: 43.5 MB (43516900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc8255dbec5821a13865484e05618c120f38a534deecf3bd28da1262315c41c`  
		Last Modified: Thu, 28 Jul 2022 16:27:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b321cf2d70fe77791d06b01472db4261d8f61c04367911cbf028e5c0eb8c2`  
		Last Modified: Thu, 28 Jul 2022 18:56:48 GMT  
		Size: 6.9 MB (6919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29f95a5af7ec22468bca73b4e5a1c242481b60d7b7554e412548ebf32b6d95d`  
		Last Modified: Thu, 28 Jul 2022 18:56:49 GMT  
		Size: 27.8 MB (27783615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f91076c950f202fad3fe5f0690995a1e0ba0b864f1cf6139c6f974d9a03c4`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda039f6be64c2cf18f6a2a4dc38b2fd55edd44f47ac6d75bda1606e3518aa67`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 1.1 MB (1057824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd99ae721f03e5be60281d72991e6829cf3423d224dd88f1737a3877de7bdbb`  
		Last Modified: Thu, 28 Jul 2022 18:56:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:e3ee8ca2776f988158f6908731065a97af4bcf204e368b2654d62c5bbdd64907
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119418771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae17aefbc9a1c019419748c63f2a8464558bb8d595e552cd1459634e50a325`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 15:40:28 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 15:41:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3fa9cb99229ede53d4efddb686106df77794e02b1f4defea6b70b2b53380a8c7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='658ee6d797e6ca4d25de24d45072a44ed8462e3a9feaa38ef9f6d033d18401c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6002b8f6c7b3421ac70601d1bf55f355b75c4a193c97e12974b4c2301d737d8d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='683902c6429f28c606685f46d628291c989de3effe50eca51889388d65f96b95';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74988677f1e1692f8f482ae5f75814b908bb3cf5a8b7d9872873a42e330e7595';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 15:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 15:41:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 18:25:39 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 18:25:39 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 28 Jul 2022 18:25:40 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 28 Jul 2022 18:25:43 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 28 Jul 2022 18:25:43 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:25:44 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 28 Jul 2022 18:25:55 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 28 Jul 2022 18:25:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 28 Jul 2022 18:25:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 28 Jul 2022 18:25:57 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 18:25:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 28 Jul 2022 18:25:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417e8638aad07f61e7c9047910d97970c246439035ead3a991fab7760e489b8`  
		Last Modified: Thu, 28 Jul 2022 15:48:51 GMT  
		Size: 41.8 MB (41846560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c060d7aa2dde1ab42563f6114cc26f12f075abcf4159fa4c0a3db98287c701`  
		Last Modified: Thu, 28 Jul 2022 15:48:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781cdbf7395858245a361b3f499b94d67201d2578f61954177d6f2d36f41ffaf`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 5.6 MB (5643403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4a6a243373d326b702e2f36a58fa5ec01315d6cdae00b009cc48f11932ca9a`  
		Last Modified: Thu, 28 Jul 2022 18:28:25 GMT  
		Size: 27.8 MB (27782127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85acf0a98ce53abb9571a69a0b06de9f8f2a03da0969f9105a4a0d4770d1652`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4b9ce72335676149f5ca6049ad402e0153aede52bffc3c1135ec36cdbd739a`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 1.1 MB (1056702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad241adc57c31cb2b7fded82b022a42a0b29868c7717a97e3e65c0b2d66bdf0f`  
		Last Modified: Thu, 28 Jul 2022 18:28:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jre8`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jre8` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jre8` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:latest`

```console
$ docker pull jruby@sha256:8157c7a110d55c1c33f4541c2879b89599b7508da84da21233d6854260582fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:latest` - linux; amd64

```console
$ docker pull jruby@sha256:53e4e9d80d82a761f1f98296707d77ff62ca82822a5ac0657a3e45227472680c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122153332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bcdddf1e843cf3e9a41476c50663e7045af8f3cc8c804dad7f54c537cb3b2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:12:53 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 19:07:31 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:07:32 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:07:34 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:07:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:07:43 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:07:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f97d71216338a638955bb5df149dc27c1e9491901eb7e6e8301a1e0a27e6ca3`  
		Last Modified: Tue, 07 Jun 2022 00:20:08 GMT  
		Size: 41.8 MB (41798982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270d9e33d909b5daa900daba5ed5652d3fe07edbcc53ae67e0630cdfd536f0b`  
		Last Modified: Tue, 07 Jun 2022 00:20:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264da0e17e9ee2036f3e0853408ce9eec8a0a804523acca3317165815c304d8`  
		Last Modified: Thu, 30 Jun 2022 19:11:32 GMT  
		Size: 6.9 MB (6913860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bce4dd92495121c90afd8517f2cb6ce2602e5a787cb4681777d5a41cc00312`  
		Last Modified: Thu, 30 Jun 2022 19:11:33 GMT  
		Size: 27.8 MB (27783511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649025cc1103118d871acf3671d0292a31d826c1d6eabb874f33459301514c43`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64844070c032565ede0ecd4eb0b3101408363f78b36b06b7f3b37b0db06849c1`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3b61c90f122023cb6d4b2ec7e5bcbcedc10afa046321a8bd3c2b7f3471fd7`  
		Last Modified: Thu, 30 Jun 2022 19:11:31 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:latest` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5a63045b600f587f1d996395db375b001c5427be9891d652594927948951a4a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b598d0103ae7118cc05da811750c690da50712f1248aa2ad3686b03e31e54e0`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:34:18 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 06:35:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 30 Jun 2022 20:08:29 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:08:29 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:08:30 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:08:33 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:08:34 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:35 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:08:46 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:08:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:08:49 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:08:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:08:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4ee9523c27ce56645c07f25e32f84c4fd83a4216ae43725a34ca69220624bf`  
		Last Modified: Tue, 07 Jun 2022 06:42:34 GMT  
		Size: 40.8 MB (40785918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417deba051990dc1f414c8e194a86e9ecb62977afd4bed482871f23b395fbbd0`  
		Last Modified: Tue, 07 Jun 2022 06:42:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c198e84527580f1663d69167ca37a26fbc938fb1e8ee9bb352ca9b797d7b3`  
		Last Modified: Thu, 30 Jun 2022 20:12:21 GMT  
		Size: 5.6 MB (5638968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55043a6d2d78e330c843ffdf59326d5694a58f01deddbbc4eafa105ddc92db9b`  
		Last Modified: Thu, 30 Jun 2022 20:12:22 GMT  
		Size: 27.8 MB (27781251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bcfa578ee09bbef33d8c78f24f74be0155223f0346ea17e8bdef51943d7ee5`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484c0e42cb965854b7839e62fc265a8cf4635ac26f508b0e901d412aa1b0005b`  
		Last Modified: Thu, 30 Jun 2022 20:12:20 GMT  
		Size: 1.1 MB (1052750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47f7bb5a843bd3cf07050a485c354ebe053826da86aba761a9d1e9c6f6a05c6`  
		Last Modified: Thu, 30 Jun 2022 20:12:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
