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
$ docker pull jruby@sha256:2cbb60406d73eeb163e12265ecbbbbdcf76cf297e7187eaa22dd2bd6c12e892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:54ecf9e3151e0d61c23d4a4e592782695d3edfd1da9ce99e98bad2cf537ecda6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274499702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364649250e72cb02b8a81a99800aa4d45918e474466b4de5ceb5cdee7957ba88`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:08:38 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:10:04 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:10:04 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:10:05 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:10:06 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:06 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:14 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:15 GMT
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
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced845e7ea3d13662c8d6adfbfea63fcc8f56552f7a18ab8adc659b161e64d2`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 6.9 MB (6913816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b8026900f5ba57ea6e7423a9d2d635c6f311a41d66cf33c057d2132cab0db`  
		Last Modified: Thu, 30 Jun 2022 19:15:04 GMT  
		Size: 27.8 MB (27844706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277cac1c7dd94767f695e188eac4aa45e08e570a124886df35615c5db11581a`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faeaf70d02ec9f0384d3014e3862d46d3de546c88fad7301e824813ec38a2e7`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 1.1 MB (1053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038c6eb12538cae06da1bec933848b7ba20cece4da97ee4038ec714a6ba2bf27`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2-jdk17`

```console
$ docker pull jruby@sha256:8efc2951eb3162bd63162b4afcbed5e59da3a8c594f713803e9ac3596f463fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:2b31d2e35e2cf8ad81e907cd989e34dd9d5a68b60c45f304b159101cc29b18f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276636470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d26ebf6c5cdb204e94e6212c4334ac281c9800dbfdd0a04c0e89cc3df14f3`
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
# Tue, 07 Jun 2022 00:15:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:15:39 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:09:06 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:10:17 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:10:17 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:10:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:10:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:20 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:27 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:28 GMT
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
	-	`sha256:5437eeffcc0b1025eb5df6497a5dee6331c2dfee7164dee4336a76ed69bf4c09`  
		Last Modified: Tue, 07 Jun 2022 00:22:16 GMT  
		Size: 192.5 MB (192474620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b1a9e656a37b085bd14614614dbc77ed1928cf5b5d27293c43b472541c70e4`  
		Last Modified: Tue, 07 Jun 2022 00:22:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dab290afef28f40c05dae7bc119fcf1f353f4545aedca999b3ef95adba0c15`  
		Last Modified: Thu, 30 Jun 2022 19:13:25 GMT  
		Size: 6.9 MB (6916182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3bd709bdf5d5b534b7fb7ed28ac34fdf57df29d08138532f04db6d5439ede`  
		Last Modified: Thu, 30 Jun 2022 19:15:21 GMT  
		Size: 27.8 MB (27844715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a02f0fb0ba298814393be6b235c4aa097571a9e46ac30941600604c2a8d707`  
		Last Modified: Thu, 30 Jun 2022 19:15:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0cef369c5cc9e44194fafe0307463ccf0902a80db16a640b55cba167f70e01`  
		Last Modified: Thu, 30 Jun 2022 19:15:19 GMT  
		Size: 1.1 MB (1053881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257830dfe4cd3dac5d10de8c99de8145625d8c8c0f18755c89ac0954c1561ff8`  
		Last Modified: Thu, 30 Jun 2022 19:15:18 GMT  
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
$ docker pull jruby@sha256:43eb203b59b9344eb5b0eabd609500471b57d6c90aed68ca83d1ddcfeeb27263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:2026fe0f3e33b6993e5c8df1fd5bf3881eedc1b8f05b70c52b4298029f38e61d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123682544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324638d794b775ce6622a31a870d020e4aa9bc4bd2df54eb110d45d5eaccfcc`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 19:08:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:49 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:50 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:51 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:52 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:01 GMT
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d60e62b2b68748c3eeb21f8519d33a819a42a66aa4b80cab40c3937c976090`  
		Last Modified: Thu, 30 Jun 2022 19:12:51 GMT  
		Size: 6.9 MB (6913695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8b23fea571fae4f5c5a33c644721bae1ac1c50707b2fd24a361fba25a2a62a`  
		Last Modified: Thu, 30 Jun 2022 19:14:46 GMT  
		Size: 27.8 MB (27844678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa679fee5e31d6ad378e1bc3bdac7482929dc3c1608d1114dc88e1f9e991ed`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb26befc5930a36673cf40a1517e5963ac8dd67ea6def06b6f2a4c56de20d24b`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
		Size: 1.1 MB (1053909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f94e288972703532a2d882646f5793e7638b30cf25672a321bba7d7782468`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
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
$ docker pull jruby@sha256:2cbb60406d73eeb163e12265ecbbbbdcf76cf297e7187eaa22dd2bd6c12e892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:54ecf9e3151e0d61c23d4a4e592782695d3edfd1da9ce99e98bad2cf537ecda6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274499702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364649250e72cb02b8a81a99800aa4d45918e474466b4de5ceb5cdee7957ba88`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:08:38 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:10:04 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:10:04 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:10:05 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:10:06 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:06 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:14 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:15 GMT
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
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced845e7ea3d13662c8d6adfbfea63fcc8f56552f7a18ab8adc659b161e64d2`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 6.9 MB (6913816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b8026900f5ba57ea6e7423a9d2d635c6f311a41d66cf33c057d2132cab0db`  
		Last Modified: Thu, 30 Jun 2022 19:15:04 GMT  
		Size: 27.8 MB (27844706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277cac1c7dd94767f695e188eac4aa45e08e570a124886df35615c5db11581a`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faeaf70d02ec9f0384d3014e3862d46d3de546c88fad7301e824813ec38a2e7`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 1.1 MB (1053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038c6eb12538cae06da1bec933848b7ba20cece4da97ee4038ec714a6ba2bf27`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21-jdk17`

```console
$ docker pull jruby@sha256:8efc2951eb3162bd63162b4afcbed5e59da3a8c594f713803e9ac3596f463fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:2b31d2e35e2cf8ad81e907cd989e34dd9d5a68b60c45f304b159101cc29b18f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276636470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d26ebf6c5cdb204e94e6212c4334ac281c9800dbfdd0a04c0e89cc3df14f3`
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
# Tue, 07 Jun 2022 00:15:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:15:39 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:09:06 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:10:17 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:10:17 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:10:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:10:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:20 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:27 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:28 GMT
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
	-	`sha256:5437eeffcc0b1025eb5df6497a5dee6331c2dfee7164dee4336a76ed69bf4c09`  
		Last Modified: Tue, 07 Jun 2022 00:22:16 GMT  
		Size: 192.5 MB (192474620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b1a9e656a37b085bd14614614dbc77ed1928cf5b5d27293c43b472541c70e4`  
		Last Modified: Tue, 07 Jun 2022 00:22:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dab290afef28f40c05dae7bc119fcf1f353f4545aedca999b3ef95adba0c15`  
		Last Modified: Thu, 30 Jun 2022 19:13:25 GMT  
		Size: 6.9 MB (6916182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3bd709bdf5d5b534b7fb7ed28ac34fdf57df29d08138532f04db6d5439ede`  
		Last Modified: Thu, 30 Jun 2022 19:15:21 GMT  
		Size: 27.8 MB (27844715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a02f0fb0ba298814393be6b235c4aa097571a9e46ac30941600604c2a8d707`  
		Last Modified: Thu, 30 Jun 2022 19:15:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0cef369c5cc9e44194fafe0307463ccf0902a80db16a640b55cba167f70e01`  
		Last Modified: Thu, 30 Jun 2022 19:15:19 GMT  
		Size: 1.1 MB (1053881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257830dfe4cd3dac5d10de8c99de8145625d8c8c0f18755c89ac0954c1561ff8`  
		Last Modified: Thu, 30 Jun 2022 19:15:18 GMT  
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
$ docker pull jruby@sha256:43eb203b59b9344eb5b0eabd609500471b57d6c90aed68ca83d1ddcfeeb27263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:2026fe0f3e33b6993e5c8df1fd5bf3881eedc1b8f05b70c52b4298029f38e61d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123682544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324638d794b775ce6622a31a870d020e4aa9bc4bd2df54eb110d45d5eaccfcc`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 19:08:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:49 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:50 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:51 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:52 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:01 GMT
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d60e62b2b68748c3eeb21f8519d33a819a42a66aa4b80cab40c3937c976090`  
		Last Modified: Thu, 30 Jun 2022 19:12:51 GMT  
		Size: 6.9 MB (6913695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8b23fea571fae4f5c5a33c644721bae1ac1c50707b2fd24a361fba25a2a62a`  
		Last Modified: Thu, 30 Jun 2022 19:14:46 GMT  
		Size: 27.8 MB (27844678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa679fee5e31d6ad378e1bc3bdac7482929dc3c1608d1114dc88e1f9e991ed`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb26befc5930a36673cf40a1517e5963ac8dd67ea6def06b6f2a4c56de20d24b`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
		Size: 1.1 MB (1053909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f94e288972703532a2d882646f5793e7638b30cf25672a321bba7d7782468`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
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
$ docker pull jruby@sha256:2cbb60406d73eeb163e12265ecbbbbdcf76cf297e7187eaa22dd2bd6c12e892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:54ecf9e3151e0d61c23d4a4e592782695d3edfd1da9ce99e98bad2cf537ecda6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274499702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364649250e72cb02b8a81a99800aa4d45918e474466b4de5ceb5cdee7957ba88`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:08:38 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:10:04 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:10:04 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:10:05 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:10:06 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:06 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:14 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:14 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:15 GMT
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
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced845e7ea3d13662c8d6adfbfea63fcc8f56552f7a18ab8adc659b161e64d2`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 6.9 MB (6913816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b8026900f5ba57ea6e7423a9d2d635c6f311a41d66cf33c057d2132cab0db`  
		Last Modified: Thu, 30 Jun 2022 19:15:04 GMT  
		Size: 27.8 MB (27844706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277cac1c7dd94767f695e188eac4aa45e08e570a124886df35615c5db11581a`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faeaf70d02ec9f0384d3014e3862d46d3de546c88fad7301e824813ec38a2e7`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 1.1 MB (1053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038c6eb12538cae06da1bec933848b7ba20cece4da97ee4038ec714a6ba2bf27`  
		Last Modified: Thu, 30 Jun 2022 19:15:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.2.21.0-jdk17`

```console
$ docker pull jruby@sha256:8efc2951eb3162bd63162b4afcbed5e59da3a8c594f713803e9ac3596f463fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:2b31d2e35e2cf8ad81e907cd989e34dd9d5a68b60c45f304b159101cc29b18f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276636470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d26ebf6c5cdb204e94e6212c4334ac281c9800dbfdd0a04c0e89cc3df14f3`
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
# Tue, 07 Jun 2022 00:15:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:15:39 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:09:06 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:10:17 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:10:17 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:10:19 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:10:19 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:20 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:27 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:28 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:28 GMT
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
	-	`sha256:5437eeffcc0b1025eb5df6497a5dee6331c2dfee7164dee4336a76ed69bf4c09`  
		Last Modified: Tue, 07 Jun 2022 00:22:16 GMT  
		Size: 192.5 MB (192474620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b1a9e656a37b085bd14614614dbc77ed1928cf5b5d27293c43b472541c70e4`  
		Last Modified: Tue, 07 Jun 2022 00:22:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dab290afef28f40c05dae7bc119fcf1f353f4545aedca999b3ef95adba0c15`  
		Last Modified: Thu, 30 Jun 2022 19:13:25 GMT  
		Size: 6.9 MB (6916182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3bd709bdf5d5b534b7fb7ed28ac34fdf57df29d08138532f04db6d5439ede`  
		Last Modified: Thu, 30 Jun 2022 19:15:21 GMT  
		Size: 27.8 MB (27844715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a02f0fb0ba298814393be6b235c4aa097571a9e46ac30941600604c2a8d707`  
		Last Modified: Thu, 30 Jun 2022 19:15:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0cef369c5cc9e44194fafe0307463ccf0902a80db16a640b55cba167f70e01`  
		Last Modified: Thu, 30 Jun 2022 19:15:19 GMT  
		Size: 1.1 MB (1053881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257830dfe4cd3dac5d10de8c99de8145625d8c8c0f18755c89ac0954c1561ff8`  
		Last Modified: Thu, 30 Jun 2022 19:15:18 GMT  
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
$ docker pull jruby@sha256:43eb203b59b9344eb5b0eabd609500471b57d6c90aed68ca83d1ddcfeeb27263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jruby:9.2.21.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:2026fe0f3e33b6993e5c8df1fd5bf3881eedc1b8f05b70c52b4298029f38e61d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123682544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324638d794b775ce6622a31a870d020e4aa9bc4bd2df54eb110d45d5eaccfcc`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 19:08:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:49 GMT
ENV JRUBY_VERSION=9.2.21.0
# Thu, 30 Jun 2022 19:09:50 GMT
ENV JRUBY_SHA256=dbf05fca4f61bd7d5131d9b83c5f4d1a249213c474b82def37e82013969c8b8a
# Thu, 30 Jun 2022 19:09:51 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:52 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:52 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:10:00 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:10:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:10:00 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:10:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:10:01 GMT
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d60e62b2b68748c3eeb21f8519d33a819a42a66aa4b80cab40c3937c976090`  
		Last Modified: Thu, 30 Jun 2022 19:12:51 GMT  
		Size: 6.9 MB (6913695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8b23fea571fae4f5c5a33c644721bae1ac1c50707b2fd24a361fba25a2a62a`  
		Last Modified: Thu, 30 Jun 2022 19:14:46 GMT  
		Size: 27.8 MB (27844678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa679fee5e31d6ad378e1bc3bdac7482929dc3c1608d1114dc88e1f9e991ed`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb26befc5930a36673cf40a1517e5963ac8dd67ea6def06b6f2a4c56de20d24b`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
		Size: 1.1 MB (1053909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837f94e288972703532a2d882646f5793e7638b30cf25672a321bba7d7782468`  
		Last Modified: Thu, 30 Jun 2022 19:14:44 GMT  
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
$ docker pull jruby@sha256:deeb5ed21992e7af20977470d82f034c348e8d213aeb18b74676ef0910aeb24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:6aa0c06be8c34b547483533bd8e13bc704ecdc0bfbe24f22d6905362abdb0179
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274438561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5826c98cb13962c658e5e4712de2a22712d5a40b4a863812fdf618d5d9862d`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:08:38 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:08:38 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:08:38 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:08:46 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:08:47 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:47 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:56 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:57 GMT
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
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced845e7ea3d13662c8d6adfbfea63fcc8f56552f7a18ab8adc659b161e64d2`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 6.9 MB (6913816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ebcfb9c8cafe04f08a5bd589c0eaad49b100e1c09286c9a13f13fb0a8d79e4`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 27.8 MB (27783471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b28aa471833f794663cfad51dae95b26bab9ca7ded7861024cb42e03b427f`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df9d12342ba08653c2fbe1b60d1e129da84e7fe3963f0c8d8b32f6a2d51e2ed`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 1.1 MB (1053990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c43269a8223739eee38738eb2c79060c18460cc4c07c162376829a9014c55ce`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:809aa4c9b9b4c9d0f52845596c6ac435ecea121511ac2ff4fb5bea813a16bb47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268387850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4d65f9bb34c34c2d42697fbbef379a7558995d6c4c24c733e447bc9ed04383`
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
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:35:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:35:47 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 20:10:22 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:10:22 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:10:23 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:10:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:10:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:27 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:10:39 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:10:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:41 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:10:43 GMT
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
	-	`sha256:45f2246f583b817221ee4ff9cf491f3f17cc8881295de0bd6c1b213dbe7c8585`  
		Last Modified: Tue, 07 Jun 2022 06:43:20 GMT  
		Size: 190.8 MB (190824584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ec9350bf8b0d1ea50051917adf749e1d1b7675d672e1e9c731b5e937ad271e`  
		Last Modified: Tue, 07 Jun 2022 06:43:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e8204c400f744378fd8e5a42898179d96d8546b7fdadbdf8e923c4e09c5ca6`  
		Last Modified: Thu, 30 Jun 2022 20:13:56 GMT  
		Size: 5.6 MB (5638916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd270915ae348dca952927e455105920840c0e2b8bcd8a6570651760e7b8ba7`  
		Last Modified: Thu, 30 Jun 2022 20:13:58 GMT  
		Size: 27.8 MB (27781588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9589be44099a1046de7ea8c6ff5b59cf72ca520f6ff531c62060a429dbaf64`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acadeb37dd32a9edbb57c83c8769f8d98689446ce1e08e7d100d963ffdfb0d9`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 1.1 MB (1052781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ca30488ba3b352c1f2fb7a3373979e837f8d630c5522eeac5bf11e7f96de1d`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3-jdk17`

```console
$ docker pull jruby@sha256:a23c9e69253ba62fef50d63ce05f5464e9996b07234eddfaa69d194717d720fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:16afa8ad054d6a3f83f3bbffaec0fa18c198d27f46a07e1ab883dbf18b7bf26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276575366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264ec8a7706e3827aef10c4e167168bee2c0df7a7126d3efb643379e573f997`
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
# Tue, 07 Jun 2022 00:15:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:15:39 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:09:06 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:06 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:09:06 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:09:08 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:08 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:09 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:18 GMT
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
	-	`sha256:5437eeffcc0b1025eb5df6497a5dee6331c2dfee7164dee4336a76ed69bf4c09`  
		Last Modified: Tue, 07 Jun 2022 00:22:16 GMT  
		Size: 192.5 MB (192474620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b1a9e656a37b085bd14614614dbc77ed1928cf5b5d27293c43b472541c70e4`  
		Last Modified: Tue, 07 Jun 2022 00:22:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dab290afef28f40c05dae7bc119fcf1f353f4545aedca999b3ef95adba0c15`  
		Last Modified: Thu, 30 Jun 2022 19:13:25 GMT  
		Size: 6.9 MB (6916182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e0c199eb2a8e5954a7a96c12f5adab29b5bda9caded2e0e11f617b8f276ea6`  
		Last Modified: Thu, 30 Jun 2022 19:13:26 GMT  
		Size: 27.8 MB (27783502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342dcd8039233c659bcbf61a3d05e8b9f8070a035e5bc885fded13b6342ef914`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142f0ed082323662d8300909d3f4254fb0aac32ee9be7af3d8f9068c18e50e30`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18498e5a31480e8708a32096e902f62490bfaef6c6ccc8a6eba39a85429e8d42`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:d636218332eadb6dee0713ca7e5cb1f6a737e1cdb50c30ea7a2d8d51cd5890c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273412064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ba2692fa81dd15f6ff48267911af8e532532dddba2ed67ee63b6db57ae7db0`
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
# Tue, 07 Jun 2022 06:36:39 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 06:36:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:37:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:37:01 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 20:10:58 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:10:59 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:11:00 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:11:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:11:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:11:04 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:11:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:11:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:11:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:11:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:11:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:11:19 GMT
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
	-	`sha256:ed995bf8c9f64f73e00fd830f670eb602283eadf54da63b7ddedabed61cba76e`  
		Last Modified: Tue, 07 Jun 2022 06:45:03 GMT  
		Size: 191.2 MB (191243930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ef7399b17ee73d94d5ba60ef36d0e3d6ffe4afe7415cf876d6bdae7c807959`  
		Last Modified: Tue, 07 Jun 2022 06:44:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a0935dae9b8d62e77be2a42fe60fe11f1240c0b96a4ba44ac8d50373df8077`  
		Last Modified: Thu, 30 Jun 2022 20:14:15 GMT  
		Size: 5.6 MB (5640833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323395399ae2ea204cc407c48690eb02172a9cc67de29ab77d8ec77b902f23cd`  
		Last Modified: Thu, 30 Jun 2022 20:14:16 GMT  
		Size: 27.8 MB (27781864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16868060b224b29c23a624c42de666ec1e772802351bd64e9daf6596956db75`  
		Last Modified: Thu, 30 Jun 2022 20:14:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038d1e976a77465ab75432a10cec8991a58acced0b63def1d83a7811fd037456`  
		Last Modified: Thu, 30 Jun 2022 20:14:14 GMT  
		Size: 1.1 MB (1052774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69adbb0bd1d6c6593ffb21b350415dce99bd3bb20577360b3413f0a5e8835f5`  
		Last Modified: Thu, 30 Jun 2022 20:14:13 GMT  
		Size: 144.0 B  
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
$ docker pull jruby@sha256:c58b7bad29c9910e35c935cbcf4c601c6833743164392e5c36c3149ad5143233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:65722a0a31ab0255b541bbd644e2c4791a2f57b599911ddab23cfc374ecdd38e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123621425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294c22f269e2a38ccc59902da1f8664a4c41db90fbbb67be8ae5f0ec50e457c5`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 19:08:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:08:18 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:08:18 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:08:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:08:20 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:30 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:31 GMT
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d60e62b2b68748c3eeb21f8519d33a819a42a66aa4b80cab40c3937c976090`  
		Last Modified: Thu, 30 Jun 2022 19:12:51 GMT  
		Size: 6.9 MB (6913695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbb2ca18dde208ae3d9d00dc3d6ab0052417a909207411302a3e3ce2765e0c6`  
		Last Modified: Thu, 30 Jun 2022 19:12:52 GMT  
		Size: 27.8 MB (27783481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43109b1862d02362522485b837234fb2e1862e7330d97ce028208d07cd022046`  
		Last Modified: Thu, 30 Jun 2022 19:12:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646acacb7d6c2b3bfd64d7491f778168ad7d2c9fc5d18c931a1c67a3145e4c93`  
		Last Modified: Thu, 30 Jun 2022 19:12:50 GMT  
		Size: 1.1 MB (1053991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01030e62dbf371e014fe2c7ae02001d73b5eff0117de70cbb34ab1ed4a111b4`  
		Last Modified: Thu, 30 Jun 2022 19:12:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5b98e49afd2224afa6628b45823dff60be3f3bc4f1d20e2e11c89e00f9fed4ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119171937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39541b19d58bf4ac274013c9bf3c2e38f4c5459a339123f5b7c48123a56b4acb`
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
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 20:09:45 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:46 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:47 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:50 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:50 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:51 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:10:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:10:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:10:08 GMT
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
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601161940d6bcacbf3189413a7ba07354aabf04919f86500fb63ff32a5ddbe`  
		Last Modified: Thu, 30 Jun 2022 20:13:38 GMT  
		Size: 5.6 MB (5638957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed42755d2610740508a5fa37484b4f296199745b5426ba19ec78d06d53fd055`  
		Last Modified: Thu, 30 Jun 2022 20:13:40 GMT  
		Size: 27.8 MB (27781902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207ecc7207303bde81f7448753744e0910f48fae5462e0dd81c81e5d0984eba`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079c86016f824866b6452b4e2f26f47f82352cbba475dba61765f999274f236f`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 1.1 MB (1052744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623526e9fa12ca4f0fbdeea10c4ad5589119f78dc2ca7d238652fe1857866be0`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 143.0 B  
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
$ docker pull jruby@sha256:deeb5ed21992e7af20977470d82f034c348e8d213aeb18b74676ef0910aeb24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:6aa0c06be8c34b547483533bd8e13bc704ecdc0bfbe24f22d6905362abdb0179
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274438561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5826c98cb13962c658e5e4712de2a22712d5a40b4a863812fdf618d5d9862d`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:08:38 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:08:38 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:08:38 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:08:46 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:08:47 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:47 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:56 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:57 GMT
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
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced845e7ea3d13662c8d6adfbfea63fcc8f56552f7a18ab8adc659b161e64d2`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 6.9 MB (6913816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ebcfb9c8cafe04f08a5bd589c0eaad49b100e1c09286c9a13f13fb0a8d79e4`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 27.8 MB (27783471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b28aa471833f794663cfad51dae95b26bab9ca7ded7861024cb42e03b427f`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df9d12342ba08653c2fbe1b60d1e129da84e7fe3963f0c8d8b32f6a2d51e2ed`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 1.1 MB (1053990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c43269a8223739eee38738eb2c79060c18460cc4c07c162376829a9014c55ce`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:809aa4c9b9b4c9d0f52845596c6ac435ecea121511ac2ff4fb5bea813a16bb47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268387850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4d65f9bb34c34c2d42697fbbef379a7558995d6c4c24c733e447bc9ed04383`
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
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:35:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:35:47 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 20:10:22 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:10:22 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:10:23 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:10:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:10:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:27 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:10:39 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:10:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:41 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:10:43 GMT
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
	-	`sha256:45f2246f583b817221ee4ff9cf491f3f17cc8881295de0bd6c1b213dbe7c8585`  
		Last Modified: Tue, 07 Jun 2022 06:43:20 GMT  
		Size: 190.8 MB (190824584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ec9350bf8b0d1ea50051917adf749e1d1b7675d672e1e9c731b5e937ad271e`  
		Last Modified: Tue, 07 Jun 2022 06:43:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e8204c400f744378fd8e5a42898179d96d8546b7fdadbdf8e923c4e09c5ca6`  
		Last Modified: Thu, 30 Jun 2022 20:13:56 GMT  
		Size: 5.6 MB (5638916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd270915ae348dca952927e455105920840c0e2b8bcd8a6570651760e7b8ba7`  
		Last Modified: Thu, 30 Jun 2022 20:13:58 GMT  
		Size: 27.8 MB (27781588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9589be44099a1046de7ea8c6ff5b59cf72ca520f6ff531c62060a429dbaf64`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acadeb37dd32a9edbb57c83c8769f8d98689446ce1e08e7d100d963ffdfb0d9`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 1.1 MB (1052781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ca30488ba3b352c1f2fb7a3373979e837f8d630c5522eeac5bf11e7f96de1d`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6-jdk17`

```console
$ docker pull jruby@sha256:a23c9e69253ba62fef50d63ce05f5464e9996b07234eddfaa69d194717d720fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:16afa8ad054d6a3f83f3bbffaec0fa18c198d27f46a07e1ab883dbf18b7bf26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276575366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264ec8a7706e3827aef10c4e167168bee2c0df7a7126d3efb643379e573f997`
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
# Tue, 07 Jun 2022 00:15:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:15:39 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:09:06 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:06 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:09:06 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:09:08 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:08 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:09 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:18 GMT
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
	-	`sha256:5437eeffcc0b1025eb5df6497a5dee6331c2dfee7164dee4336a76ed69bf4c09`  
		Last Modified: Tue, 07 Jun 2022 00:22:16 GMT  
		Size: 192.5 MB (192474620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b1a9e656a37b085bd14614614dbc77ed1928cf5b5d27293c43b472541c70e4`  
		Last Modified: Tue, 07 Jun 2022 00:22:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dab290afef28f40c05dae7bc119fcf1f353f4545aedca999b3ef95adba0c15`  
		Last Modified: Thu, 30 Jun 2022 19:13:25 GMT  
		Size: 6.9 MB (6916182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e0c199eb2a8e5954a7a96c12f5adab29b5bda9caded2e0e11f617b8f276ea6`  
		Last Modified: Thu, 30 Jun 2022 19:13:26 GMT  
		Size: 27.8 MB (27783502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342dcd8039233c659bcbf61a3d05e8b9f8070a035e5bc885fded13b6342ef914`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142f0ed082323662d8300909d3f4254fb0aac32ee9be7af3d8f9068c18e50e30`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18498e5a31480e8708a32096e902f62490bfaef6c6ccc8a6eba39a85429e8d42`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:d636218332eadb6dee0713ca7e5cb1f6a737e1cdb50c30ea7a2d8d51cd5890c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273412064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ba2692fa81dd15f6ff48267911af8e532532dddba2ed67ee63b6db57ae7db0`
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
# Tue, 07 Jun 2022 06:36:39 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 06:36:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:37:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:37:01 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 20:10:58 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:10:59 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:11:00 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:11:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:11:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:11:04 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:11:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:11:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:11:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:11:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:11:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:11:19 GMT
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
	-	`sha256:ed995bf8c9f64f73e00fd830f670eb602283eadf54da63b7ddedabed61cba76e`  
		Last Modified: Tue, 07 Jun 2022 06:45:03 GMT  
		Size: 191.2 MB (191243930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ef7399b17ee73d94d5ba60ef36d0e3d6ffe4afe7415cf876d6bdae7c807959`  
		Last Modified: Tue, 07 Jun 2022 06:44:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a0935dae9b8d62e77be2a42fe60fe11f1240c0b96a4ba44ac8d50373df8077`  
		Last Modified: Thu, 30 Jun 2022 20:14:15 GMT  
		Size: 5.6 MB (5640833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323395399ae2ea204cc407c48690eb02172a9cc67de29ab77d8ec77b902f23cd`  
		Last Modified: Thu, 30 Jun 2022 20:14:16 GMT  
		Size: 27.8 MB (27781864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16868060b224b29c23a624c42de666ec1e772802351bd64e9daf6596956db75`  
		Last Modified: Thu, 30 Jun 2022 20:14:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038d1e976a77465ab75432a10cec8991a58acced0b63def1d83a7811fd037456`  
		Last Modified: Thu, 30 Jun 2022 20:14:14 GMT  
		Size: 1.1 MB (1052774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69adbb0bd1d6c6593ffb21b350415dce99bd3bb20577360b3413f0a5e8835f5`  
		Last Modified: Thu, 30 Jun 2022 20:14:13 GMT  
		Size: 144.0 B  
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
$ docker pull jruby@sha256:c58b7bad29c9910e35c935cbcf4c601c6833743164392e5c36c3149ad5143233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:65722a0a31ab0255b541bbd644e2c4791a2f57b599911ddab23cfc374ecdd38e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123621425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294c22f269e2a38ccc59902da1f8664a4c41db90fbbb67be8ae5f0ec50e457c5`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 19:08:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:08:18 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:08:18 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:08:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:08:20 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:30 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:31 GMT
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d60e62b2b68748c3eeb21f8519d33a819a42a66aa4b80cab40c3937c976090`  
		Last Modified: Thu, 30 Jun 2022 19:12:51 GMT  
		Size: 6.9 MB (6913695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbb2ca18dde208ae3d9d00dc3d6ab0052417a909207411302a3e3ce2765e0c6`  
		Last Modified: Thu, 30 Jun 2022 19:12:52 GMT  
		Size: 27.8 MB (27783481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43109b1862d02362522485b837234fb2e1862e7330d97ce028208d07cd022046`  
		Last Modified: Thu, 30 Jun 2022 19:12:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646acacb7d6c2b3bfd64d7491f778168ad7d2c9fc5d18c931a1c67a3145e4c93`  
		Last Modified: Thu, 30 Jun 2022 19:12:50 GMT  
		Size: 1.1 MB (1053991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01030e62dbf371e014fe2c7ae02001d73b5eff0117de70cbb34ab1ed4a111b4`  
		Last Modified: Thu, 30 Jun 2022 19:12:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5b98e49afd2224afa6628b45823dff60be3f3bc4f1d20e2e11c89e00f9fed4ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119171937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39541b19d58bf4ac274013c9bf3c2e38f4c5459a339123f5b7c48123a56b4acb`
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
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 20:09:45 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:46 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:47 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:50 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:50 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:51 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:10:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:10:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:10:08 GMT
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
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601161940d6bcacbf3189413a7ba07354aabf04919f86500fb63ff32a5ddbe`  
		Last Modified: Thu, 30 Jun 2022 20:13:38 GMT  
		Size: 5.6 MB (5638957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed42755d2610740508a5fa37484b4f296199745b5426ba19ec78d06d53fd055`  
		Last Modified: Thu, 30 Jun 2022 20:13:40 GMT  
		Size: 27.8 MB (27781902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207ecc7207303bde81f7448753744e0910f48fae5462e0dd81c81e5d0984eba`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079c86016f824866b6452b4e2f26f47f82352cbba475dba61765f999274f236f`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 1.1 MB (1052744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623526e9fa12ca4f0fbdeea10c4ad5589119f78dc2ca7d238652fe1857866be0`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 143.0 B  
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
$ docker pull jruby@sha256:deeb5ed21992e7af20977470d82f034c348e8d213aeb18b74676ef0910aeb24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jdk11` - linux; amd64

```console
$ docker pull jruby@sha256:6aa0c06be8c34b547483533bd8e13bc704ecdc0bfbe24f22d6905362abdb0179
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274438561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5826c98cb13962c658e5e4712de2a22712d5a40b4a863812fdf618d5d9862d`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:08:38 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:08:38 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:08:38 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:08:46 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:08:47 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:47 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:56 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:56 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:57 GMT
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
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced845e7ea3d13662c8d6adfbfea63fcc8f56552f7a18ab8adc659b161e64d2`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 6.9 MB (6913816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ebcfb9c8cafe04f08a5bd589c0eaad49b100e1c09286c9a13f13fb0a8d79e4`  
		Last Modified: Thu, 30 Jun 2022 19:13:09 GMT  
		Size: 27.8 MB (27783471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b28aa471833f794663cfad51dae95b26bab9ca7ded7861024cb42e03b427f`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df9d12342ba08653c2fbe1b60d1e129da84e7fe3963f0c8d8b32f6a2d51e2ed`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 1.1 MB (1053990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c43269a8223739eee38738eb2c79060c18460cc4c07c162376829a9014c55ce`  
		Last Modified: Thu, 30 Jun 2022 19:13:07 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jdk11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:809aa4c9b9b4c9d0f52845596c6ac435ecea121511ac2ff4fb5bea813a16bb47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268387850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4d65f9bb34c34c2d42697fbbef379a7558995d6c4c24c733e447bc9ed04383`
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
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:35:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:35:47 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 20:10:22 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:10:22 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:10:23 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:10:26 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:10:26 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:27 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:10:39 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:10:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:41 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:10:43 GMT
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
	-	`sha256:45f2246f583b817221ee4ff9cf491f3f17cc8881295de0bd6c1b213dbe7c8585`  
		Last Modified: Tue, 07 Jun 2022 06:43:20 GMT  
		Size: 190.8 MB (190824584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ec9350bf8b0d1ea50051917adf749e1d1b7675d672e1e9c731b5e937ad271e`  
		Last Modified: Tue, 07 Jun 2022 06:43:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e8204c400f744378fd8e5a42898179d96d8546b7fdadbdf8e923c4e09c5ca6`  
		Last Modified: Thu, 30 Jun 2022 20:13:56 GMT  
		Size: 5.6 MB (5638916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd270915ae348dca952927e455105920840c0e2b8bcd8a6570651760e7b8ba7`  
		Last Modified: Thu, 30 Jun 2022 20:13:58 GMT  
		Size: 27.8 MB (27781588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9589be44099a1046de7ea8c6ff5b59cf72ca520f6ff531c62060a429dbaf64`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acadeb37dd32a9edbb57c83c8769f8d98689446ce1e08e7d100d963ffdfb0d9`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 1.1 MB (1052781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ca30488ba3b352c1f2fb7a3373979e837f8d630c5522eeac5bf11e7f96de1d`  
		Last Modified: Thu, 30 Jun 2022 20:13:55 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jruby:9.3.6.0-jdk17`

```console
$ docker pull jruby@sha256:a23c9e69253ba62fef50d63ce05f5464e9996b07234eddfaa69d194717d720fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jdk17` - linux; amd64

```console
$ docker pull jruby@sha256:16afa8ad054d6a3f83f3bbffaec0fa18c198d27f46a07e1ab883dbf18b7bf26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276575366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3264ec8a7706e3827aef10c4e167168bee2c0df7a7126d3efb643379e573f997`
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
# Tue, 07 Jun 2022 00:15:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 00:15:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:15:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:15:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:15:39 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:09:06 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:09:06 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:09:06 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:09:08 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:09:08 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:09 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:09:17 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:09:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:09:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:09:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:09:18 GMT
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
	-	`sha256:5437eeffcc0b1025eb5df6497a5dee6331c2dfee7164dee4336a76ed69bf4c09`  
		Last Modified: Tue, 07 Jun 2022 00:22:16 GMT  
		Size: 192.5 MB (192474620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b1a9e656a37b085bd14614614dbc77ed1928cf5b5d27293c43b472541c70e4`  
		Last Modified: Tue, 07 Jun 2022 00:22:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dab290afef28f40c05dae7bc119fcf1f353f4545aedca999b3ef95adba0c15`  
		Last Modified: Thu, 30 Jun 2022 19:13:25 GMT  
		Size: 6.9 MB (6916182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e0c199eb2a8e5954a7a96c12f5adab29b5bda9caded2e0e11f617b8f276ea6`  
		Last Modified: Thu, 30 Jun 2022 19:13:26 GMT  
		Size: 27.8 MB (27783502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342dcd8039233c659bcbf61a3d05e8b9f8070a035e5bc885fded13b6342ef914`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142f0ed082323662d8300909d3f4254fb0aac32ee9be7af3d8f9068c18e50e30`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 1.1 MB (1053987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18498e5a31480e8708a32096e902f62490bfaef6c6ccc8a6eba39a85429e8d42`  
		Last Modified: Thu, 30 Jun 2022 19:13:24 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jdk17` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:d636218332eadb6dee0713ca7e5cb1f6a737e1cdb50c30ea7a2d8d51cd5890c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273412064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ba2692fa81dd15f6ff48267911af8e532532dddba2ed67ee63b6db57ae7db0`
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
# Tue, 07 Jun 2022 06:36:39 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Tue, 07 Jun 2022 06:36:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e3c19c1707205c6b90cc04b416e8d83078ed98417d5a69dce3cf7dc0d7cfbca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.3_7.tar.gz';          ;;        armhf|arm)          ESUM='d76c462f44c9f306a0fe4468a0218a261ab152f358a8fb55ec80865bf35e2c41';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.3_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a04587018c9719dca21073f19d56b335c4985f41afe7d99b24852c1a94b917e5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.3_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d9456cdf9719f9d8a11f26b2dd176cd6a8478d96ced09396765c7473482bc7f1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.3_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='81f5bed21077f9fbb04909b50391620c78b9a3c376593c0992934719c0de6b73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:37:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:37:01 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 20:10:58 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:10:59 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:11:00 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:11:03 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:11:03 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:11:04 GMT
RUN mkdir -p /opt/jruby/etc        && {                echo 'install: --no-document';                echo 'update: --no-document';        } >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:11:15 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:11:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:11:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:11:17 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:11:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:11:19 GMT
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
	-	`sha256:ed995bf8c9f64f73e00fd830f670eb602283eadf54da63b7ddedabed61cba76e`  
		Last Modified: Tue, 07 Jun 2022 06:45:03 GMT  
		Size: 191.2 MB (191243930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ef7399b17ee73d94d5ba60ef36d0e3d6ffe4afe7415cf876d6bdae7c807959`  
		Last Modified: Tue, 07 Jun 2022 06:44:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a0935dae9b8d62e77be2a42fe60fe11f1240c0b96a4ba44ac8d50373df8077`  
		Last Modified: Thu, 30 Jun 2022 20:14:15 GMT  
		Size: 5.6 MB (5640833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323395399ae2ea204cc407c48690eb02172a9cc67de29ab77d8ec77b902f23cd`  
		Last Modified: Thu, 30 Jun 2022 20:14:16 GMT  
		Size: 27.8 MB (27781864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16868060b224b29c23a624c42de666ec1e772802351bd64e9daf6596956db75`  
		Last Modified: Thu, 30 Jun 2022 20:14:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038d1e976a77465ab75432a10cec8991a58acced0b63def1d83a7811fd037456`  
		Last Modified: Thu, 30 Jun 2022 20:14:14 GMT  
		Size: 1.1 MB (1052774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69adbb0bd1d6c6593ffb21b350415dce99bd3bb20577360b3413f0a5e8835f5`  
		Last Modified: Thu, 30 Jun 2022 20:14:13 GMT  
		Size: 144.0 B  
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
$ docker pull jruby@sha256:c58b7bad29c9910e35c935cbcf4c601c6833743164392e5c36c3149ad5143233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9.3.6.0-jre11` - linux; amd64

```console
$ docker pull jruby@sha256:65722a0a31ab0255b541bbd644e2c4791a2f57b599911ddab23cfc374ecdd38e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123621425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294c22f269e2a38ccc59902da1f8664a4c41db90fbbb67be8ae5f0ec50e457c5`
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
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 19:08:18 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 19:08:18 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 19:08:18 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 19:08:20 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 19:08:20 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:21 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 19:08:30 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 19:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 19:08:30 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 19:08:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 19:08:31 GMT
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
	-	`sha256:b669251e19038a24bd6cab0baab92077f23163880fac4701fb3efa564350732b`  
		Last Modified: Tue, 07 Jun 2022 00:21:34 GMT  
		Size: 43.3 MB (43267270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf45eff8a02bcdf7a96904e0dc534c78c89a5c860e224fa57780ef2fc2eab99e`  
		Last Modified: Tue, 07 Jun 2022 00:21:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d60e62b2b68748c3eeb21f8519d33a819a42a66aa4b80cab40c3937c976090`  
		Last Modified: Thu, 30 Jun 2022 19:12:51 GMT  
		Size: 6.9 MB (6913695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbb2ca18dde208ae3d9d00dc3d6ab0052417a909207411302a3e3ce2765e0c6`  
		Last Modified: Thu, 30 Jun 2022 19:12:52 GMT  
		Size: 27.8 MB (27783481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43109b1862d02362522485b837234fb2e1862e7330d97ce028208d07cd022046`  
		Last Modified: Thu, 30 Jun 2022 19:12:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646acacb7d6c2b3bfd64d7491f778168ad7d2c9fc5d18c931a1c67a3145e4c93`  
		Last Modified: Thu, 30 Jun 2022 19:12:50 GMT  
		Size: 1.1 MB (1053991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01030e62dbf371e014fe2c7ae02001d73b5eff0117de70cbb34ab1ed4a111b4`  
		Last Modified: Thu, 30 Jun 2022 19:12:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9.3.6.0-jre11` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:5b98e49afd2224afa6628b45823dff60be3f3bc4f1d20e2e11c89e00f9fed4ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119171937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39541b19d58bf4ac274013c9bf3c2e38f4c5459a339123f5b7c48123a56b4acb`
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
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:36:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9e1b9fcef7c2fa9911bd9f2bf51591102ee0367a667e154cf15f20d0c6faa6a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='12489d268a6758dc72c073b11a25eb494804649f4760db05b2ef9ddb71aab73e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bd0fad840c3aa118c0ab4cf4070cb9ad25c0ccab456aa22f9b5fc02f4230b26a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d371ecceccf1d807ca9f0721dba805c65dddc9c5e59c5faaabad37f191970745';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='22831fd097dfb39e844cb34f42064ff26a0ada9cd13621d7b8bca8e9b9d3a5ee';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:36:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 30 Jun 2022 20:09:45 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Thu, 30 Jun 2022 20:09:46 GMT
ENV JRUBY_VERSION=9.3.6.0
# Thu, 30 Jun 2022 20:09:47 GMT
ENV JRUBY_SHA256=747af6af99a674f208f40da8db22d77c6da493a83280e990b52d523abd9499e2
# Thu, 30 Jun 2022 20:09:50 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Thu, 30 Jun 2022 20:09:50 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:09:51 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Thu, 30 Jun 2022 20:10:03 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Thu, 30 Jun 2022 20:10:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Jun 2022 20:10:06 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 20:10:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 30 Jun 2022 20:10:08 GMT
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
	-	`sha256:df8e9d6a15d13e6f2d5d43f40b76051350cb7090cfcae5300dc1647e3196577a`  
		Last Modified: Tue, 07 Jun 2022 06:44:15 GMT  
		Size: 41.6 MB (41608356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51219ca7d003431d2f9c6ddda7db0a1902cf2b7e4e879625811b086f268b39c`  
		Last Modified: Tue, 07 Jun 2022 06:44:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6601161940d6bcacbf3189413a7ba07354aabf04919f86500fb63ff32a5ddbe`  
		Last Modified: Thu, 30 Jun 2022 20:13:38 GMT  
		Size: 5.6 MB (5638957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed42755d2610740508a5fa37484b4f296199745b5426ba19ec78d06d53fd055`  
		Last Modified: Thu, 30 Jun 2022 20:13:40 GMT  
		Size: 27.8 MB (27781902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207ecc7207303bde81f7448753744e0910f48fae5462e0dd81c81e5d0984eba`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079c86016f824866b6452b4e2f26f47f82352cbba475dba61765f999274f236f`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 1.1 MB (1052744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623526e9fa12ca4f0fbdeea10c4ad5589119f78dc2ca7d238652fe1857866be0`  
		Last Modified: Thu, 30 Jun 2022 20:13:37 GMT  
		Size: 143.0 B  
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
