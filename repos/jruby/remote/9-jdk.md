## `jruby:9-jdk`

```console
$ docker pull jruby@sha256:0c48a74f6301afce2f072846d1b797cb98c09b5b179e6e2fd848ccb27a66698f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jruby:9-jdk` - linux; amd64

```console
$ docker pull jruby@sha256:2a6bfa80650c460b70efbf606d106bf33585946370ef006832aae476324005e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96881c296e164e65ff718f3b36c891cbbac4ed6c91b71cb5ee5aa863e8214421`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:27:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 17:27:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 17:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 17:27:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:19:59 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:06:21 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:23:12 GMT
ENV JRUBY_VERSION=9.4.0.0
# Fri, 25 Nov 2022 21:23:12 GMT
ENV JRUBY_SHA256=897bb8a98ad43adcbf5fd3aa75ec85b3312838c949592ca3f623dc1f569d2870
# Fri, 25 Nov 2022 21:23:14 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 25 Nov 2022 21:23:15 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:23:15 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 25 Nov 2022 21:23:23 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 25 Nov 2022 21:23:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 25 Nov 2022 21:23:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 25 Nov 2022 21:23:23 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:23:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 25 Nov 2022 21:23:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1869246ce33b7e9d4cfc0f2be772ef684e2425767400664f548b81c2a69eb`  
		Last Modified: Tue, 25 Oct 2022 17:33:48 GMT  
		Size: 16.4 MB (16353656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f80a1a0fab2544d040bfad097e957b495735264717b873ffc8702479c344da`  
		Last Modified: Fri, 04 Nov 2022 23:25:14 GMT  
		Size: 103.5 MB (103530792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474407bf19afc18eb4e902eab43ac082c4e6590966c2de3d6d0cdc74aa8534d6`  
		Last Modified: Fri, 04 Nov 2022 23:25:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a211813e9e7a293a1716bcf164e17faed2a52afc1235b6ec5c3ac011cb2bf31`  
		Last Modified: Sat, 05 Nov 2022 00:09:48 GMT  
		Size: 6.9 MB (6923795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ad51524c5280482ab545ee25173215dbd2ba011ff34ba21e80733d5eda45ae`  
		Last Modified: Fri, 25 Nov 2022 21:26:24 GMT  
		Size: 29.5 MB (29539785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b135c9c9ecdbcbfa1e00fcef54a7fabfe995873b9a35fa3da4fd4934cdf1b6f`  
		Last Modified: Fri, 25 Nov 2022 21:26:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653289a0a9c39e4f8c7d3d30fae8a1464c0c7a924ce70a0bb93c49485512d71a`  
		Last Modified: Fri, 25 Nov 2022 21:26:22 GMT  
		Size: 1.1 MB (1097575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a285426c797dd0553389f1a367db79ff56ea249ecb40709c982abc79c899983`  
		Last Modified: Fri, 25 Nov 2022 21:26:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jruby:9-jdk` - linux; arm64 variant v8

```console
$ docker pull jruby@sha256:d4626f0ebb785ebbf3c59b0c902ca97f1ed01b0a474fc430d91d5693905b47e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182567559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c461baec0dd5aec4151815e1cab5eb114fd82cbc8037bb46dcfea2e2399b1e9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:07:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 01:07:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 01:07:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Oct 2022 01:08:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:38 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:39:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:39:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 04 Nov 2022 23:40:32 GMT
RUN apt-get update && apt-get install -y libc6-dev --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:41:49 GMT
ENV JRUBY_VERSION=9.4.0.0
# Fri, 25 Nov 2022 21:41:49 GMT
ENV JRUBY_SHA256=897bb8a98ad43adcbf5fd3aa75ec85b3312838c949592ca3f623dc1f569d2870
# Fri, 25 Nov 2022 21:41:51 GMT
RUN mkdir /opt/jruby   && curl -fSL https://repo1.maven.org/maven2/org/jruby/jruby-dist/${JRUBY_VERSION}/jruby-dist-${JRUBY_VERSION}-bin.tar.gz -o /tmp/jruby.tar.gz   && echo "$JRUBY_SHA256 /tmp/jruby.tar.gz" | sha256sum -c -   && tar -zx --strip-components=1 -f /tmp/jruby.tar.gz -C /opt/jruby   && rm /tmp/jruby.tar.gz   && update-alternatives --install /usr/local/bin/ruby ruby /opt/jruby/bin/jruby 1
# Fri, 25 Nov 2022 21:41:51 GMT
ENV PATH=/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:41:52 GMT
RUN mkdir -p /opt/jruby/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /opt/jruby/etc/gemrc
# Fri, 25 Nov 2022 21:41:58 GMT
RUN gem install bundler rake net-telnet xmlrpc
# Fri, 25 Nov 2022 21:41:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 25 Nov 2022 21:41:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 25 Nov 2022 21:41:59 GMT
ENV PATH=/usr/local/bundle/bin:/opt/jruby/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:41:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 25 Nov 2022 21:41:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b9bffe95bbbebdbdfba5c69142aeb65478735d04064fd29982a5b9c980559e`  
		Last Modified: Wed, 26 Oct 2022 01:16:15 GMT  
		Size: 16.2 MB (16216007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d22354a80d2d12ffad6f61953c73519c4d3e501897b672ceaa720a21ca9533`  
		Last Modified: Fri, 04 Nov 2022 22:43:42 GMT  
		Size: 102.6 MB (102630792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd3de5d3cf89d4eb535267ba80576b5c8b40771b2b9213e5a423086faf1b916`  
		Last Modified: Fri, 04 Nov 2022 22:43:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76083e2bbb9d806969ce8ad3eca743ddbc01f21cf076d1145a17ed2a6cd0ad2c`  
		Last Modified: Fri, 04 Nov 2022 23:42:26 GMT  
		Size: 5.9 MB (5886787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe2970d65f7fb485e56a1d2c6a1198a7c8396dfe9228927936bc57026debc43`  
		Last Modified: Fri, 25 Nov 2022 21:44:17 GMT  
		Size: 29.5 MB (29539838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9423d2907b856cd29eb3a254668c7c3d6cb68726514a3ec8946d6fc670626aff`  
		Last Modified: Fri, 25 Nov 2022 21:44:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf585a23f7b2df18c38991675378a3567e927fc5e7526adeeae6b3faff6aaa41`  
		Last Modified: Fri, 25 Nov 2022 21:44:15 GMT  
		Size: 1.1 MB (1097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd55bcb409cdb18d82b7f0c3ecdc9ecd7944dc8274f9db158953eaee54237a5`  
		Last Modified: Fri, 25 Nov 2022 21:44:14 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
