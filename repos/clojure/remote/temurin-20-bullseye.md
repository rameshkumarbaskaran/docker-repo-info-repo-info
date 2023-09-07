## `clojure:temurin-20-bullseye`

```console
$ docker pull clojure@sha256:5a9743837834a016f6e4588f35d22bd2daee48f3c9979d3f88752795603bd1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:51046385f7a6000944bf7470e729d7b2061fad05786aa53d96ae9e64b792d7c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280726862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e18f73ca62632d6d923b0a7a0a8bf6da8ffa5ea073defd56ff1fb97c3bf74f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:26:28 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:26:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:27:23 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 03:27:23 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:27:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 03:27:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 03:27:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:27:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:27:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b8f8faea9607c7f73e95f0ee15b0fbfb23b2a90f8f727324186bc69f7be1ef`  
		Last Modified: Thu, 07 Sep 2023 03:34:59 GMT  
		Size: 153.8 MB (153791682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09006a8b14faaaa2ad326d966e4d3af07d6fa74f76b3c08fe62f4838569cce12`  
		Last Modified: Thu, 07 Sep 2023 03:35:41 GMT  
		Size: 71.9 MB (71877919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babfa3c5eda8775a396a067307ebbf6e6696853ec72a4ff7978b01c1c2c35849`  
		Last Modified: Thu, 07 Sep 2023 03:35:33 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977322817dfe7c4c4a14bb4bc76766cfde064e422f94421a046c515fda02009a`  
		Last Modified: Thu, 07 Sep 2023 03:35:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04455b9af88d623b533a75a4cc269b15932139fed2d096f8473cb3bc9c4adfc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277823825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4903c522859d8ccaed155e230e76c29bb4355128b1a102d10b3c23bf05ad99`
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
# Mon, 28 Aug 2023 19:44:59 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:44:59 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:45:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:45:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:45:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 28 Aug 2023 19:45:14 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Aug 2023 19:45:14 GMT
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
	-	`sha256:6df2c17c8ee0de1b81493b99eed744c22d5c5eeb0d6dfbb0ef6997f1ae6adbda`  
		Last Modified: Mon, 28 Aug 2023 19:51:24 GMT  
		Size: 72.0 MB (71997997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43d20586f7a257d1d5aaed75961b667b1406a15b11ef7a33f955cba0600433e`  
		Last Modified: Mon, 28 Aug 2023 19:51:18 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f7f31131fd300581d844f26d7b606a96a5d92a553fc796e63e57089e5f27aa`  
		Last Modified: Mon, 28 Aug 2023 19:51:17 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
