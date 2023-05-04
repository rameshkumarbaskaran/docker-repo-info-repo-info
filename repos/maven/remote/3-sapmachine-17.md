## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:bc5f998a7404246475bcbe276d2520c3db84a128cd02e298ffefb1f0aeb96d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:e7477b45efe7750fc55c39356d27f3c6eda31a7f19037b562a9160b399343126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262399386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb0314ddb9f74f76b5f2fed105193b208bd1b44b59323c98bdd0abd4da07407`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 18:44:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Apr 2023 18:45:35 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Apr 2023 18:45:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 20 Apr 2023 18:45:35 GMT
CMD ["jshell"]
# Wed, 26 Apr 2023 19:21:32 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Apr 2023 19:21:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 26 Apr 2023 19:21:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 26 Apr 2023 19:21:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 26 Apr 2023 19:21:32 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 26 Apr 2023 19:21:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 26 Apr 2023 19:21:32 GMT
ARG MAVEN_VERSION=3.9.1
# Wed, 26 Apr 2023 19:21:32 GMT
ARG USER_HOME_DIR=/root
# Wed, 26 Apr 2023 19:21:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 26 Apr 2023 19:21:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 26 Apr 2023 19:21:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a5b5268ecb899a31c205de0c77cf1f8053b07cfac8de0c7c410c5b57e2128d`  
		Last Modified: Thu, 20 Apr 2023 18:46:23 GMT  
		Size: 4.6 MB (4592328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fe43f98566827f1cb88420e016e467d64f34dd83c411cc6fe9b0d01f5e7bc7`  
		Last Modified: Thu, 20 Apr 2023 18:46:58 GMT  
		Size: 198.5 MB (198528092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464b0ddb131ad039fe182303231e607faa2f2c997982cb7c1a3a9c4bdbd8f919`  
		Last Modified: Thu, 20 Apr 2023 19:11:12 GMT  
		Size: 19.7 MB (19741472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fe08572ccdc19fe61a8af671113d86599eb0aa3edce8a5075a1ac6638bfd7`  
		Last Modified: Thu, 20 Apr 2023 19:11:10 GMT  
		Size: 9.1 MB (9106158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d840cf27b58e9d4971d964ad95a3c39cab53609a55eb29857c9ef1b6dd526772`  
		Last Modified: Thu, 20 Apr 2023 19:11:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a6bb6fa6d029672af1b3a0d0aff1f819ec69465263dc93fb6240964e1d0126`  
		Last Modified: Thu, 20 Apr 2023 19:11:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336155f336e1c8ddbb622bde27fe056fb031dc65e8bf138e632d032ca34ad8f`  
		Last Modified: Thu, 20 Apr 2023 19:11:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:18c5ceec5f9834edf513254208f891898b13a4117a4bbfe5bd9a1e1cae061df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258975115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b6c6de85079fb9bf6366dd22131367c96efeb35e1283811095aec07c4c69fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:53:29 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:54:27 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:54:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 04 May 2023 03:54:29 GMT
CMD ["jshell"]
# Thu, 04 May 2023 03:54:29 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 03:54:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 03:54:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 03:54:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 03:54:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 03:54:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 03:54:29 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 03:54:29 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 03:54:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 03:54:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 03:54:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabb4a680a4f885d69bcbda4c93a9dfd1b2be327ee384de4924e71b85b7144fc`  
		Last Modified: Thu, 04 May 2023 03:55:06 GMT  
		Size: 4.5 MB (4543147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fdb30dfbf27a25db96525da10ae7c1872ca3e4c010daf1afd03f5b8e4802f7`  
		Last Modified: Thu, 04 May 2023 03:55:36 GMT  
		Size: 197.1 MB (197132739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb85e3ed469000d29e01defc5fc88b24ba92033f67a32013a10dd6e3492bf729`  
		Last Modified: Thu, 04 May 2023 12:04:26 GMT  
		Size: 19.8 MB (19802270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999813b9a619cc732d912c886ef7b139361e985aded6919880eb1881aadbed81`  
		Last Modified: Thu, 04 May 2023 12:04:24 GMT  
		Size: 9.1 MB (9106153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718b81fb1d323a01ac3861377a4f999be75e3753c486cd5b535e10a1d1f98bb8`  
		Last Modified: Thu, 04 May 2023 12:04:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52b9cd8fe3d5477d212f9b9edd0317cc0e874af15696214b89ddae528e1d56`  
		Last Modified: Thu, 04 May 2023 12:04:23 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f0ffbd2becbbe31ffacfa98de7c7139f385400ea76d9307862e3f7abfe7e4a`  
		Last Modified: Thu, 04 May 2023 12:04:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:e1eef874c635cd2c3bc72abceed7e7ec127ba4bf289539b0c7244ee460ed9646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272803794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34659426373091ff1141b10f6b5a1c14df11e755b35981f0b3f8717404d9233d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 18:22:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Apr 2023 18:26:33 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Apr 2023 18:26:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 20 Apr 2023 18:26:38 GMT
CMD ["jshell"]
# Wed, 26 Apr 2023 19:20:17 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Apr 2023 19:20:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 26 Apr 2023 19:20:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 26 Apr 2023 19:20:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 26 Apr 2023 19:20:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 26 Apr 2023 19:20:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 26 Apr 2023 19:20:17 GMT
ARG MAVEN_VERSION=3.9.1
# Wed, 26 Apr 2023 19:20:17 GMT
ARG USER_HOME_DIR=/root
# Wed, 26 Apr 2023 19:20:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 26 Apr 2023 19:20:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 26 Apr 2023 19:20:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a222b3ac44e570000940f79657b7cfdced6857f11e00bce8cf474f050eaca0`  
		Last Modified: Thu, 20 Apr 2023 18:29:26 GMT  
		Size: 5.4 MB (5357304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957c76f13716087105b2398278590615a77dd32f0b5644e7d21378483975105f`  
		Last Modified: Thu, 20 Apr 2023 18:30:26 GMT  
		Size: 199.5 MB (199484828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0074ec4eca8f6e0c6d0b8684d8063a3beaf686a19913e14e0df6697039d1a8ce`  
		Last Modified: Thu, 20 Apr 2023 18:49:22 GMT  
		Size: 23.1 MB (23142422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866b54c31e19428bc614baa1bf0576748710e00011970242641434a5c0ea193`  
		Last Modified: Thu, 20 Apr 2023 18:49:16 GMT  
		Size: 9.1 MB (9106141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d7426c864e86f1fde7ffaf801872536d395114024808a6c99f58d1cbf1deaa`  
		Last Modified: Thu, 20 Apr 2023 18:49:15 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe3c2a9b66e8b9671c54d156bce6f8b878fb6fe2839c4cbe1f5d1e2358a2743`  
		Last Modified: Thu, 20 Apr 2023 18:49:15 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c1dac58a8cd925067e6d060ac071734070f2a59d1b794644b96ee9212dc0e`  
		Last Modified: Thu, 20 Apr 2023 18:49:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
