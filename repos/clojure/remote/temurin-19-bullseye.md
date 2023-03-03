## `clojure:temurin-19-bullseye`

```console
$ docker pull clojure@sha256:5759c65e0fff22243b441b378cc4a30a24137081ab811c5bd31607bf46c205f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:89d9e6ae39116119efa0806adbd6ff69d8e5ff9ed5b5e2f6d5dc4b4917d327a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328037313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb10b9471fb86bc81d20c48a314f2d9fa29d0479b553873541dd5eaabd10618`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:49:43 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Mar 2023 19:27:45 GMT
ENV CLOJURE_VERSION=1.11.1.1237
# Fri, 03 Mar 2023 19:27:45 GMT
WORKDIR /tmp
# Fri, 03 Mar 2023 19:28:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1cadeebb4ac96c7655f04c60369c6ea69968cc168b44e607df32aac739700751 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 03 Mar 2023 19:28:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Mar 2023 19:28:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Mar 2023 19:28:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Mar 2023 19:28:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28081d65626e3fe290ed0277941e3e5a31dee293f2403db18b27a4b41888fb76`  
		Last Modified: Wed, 01 Mar 2023 08:00:49 GMT  
		Size: 201.1 MB (201112993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d27a9be9d5404d64575822b7ff0b725c24d3720a9a66a35e7f4cd56cb418a5`  
		Last Modified: Fri, 03 Mar 2023 19:38:17 GMT  
		Size: 71.9 MB (71877379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2afa130a72679e5fae146e5756cbcaa52fcd8022d1b2ca70891a813e66f9692`  
		Last Modified: Fri, 03 Mar 2023 19:38:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b66ae272da9c382927c9cead97b89f741f0a7c1f229176d9206560ef37ed4e`  
		Last Modified: Fri, 03 Mar 2023 19:38:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2afe4bd75d028658355f76e3961c199a75a4d5df84c65ed6e1c2916470932b44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325550455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d2097e1e8c5d713fb6280961c7bb8f0a84bf1e95f616d1fb48813f77643d38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:13 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Mar 2023 19:46:51 GMT
ENV CLOJURE_VERSION=1.11.1.1237
# Fri, 03 Mar 2023 19:46:51 GMT
WORKDIR /tmp
# Fri, 03 Mar 2023 19:47:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1cadeebb4ac96c7655f04c60369c6ea69968cc168b44e607df32aac739700751 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 03 Mar 2023 19:47:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Mar 2023 19:47:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Mar 2023 19:47:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Mar 2023 19:47:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f14b17f40d43b36c3ca31112958858ecb243428662f3cf865bcfd47ff1cf7c3`  
		Last Modified: Wed, 01 Mar 2023 03:19:11 GMT  
		Size: 199.9 MB (199855198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f93c84e016bcf758ae4e15b2703c0331136f1bc49b209b9eeee80e3851018c`  
		Last Modified: Fri, 03 Mar 2023 19:55:22 GMT  
		Size: 72.0 MB (71991026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fa7883d666e6953ee2947e81793571748ea171df3ae541c44c0f84f307e9fb`  
		Last Modified: Fri, 03 Mar 2023 19:55:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33971a0459d362f4112fd82deea921dd0729140c32ea7de93e97f9180042a0e`  
		Last Modified: Fri, 03 Mar 2023 19:55:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
