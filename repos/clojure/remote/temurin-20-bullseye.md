## `clojure:temurin-20-bullseye`

```console
$ docker pull clojure@sha256:772747ab8d215dc4fd7a60d1c2a90dbc5f5d9b8b8c5a07065be2464abfefea58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:26db38ff91cbf949c6aa2f627204807fb431aef90a55203eea10a11a4415f3e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280742898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32f696e9dd5ed5b260427f9f1eedc878c9f72dcbb7294f00dcdf327462ece91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:24:49 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 23:26:03 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Mon, 14 Aug 2023 23:26:03 GMT
WORKDIR /tmp
# Mon, 14 Aug 2023 23:26:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 14 Aug 2023 23:26:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Aug 2023 23:26:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 14 Aug 2023 23:26:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Aug 2023 23:26:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7b3791075e937ca44303722209d883595c7671dd2a19c46338ac19c38a452`  
		Last Modified: Fri, 28 Jul 2023 03:33:09 GMT  
		Size: 153.8 MB (153791746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2f4e31dfe6d5de25935b9d8a2f045830f99a019faea60367290d6bbd8526`  
		Last Modified: Mon, 14 Aug 2023 23:34:17 GMT  
		Size: 71.9 MB (71894563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01c69b046b0cbfacad55a4556bea1b8b1266016065753175eb59220891f4113`  
		Last Modified: Mon, 14 Aug 2023 23:34:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ea0b8feda388ca283fd33ba3aeafac76f7557f1bf58af91064df6179386be`  
		Last Modified: Mon, 14 Aug 2023 23:34:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c883d98b8459c73f6219916a1d6eca827dfef90e3263b1c2533b50f67f06163b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277834629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023e851a504465552fa96ec99f72de937e08293a80c31431b7d3157a93105c4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:37:27 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:37:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Aug 2023 00:34:34 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Tue, 15 Aug 2023 00:34:34 GMT
WORKDIR /tmp
# Tue, 15 Aug 2023 00:34:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Aug 2023 00:34:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Aug 2023 00:34:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Aug 2023 00:34:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Aug 2023 00:34:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f9c63aa786ee3ab03231f07e1160261941272ad745ade935aa994d34f0dc9`  
		Last Modified: Fri, 28 Jul 2023 14:44:47 GMT  
		Size: 152.1 MB (152120124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2ff6c3ff8744ca8df4f2735b71d808f6bbfc17efa3ce5c11cc5d003bcad995`  
		Last Modified: Tue, 15 Aug 2023 00:41:10 GMT  
		Size: 72.0 MB (72008699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6124ac171a6a7a3edb0059f0dba9bc1e7ad69ec20c6c4d39f18e6e3bae77c195`  
		Last Modified: Tue, 15 Aug 2023 00:41:04 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c812b7d27ce16b08200c4f7d376a5afd60bb9bf3d38e2671b4bf3455075b534`  
		Last Modified: Tue, 15 Aug 2023 00:41:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
