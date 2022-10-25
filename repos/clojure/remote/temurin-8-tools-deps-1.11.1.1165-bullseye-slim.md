## `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye-slim`

```console
$ docker pull clojure@sha256:fce9760c7ed4c2b4335c1b0dbbec42d0d149150a0177b11b806ed6734970a416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:efce34a577f94efec0510dccf37f03d3f295d73310cfc5ed2cada232b57494a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196406739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59debb3f07e3ff0c769d66b918afd0ea6feedad0aec55b8bbb1c2abe0f464a11`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 02:33:27 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Tue, 25 Oct 2022 02:33:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:35:35 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Tue, 25 Oct 2022 02:35:36 GMT
WORKDIR /tmp
# Tue, 25 Oct 2022 02:35:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 25 Oct 2022 02:35:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 25 Oct 2022 02:35:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8fc7384965746c1eff2e3c90a689ae0048d4ae23d30592f0dd0e23c474bc5`  
		Last Modified: Tue, 25 Oct 2022 02:48:26 GMT  
		Size: 103.5 MB (103513848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87c418e89a8a4b0311de2819c4fe82f896b4b185460701b69114f85d6a6d85a`  
		Last Modified: Tue, 25 Oct 2022 02:49:32 GMT  
		Size: 61.5 MB (61472234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223ab33866a9267fccf60bf001d5cea904523ebe09318a041690cc4d89bb0d8`  
		Last Modified: Tue, 25 Oct 2022 02:49:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5797eff26d82da40d7e82c428e5df50d8279ebc2c1b50db7e400a2e445d7b9ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194071584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26db61bbac45079d1e9076368c9ec0a69ddfa6e0e1122d11e93cf427e3d3bf2f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:54 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:56:19 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 00:56:19 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:56:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 00:56:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 00:56:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911611afa665b0683fbe96bda4abb9185fe2c620cdfcc9b8a6381b9fdee36056`  
		Last Modified: Wed, 05 Oct 2022 01:13:35 GMT  
		Size: 102.6 MB (102613711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be159d2e8ac3bb01bce97a65c807aaa806e8dc7647aecfd7debc502bfc1bf345`  
		Last Modified: Wed, 05 Oct 2022 01:14:48 GMT  
		Size: 61.4 MB (61392860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e7c2eaeb4d25b5876c2b5dac80ff55098bd70f1eb0761014456585e870afe0`  
		Last Modified: Wed, 05 Oct 2022 01:14:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
