## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:268831200797e6e916dae1de3e6b858b07f3cf45e0a4eaf7654861fbf0c4a308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:810c72ee7b506b85de896ad89267d4f9c722335c13018dcd69d8e8f7d9aedc20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291793547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b220ae7c39da3e0f7b683a2bee730c8827f70ad7d5dd9af39728c66f70c90ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:07:38 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:07:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:31:30 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:31:30 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:31:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:31:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:31:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 18:31:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 18:31:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3a90da154217ecef60b201c1bc5d5def59c094922336d6be8b224eaaf18d5`  
		Last Modified: Tue, 21 Nov 2023 10:28:30 GMT  
		Size: 158.6 MB (158630613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d9d464663e6669f5b25f7bf9d5137590102c2cd6affce5c74900665de4aaed`  
		Last Modified: Tue, 05 Dec 2023 18:42:59 GMT  
		Size: 83.6 MB (83579689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078ff37a5e6cc884d79cde5a83cf810b67e254e64fbbd4040d345c34c28f784c`  
		Last Modified: Tue, 05 Dec 2023 18:42:50 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6151cfe8ea40fc7fc0638e87d4fe3e99f855a17f7c41ad76415ed2c127ade4`  
		Last Modified: Tue, 05 Dec 2023 18:42:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:397dd02e52409ba5aa88ecf7b18f98e808b1f07df79a0162bcdfef300e24156e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289818557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ebb0bdfb2c4c7cb6ea6a1ef8b9a5d609b1ca5007a223146836702d2e67a638`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:20:18 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:20:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:46:54 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:46:54 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:47:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:47:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:47:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 19:47:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 19:47:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e114fbda3686a5d964b1bc17b07f06fee9fbefa9480d38197335f8a25aa827eb`  
		Last Modified: Tue, 21 Nov 2023 07:39:44 GMT  
		Size: 156.9 MB (156872155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a260f074bfd89200842c921c06e4976b231eb232d14c974e7a1006b61e2dde83`  
		Last Modified: Tue, 05 Dec 2023 19:56:32 GMT  
		Size: 83.3 MB (83332735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fbba537455b38f2c5e5e44af54307d8f26514d882611a7aba309ba0e9f45d0`  
		Last Modified: Tue, 05 Dec 2023 19:56:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32babe022d5b1be038372c8b8f6fc197f645e53063f1bddd1179ea3998ea3325`  
		Last Modified: Tue, 05 Dec 2023 19:56:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
