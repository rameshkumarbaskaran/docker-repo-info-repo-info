## `clojure:temurin-20-bullseye`

```console
$ docker pull clojure@sha256:1068ed5b173197b0f64b49804043f1e857e8afec6fd5adc8cae7facb13f8ee43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0a737a5d0e919ccfa7950cdb8ec9a58a1f9c14c1f5929d3a414acd5dc385eec8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280743954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc69623d3d6e81e36bb7f2481c309f61b6288e2fe8fa09541c40e0efdacca51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:35:34 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:35:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 01:36:29 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Wed, 16 Aug 2023 01:36:29 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 01:36:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 16 Aug 2023 01:36:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 16 Aug 2023 01:36:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 01:36:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 01:36:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90caec4e7b99b48f1f89782ec874bda17eaa1c0668d0881c12015fed8413ae7c`  
		Last Modified: Wed, 16 Aug 2023 01:44:30 GMT  
		Size: 153.8 MB (153791716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09a9c1d19514547b4cf950d86af8724e7c9b9e58454b61b9d0a020ce7546445`  
		Last Modified: Wed, 16 Aug 2023 01:45:14 GMT  
		Size: 71.9 MB (71894600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9864f1f7ada09ac5a444d80d1d9163cf8750c574a5aac779232b2391af2e7b1d`  
		Last Modified: Wed, 16 Aug 2023 01:45:06 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8798e54cf0c494935bda0d08e61c1fadf936b58e17db1cdede03ebd8f56ed8ab`  
		Last Modified: Wed, 16 Aug 2023 01:45:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7652270d5f6e9b159fe11d5a08698e67d4bee625222dc229b346489507f6745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277824581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18c66e4e404e58f0045eb376485502ca95d3614adf01ed3f588f90d28d186ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:53:28 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:53:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 19:46:24 GMT
ENV CLOJURE_VERSION=1.11.1.1405
# Wed, 23 Aug 2023 19:46:24 GMT
WORKDIR /tmp
# Wed, 23 Aug 2023 19:46:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "e02966d807e5fcee40d3aeee823196fd296cb97e91746f444ac8c6681731b354 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 23 Aug 2023 19:46:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 23 Aug 2023 19:46:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 23 Aug 2023 19:46:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 23 Aug 2023 19:46:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80577829fd2ca0f87088aee439e2af91b6b5d473c01321aca658e856bb10ee3f`  
		Last Modified: Wed, 16 Aug 2023 02:01:01 GMT  
		Size: 152.1 MB (152120028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f15a3b1ebd3f8f8b77b7d2f2c2a78c4c3eb35d9a833888df2cf646cacdf1221`  
		Last Modified: Wed, 23 Aug 2023 19:52:44 GMT  
		Size: 72.0 MB (71998758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d42bf326fa4bf7b2ef9f35ac59410a81b0b5941347be0b0ea017611d5d941e`  
		Last Modified: Wed, 23 Aug 2023 19:52:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dac715b334a5357cbab09892b7afc7457f15c78bdc5786876ecd84ffcab5cc`  
		Last Modified: Wed, 23 Aug 2023 19:52:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
