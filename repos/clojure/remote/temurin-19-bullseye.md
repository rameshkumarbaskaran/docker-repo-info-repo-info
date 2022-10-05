## `clojure:temurin-19-bullseye`

```console
$ docker pull clojure@sha256:4ad5e76c68f0504bbb6124b2c41c4747079f1b1fa847004b9cf9d31344fcf0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:30e651a979aa9589e16878d673b328274c06da84b53070d3192db2f4905f5829
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f6ea2c4d87c893eb3542e1801d356328e2ed2b7299dbd1df3ca4248ec9108b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:40:10 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:40:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:42:21 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:42:22 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:42:37 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:42:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:42:38 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:42:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:42:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39dc413a8bf8accdfa9d56cfc7b9aa47547fa5bfec61a15afe8626681e3df2ff`  
		Last Modified: Wed, 05 Oct 2022 01:51:46 GMT  
		Size: 200.8 MB (200843783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3520ae3d36c0bc3e4b43ac0aefebed665fbb9a9d2aa1b9d5a1b810a1b557bb`  
		Last Modified: Wed, 05 Oct 2022 01:52:53 GMT  
		Size: 47.3 MB (47295627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487d6c3e49fe6787ec0716194702c24368cbe902247e15b0442e4cb1dc34ae06`  
		Last Modified: Wed, 05 Oct 2022 01:52:47 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49207485a855f91d760e372a37f51c6867e0dce6dbeb1539c5193f19ef1213b4`  
		Last Modified: Wed, 05 Oct 2022 01:52:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4fbe125b2fd7184314ba1df371dbfa603102022430c40d8c5c94106bc37c8878
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e92e8df5a253118468117dedf60e385ab18777e5976e47e12fe13f8cd52aa7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:04:33 GMT
COPY dir:58f6c37df253d3555e493197f96e3f21593e31d3faf1967e0a7b9d8f0ae9e30c in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:07:23 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:07:23 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:07:39 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:07:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:07:41 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:07:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:07:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf37d84f42eaa21611ea540fea88bea6b18861b24ed7b7691a2ba8a5f87f4fc`  
		Last Modified: Wed, 05 Oct 2022 01:20:34 GMT  
		Size: 199.6 MB (199582867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4c63c14b094e88846b44c5ef8431a40b32092b23f5ca181e1bfe906127a35f`  
		Last Modified: Wed, 05 Oct 2022 01:21:52 GMT  
		Size: 47.1 MB (47086355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e185a433daef4f2f6476c101f5a7e14c110ca9c5df6ccf66d0a289a680966d0`  
		Last Modified: Wed, 05 Oct 2022 01:21:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8222a38a4c7ade1b787c326d787a67bef122c77bd8bf1d85abfc98381238844`  
		Last Modified: Wed, 05 Oct 2022 01:21:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
