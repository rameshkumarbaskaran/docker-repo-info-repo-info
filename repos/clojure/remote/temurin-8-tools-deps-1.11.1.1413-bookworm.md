## `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm`

```console
$ docker pull clojure@sha256:12e08538cea141c3be7bfedc02f433a56a9a5ef7f96f61b94bdd48fc611f8654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:28426e7563386f862b7620fb782d00c20a9d13b898318a1af7fd10c75340d26e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236543492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b031c1279928f3d8cd0bf78d8e79cfe99fb10160da0d981633e7aad14ac7010`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:49:21 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:55:41 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 01:55:41 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:56:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 02 Nov 2023 01:56:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 01:56:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb39566a75265042a4da46fe895a549775ce2e985de2d6c4feb658793a1d88e`  
		Last Modified: Thu, 02 Nov 2023 02:02:40 GMT  
		Size: 103.6 MB (103598249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64839beba00a7dcda92e27cfa7030e3bd8a2c59d4e518118ef69492e74071c5d`  
		Last Modified: Thu, 02 Nov 2023 02:05:55 GMT  
		Size: 83.4 MB (83362601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65c9fc1fff303748e2d87758feee2a8605b445f36948c0bbdd006795f5761e2`  
		Last Modified: Thu, 02 Nov 2023 02:05:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:36e8899d1f3d57487ed78dca5ba29edcea0874c1798da31ce4809488f56a802b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235428793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c0b7dbf022aadea896173c029d0f5b99d6b9dffc865ea3f1686133be3a27a8`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:28:09 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:32:59 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 03:32:59 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:33:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 02 Nov 2023 03:33:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 03:33:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a214d30cfffddc78d15882c23dbbb68b263dad08cc11c233ef134c0c7e821fd`  
		Last Modified: Thu, 02 Nov 2023 03:38:08 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92146940864a7e1c343bf831005ba34b8b8b92a0ad4f4b17b8be9146c45f5acd`  
		Last Modified: Thu, 02 Nov 2023 03:40:49 GMT  
		Size: 83.1 MB (83113993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5db8480fc81592357e7a18e62250d475a68aea47348b4c1f9637c96d112da2c`  
		Last Modified: Thu, 02 Nov 2023 03:40:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
