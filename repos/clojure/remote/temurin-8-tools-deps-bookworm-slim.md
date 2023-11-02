## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:9569c5511ad050c5cd8b3a54adca49b4a223026f23ea13ff7c7de013909c6ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:570cd0cb4c09b06a82d334f8dc3ed31a8c9db47c56edfb34f747ad69d6a4b860
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204681812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0363ddfed244562ba13f0eb0090585638fb1075c0f277ddce923e51ba484d3c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:50:31 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:50:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:56:10 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 01:56:10 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:56:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 02 Nov 2023 01:56:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 01:56:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a218e9c40dab330f555e00fbdf54bbc4a1c72977e72f15e20a344c6eb36f3`  
		Last Modified: Thu, 02 Nov 2023 02:02:58 GMT  
		Size: 103.6 MB (103598265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc11372e0fac332c5604599739dcbb87c9db9f0e16657c3cd55e69d609052df`  
		Last Modified: Thu, 02 Nov 2023 02:06:20 GMT  
		Size: 71.9 MB (71933093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6dd2155bc26a1b3c69d0234e86d1cf6dc078f06c2b67fcd9724b6d8db6aa5c`  
		Last Modified: Thu, 02 Nov 2023 02:06:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7aaf057dbf0cc5e637a467c1120e34afc84f11d84a478f7d908b7e07bc99661
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203564327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6df50b175c613bfe480ee0da21c30adb706107fd8c469817deb1925d3d69a70`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:22:22 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:25:29 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 02:25:29 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:25:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 02:25:45 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 02:25:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1456740a40a5931b0447bcb842d472fd2ce5551c26816f7d692bc84052855f3f`  
		Last Modified: Wed, 01 Nov 2023 02:41:23 GMT  
		Size: 102.7 MB (102690497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc180a5393e3971055ed8786ed8ae362ccb0def4a74f920b5e61db9f0b8937b`  
		Last Modified: Wed, 01 Nov 2023 02:43:15 GMT  
		Size: 71.7 MB (71694095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00928afe8eda749ecc1b8500f397bb0b18c4d04a27b54f06a054e05efc499de`  
		Last Modified: Wed, 01 Nov 2023 02:43:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
