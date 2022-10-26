## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:fcba121000954d0a0ec3f8e8d2361c6a014f3109838741daeaa84d2cb6d1c1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:228ee354e686b05c97a847afbaa1284526c4ef1575dcf3d5542f3f429df3e9c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285030153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b2e3116bb9bbfda300e366bd93d715d2ee4056d696c79ca8f952ebfa35d0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 21:55:22 GMT
COPY dir:b50a87fd6710a805ef25d6c1dd2c5f7aa37ef63d04ab1c00c91801848dae94f0 in /opt/java/openjdk 
# Wed, 26 Oct 2022 21:55:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 21:58:18 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 26 Oct 2022 21:58:18 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 21:58:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Oct 2022 21:58:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Oct 2022 21:58:36 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 21:58:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 21:58:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e670a3c00fcddd4db26555e9c844d563ed2f95a3a416c451f078b9d2826bd660`  
		Last Modified: Wed, 26 Oct 2022 22:11:01 GMT  
		Size: 192.1 MB (192137485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39ef442a279e7eb6531fa7c5edb4cf89b089290bc7ae994b8471ef95df77761`  
		Last Modified: Wed, 26 Oct 2022 22:13:25 GMT  
		Size: 61.5 MB (61471610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccec68c01934551ec16f475b078b4c60c0c1e99e1b675510854db7a507db141`  
		Last Modified: Wed, 26 Oct 2022 22:13:17 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb192145cda1a23e7aacacaab20380e79ed63ff7c08ed5a763147a408bf435ad`  
		Last Modified: Wed, 26 Oct 2022 22:13:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c54badfc9df1dd8e237006a885a8e5d3559ddf81f21940d84731acb2a5bcc60d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282561344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105309599e6785147267ba468d067a051b33ce82d12427e8b04166840229934`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:45:22 GMT
COPY dir:580c509aa131da1d31de9db8eed968c1f0ef93ad270f258b0b43d9d7d72bba84 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:48:02 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 26 Oct 2022 15:48:02 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:48:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Oct 2022 15:48:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Oct 2022 15:48:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 15:48:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 15:48:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5227b5452ba825facdc158312391c195512969f1ab7a485e56b2a432c2fcf433`  
		Last Modified: Wed, 26 Oct 2022 16:01:26 GMT  
		Size: 190.9 MB (190904076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50bc991f776f30364e63a7c939321010aed25533122665d051779bcdbd59e4`  
		Last Modified: Wed, 26 Oct 2022 16:03:45 GMT  
		Size: 61.6 MB (61592341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082186c33c35abe6a621dbfa61da5eaacba4dbd47f9fbfc712257f9ac1789bea`  
		Last Modified: Wed, 26 Oct 2022 16:03:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50888f14a951bfa32cd86294ed1dc41f40c9292a5cb971a61f36003b2b7b0e23`  
		Last Modified: Wed, 26 Oct 2022 16:03:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
