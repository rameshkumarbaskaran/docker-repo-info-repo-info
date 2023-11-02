## `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm`

```console
$ docker pull clojure@sha256:d98f5e0ac8c9dca9bc139ff9421bcb07b514749fd3cad6a041668a204c27f734
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
$ docker pull clojure@sha256:7eb06c51708d260eb91fde60799f2387501d7e60afeb2666b5bb0386ae29bb94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235417783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbdba7ce3ea0aaad11be38d1565a88586a4a18cca42008be79a9533efcc20be`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:21:50 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:25:09 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 02:25:09 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:25:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 02:25:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 02:25:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb7d2235ea2a72ac31188f98768da3ba53d7b513fc150bf335e52018597db0`  
		Last Modified: Wed, 01 Nov 2023 02:41:02 GMT  
		Size: 102.7 MB (102690512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0c5a9ab4898472d511301a0243be98093a90bf1a8e7f9e9602d2a794a61fa5`  
		Last Modified: Wed, 01 Nov 2023 02:42:56 GMT  
		Size: 83.1 MB (83114000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35a197c92150c191de6532cb217426cef7a9c85fd278e8bcd59d10f657d6ee`  
		Last Modified: Wed, 01 Nov 2023 02:42:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
