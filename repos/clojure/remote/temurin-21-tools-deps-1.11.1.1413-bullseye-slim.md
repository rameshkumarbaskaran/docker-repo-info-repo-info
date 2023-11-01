## `clojure:temurin-21-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:7a6126b5368832f3a2ca0d6d36c11cab7a0fce5788a6ac5a8129cbd329d4ec2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.1.1413-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:49a74ea94256c1aea6968eb904e87ec6e5e6729690032f7afe4bf0aedce62ea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251553040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac1b4911935f96ec2b5b983bc4c14ebdc10c570fffe090df8280482a8fdf21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:28:41 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:28:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:30:13 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:30:13 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:30:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:30:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:30:29 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:30:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:30:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bf17cf2c726bca323c64986cb4cfabf5e168faf86ceb9906f3ec18029103da`  
		Last Modified: Wed, 01 Nov 2023 01:44:34 GMT  
		Size: 158.6 MB (158630598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bc71cb4bb7ac7d4c2277398d361a197b89e0027d7879d4ff662c35331b9b3`  
		Last Modified: Wed, 01 Nov 2023 01:46:14 GMT  
		Size: 61.5 MB (61503513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e8f468d5df04103a09c09eeed8bdc2bd5cd72095da3f6bc7f5fe5e434c7ec`  
		Last Modified: Wed, 01 Nov 2023 01:46:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8501492293db1cdec8f5cc7099a2de8893a8379f414e0571288131b265d540`  
		Last Modified: Wed, 01 Nov 2023 01:46:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:134c44ca6e9376444a2d8f39280835635eaf6705b5fe7941f226374077faf9a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248557537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66396f2541d3b48ee136c35815607efaa7c06d1aad3634a7dbb018ddcb82d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:12:30 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:14:08 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 31 Oct 2023 01:14:08 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:14:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 31 Oct 2023 01:14:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 31 Oct 2023 01:14:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:14:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:14:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ab2c4a6a483c8978c14f7ed4bdd931493c1a12faa7bb05299aab3abfefa93a`  
		Last Modified: Tue, 31 Oct 2023 01:28:22 GMT  
		Size: 156.9 MB (156872111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfc5abbf33535aeaab48296e6d7a49bd9dd0380142769fc61a9fc8e4e2bb696`  
		Last Modified: Tue, 31 Oct 2023 01:30:03 GMT  
		Size: 61.6 MB (61620325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596e29c52583aa09cf3d59d99384ed37aa8dd03174f35ba5ff1db707ffc88753`  
		Last Modified: Tue, 31 Oct 2023 01:29:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75480b24b4b1e52b8c1d22f04204ebd02deb57785411f887f28c2ce64ad982c`  
		Last Modified: Tue, 31 Oct 2023 01:29:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
