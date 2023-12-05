## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9180547c3f81095d1627e23fdde3ae6aecba97b57337d787c432d271bc7dd6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e5c3d7b12feee7e09497d5ca29f34f726009188c02bc2e50c7225cb4f3d88b34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236760695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a0b54fc75ca4fb7ab103ff5df5a6fdc354798ff5a89f2ee37e4c5fbe9ecde`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:08:27 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:08:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:22:37 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:22:37 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:22:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:22:57 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:22:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafcc59647295681d6450f088ef58ed34e24d6971f2f1e50b101f7692733d612`  
		Last Modified: Tue, 21 Nov 2023 10:28:45 GMT  
		Size: 103.6 MB (103598261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1a3e1478e38de75a1d9d9e200c40359b502133aa4aa9723c9a9ce58a4e499`  
		Last Modified: Tue, 05 Dec 2023 18:36:01 GMT  
		Size: 83.6 MB (83579592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13601bb83171f06de96af08dea2244dc351ff30637698832ce03910f188fb7d2`  
		Last Modified: Tue, 05 Dec 2023 18:35:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2fff529d6b784aa023c6e05c92eb6a392f7e88140ed652acec75ca86ffe1e386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235647305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a098d5736cbc21338e308507f89eddce665dacec5e221f5e7e9a3fab67615a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:21:05 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:21:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:39:31 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:39:31 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:39:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:39:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:39:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed78b2f6a939d9bf427c5f2e807ccac60d5947b296d683ccf2519fb74ff8df3`  
		Last Modified: Tue, 21 Nov 2023 07:39:58 GMT  
		Size: 102.7 MB (102701523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2c197054e4bc0068f8b27e1f948f52c79ec58c539b8b138ef9bedea1dc90f`  
		Last Modified: Tue, 05 Dec 2023 19:50:35 GMT  
		Size: 83.3 MB (83332511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d624d517da377bed350672ff552ffd1fa000a14ec823a9ca5968d193cef476`  
		Last Modified: Tue, 05 Dec 2023 19:50:26 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
