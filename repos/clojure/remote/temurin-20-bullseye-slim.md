## `clojure:temurin-20-bullseye-slim`

```console
$ docker pull clojure@sha256:67b53034bb68ff05c88d935d3f12b46977f0ab272b28bfa30c0ab77c6bd4324f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3946ec663d7706cf1d6760ca2b0f9fb4ab186339bee78d119d2d2b560525f8aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246711692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31c7107f670956ecfdaeb09a67ac39d792025700aa38b88c91c72b6b9cba141`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:36:02 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:36:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 01:36:53 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Wed, 16 Aug 2023 01:36:53 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 01:37:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 16 Aug 2023 01:37:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 16 Aug 2023 01:37:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 01:37:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 01:37:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566987b9dae8e5a20c4a3b1a42a6bdf8a8a7b88a5990e626224c1547e0050b0`  
		Last Modified: Wed, 16 Aug 2023 01:44:52 GMT  
		Size: 153.8 MB (153791733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7aaad8e169408a45420d49fefed12a203a847b93228b734ff4b9ce382922a`  
		Last Modified: Wed, 16 Aug 2023 01:45:32 GMT  
		Size: 61.5 MB (61501265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83198c5a84573f04844c9c9abc74709d806c1b40a28f817bf7d13a3bd4f01d4`  
		Last Modified: Wed, 16 Aug 2023 01:45:24 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c886d45058e9b53cded3a702d140c9d069895e33e696528e4b72aeb96dfd843`  
		Last Modified: Wed, 16 Aug 2023 01:45:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d79266aa5fdb6fe4d615bccc708696edf94df7614c2239a74f697b5fafe78b59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243796358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0814599361842ef603a4ce2b283614edcf8c79342aff04ae788abd5537b561`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:53:50 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:53:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 19:46:44 GMT
ENV CLOJURE_VERSION=1.11.1.1405
# Wed, 23 Aug 2023 19:46:44 GMT
WORKDIR /tmp
# Wed, 23 Aug 2023 19:46:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "e02966d807e5fcee40d3aeee823196fd296cb97e91746f444ac8c6681731b354 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 23 Aug 2023 19:46:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 23 Aug 2023 19:46:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 23 Aug 2023 19:46:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 23 Aug 2023 19:46:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b04b4e3bfe044338b1636c6d1fe76f6e2c078f769b995d868ef50c1b27e924c`  
		Last Modified: Wed, 16 Aug 2023 02:01:19 GMT  
		Size: 152.1 MB (152120026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229b05f4fcbc561aca869669b82997e0ac596851adac25d508c4cacef238f4fb`  
		Last Modified: Wed, 23 Aug 2023 19:53:00 GMT  
		Size: 61.6 MB (61612498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8e80e93a2efd5cf58bf98575295acf209b92eb2862a43b0b3ca8fb66bea575`  
		Last Modified: Wed, 23 Aug 2023 19:52:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fbf0a1192211573ddf0becdf706b4fa10eb7dc4865a5aba0cf0760afe906c5`  
		Last Modified: Wed, 23 Aug 2023 19:52:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
