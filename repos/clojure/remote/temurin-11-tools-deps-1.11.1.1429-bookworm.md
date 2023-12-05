## `clojure:temurin-11-tools-deps-1.11.1.1429-bookworm`

```console
$ docker pull clojure@sha256:63ca59e6b12e7d9e978f4df35f94c6f6bf98083df2c631899af3e3deb71d9bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1429-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:771acc5df2ae4fd0c05143e915118b371d1cd93e0d890ef8c19373fc3fb3bc32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278428918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887c456e9e21cd1597c8652f698bc06af114d5c55c3ea829bd0e78546d42647e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:54:06 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:54:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:26:01 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:26:01 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:26:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:26:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:26:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5a177a4408bf01c234a96a773d806e23dea8a68ad9b62f313c86daab19599e`  
		Last Modified: Sat, 02 Dec 2023 10:13:41 GMT  
		Size: 145.3 MB (145266398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae64dd072ab07c813e70a2117f1d110d4504cbb7da30953f0229e8659b9d140`  
		Last Modified: Tue, 05 Dec 2023 18:38:21 GMT  
		Size: 83.6 MB (83579675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbc25d734773445f8b543d5473e7421a00c4f0a0ea2cde442637872d485f5fc`  
		Last Modified: Tue, 05 Dec 2023 18:38:12 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1429-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e550b334f85a77101b090baa8a6a9c5aec33309c93d319fb58f61d8f2780a0bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274947732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba19153d2ce186936145eba64793ff6be4604630b86c764ce4c8fb7a48449dfc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:44:30 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:44:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:42:37 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:42:38 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:42:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:42:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:42:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315e261122e4eab35c627bf04f6ca13cb4652c256e98fcc558b03f00b879462f`  
		Last Modified: Sat, 02 Dec 2023 09:03:38 GMT  
		Size: 142.0 MB (142001821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262cc52b49dd928294bfc658ef903389783f4a8f341412220143f60e03680ece`  
		Last Modified: Tue, 05 Dec 2023 19:52:39 GMT  
		Size: 83.3 MB (83332644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16bdbbee66751537317cae15146c6db3f02e35115ede2cf345d87216d2ccad`  
		Last Modified: Tue, 05 Dec 2023 19:52:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
