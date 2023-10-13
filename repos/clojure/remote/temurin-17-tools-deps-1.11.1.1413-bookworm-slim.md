## `clojure:temurin-17-tools-deps-1.11.1.1413-bookworm-slim`

```console
$ docker pull clojure@sha256:96449545c36c86f79d72c30c3bae95fc6a9b4ed6bf5b984bcff3499469a7eb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:64d4b8fa25ef83d1be9e6e6da732170d88ac64c35bedb05eac48a3ece3671258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245859931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f561b9912552d813eda5e5914fdb402b2cc1a69ce80911db7c8841f2239d19e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:52:38 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:58:12 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 12:58:12 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:58:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 12:58:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 12:58:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:58:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:58:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a34b75927f2306868c4a7fe1a7e58cbd84682bb3f607d3c9b61603d11b9ef3d`  
		Last Modified: Fri, 13 Oct 2023 13:10:13 GMT  
		Size: 144.8 MB (144775764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913aad8cd3e361f21c5b0e640140ee89097b37d32ea32c8c1fb78dd79ac8680b`  
		Last Modified: Fri, 13 Oct 2023 13:13:21 GMT  
		Size: 71.9 MB (71933277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4e7cac1422ddd32cecad9a7b596f294ce6e02d200de1cadacf3c454676b196`  
		Last Modified: Fri, 13 Oct 2023 13:13:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed35f744610fb4b8b2a7c5221d51fa9da7a84cb47bf49839a269cc6c33a125ed`  
		Last Modified: Fri, 13 Oct 2023 13:13:13 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1413-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a578e83848ff55f37e7968d8cc622ba18e81e44e42924ab3c319b40d0e337c9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244418565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772016f79b2d7c9138858baeefcca945bf6fc7cf87b53c44145d0628b97f813`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:19:14 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:23:36 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 10:23:36 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:23:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 10:23:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 10:23:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:23:52 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:23:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff307ae0c323a4d6fd223fe9031e67bc368768a88263d2cc046c321b0bcaacfb`  
		Last Modified: Fri, 13 Oct 2023 10:34:23 GMT  
		Size: 143.5 MB (143543485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b6d8c345fe2d912ae308c98e8aa3424afb6dd845b5213acf052c39a0800f1e`  
		Last Modified: Fri, 13 Oct 2023 10:38:20 GMT  
		Size: 71.7 MB (71694783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d898b82b2777db2ce3668d820844e2fce7e12950789aedfaab6000f42d3e28ec`  
		Last Modified: Fri, 13 Oct 2023 10:38:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46bb4620526862ac885b60d56ef19d19ab7fb0740d3a2fef81e354196f4041a`  
		Last Modified: Fri, 13 Oct 2023 10:38:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
