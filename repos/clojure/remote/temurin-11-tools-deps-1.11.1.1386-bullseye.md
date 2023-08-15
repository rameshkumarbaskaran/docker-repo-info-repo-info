## `clojure:temurin-11-tools-deps-1.11.1.1386-bullseye`

```console
$ docker pull clojure@sha256:09f72f9e97f8f77afaaf5533d3c660b12f4425e0cdb8c32299dcad91a8a463e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1386-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b9ed21f6d696d547e2e7378f35594addac8d21f422a78715e37ffaa9c4e4f400
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271782478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d275e5f8e54043250a2f83b42ca6712f2e27cc28b0c8d4ccee9d37b7957daa`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 22:29:36 GMT
COPY dir:071e7267c24117f41caea93a03f9d7c7d8dc1c681571e9b8f2b8b433c86f9778 in /opt/java/openjdk 
# Tue, 08 Aug 2023 22:29:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 23:22:41 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Mon, 14 Aug 2023 23:22:41 GMT
WORKDIR /tmp
# Mon, 14 Aug 2023 23:22:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 14 Aug 2023 23:22:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Aug 2023 23:22:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320a4eb0585d7c0fad1a2cb76388ee1ecc94aa2230b3e8084d56c17968d0ef2f`  
		Last Modified: Tue, 08 Aug 2023 22:46:07 GMT  
		Size: 144.8 MB (144831528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc9b4bbd18d8ae40bed5b9f1a70f2c03b7e9c8775b91a338ee43fb149bbb3f`  
		Last Modified: Mon, 14 Aug 2023 23:30:49 GMT  
		Size: 71.9 MB (71894761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41c1336cce2fd86521acf15d1f32144b17768d6e035ba05c401b81cd8a2665`  
		Last Modified: Mon, 14 Aug 2023 23:30:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1386-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:accc4e7c8100e5f5a5ef371ca821171e740f4a8f2e9a49674e62edd9f864c293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267279534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c16a73df5b5470b7ff9a304bc972fa405e8330f8a8010e09e9c60accabfd1ca`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 20:20:57 GMT
COPY dir:ddfd64e7bd36f630cd100cf454a9685f9fd0f9483467dbf7a4c9a71ab0af7089 in /opt/java/openjdk 
# Tue, 08 Aug 2023 20:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Aug 2023 00:31:55 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Tue, 15 Aug 2023 00:31:55 GMT
WORKDIR /tmp
# Tue, 15 Aug 2023 00:32:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Aug 2023 00:32:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Aug 2023 00:32:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407c6d757b759af4edf90fb98cce4e2d9dcbe1dbefa7c50cb1db816f3fc06be8`  
		Last Modified: Tue, 08 Aug 2023 20:32:30 GMT  
		Size: 141.6 MB (141565363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2635d87cb652655a80e3f9eb9cdd3f2d74bc0e0dbd24a0f733444f480e7ad81`  
		Last Modified: Tue, 15 Aug 2023 00:38:18 GMT  
		Size: 72.0 MB (72008762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d04941e2239cf8b7eb9e338c2fd714c3bbfd85018204b4812571a80274dcd28`  
		Last Modified: Tue, 15 Aug 2023 00:38:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
