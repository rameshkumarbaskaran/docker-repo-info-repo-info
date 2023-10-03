## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:dda362a93563420efdb46fb82d0fb467f250a089b2118a3ac58b64d171332930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dcc52969556877f9b6e77b7f86e98cb5db659af2890bb6a154ceec0d265836ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237738783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b576d9106d35d0da5a848637c194eafa39d66e09917b8011a521a5f43ce8aff6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:37:40 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:37:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:40:20 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:40:21 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:40:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:40:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:40:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9489ff926f0d6a8ba20abc78a9461fc70a87d4c0a043fb72a95b43934f07a8ac`  
		Last Modified: Tue, 03 Oct 2023 08:54:16 GMT  
		Size: 144.8 MB (144825998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7fd6a25a29e46453476949e2184d0fb979e329c4b7086e919070537ef30f72`  
		Last Modified: Tue, 03 Oct 2023 08:55:45 GMT  
		Size: 61.5 MB (61494455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a614abf6b442e5c48f33f4105b99fcb23d0ab2c67ed72e340228c730d48ce2f7`  
		Last Modified: Tue, 03 Oct 2023 08:55:37 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aed63ca697f8d2ef237afc2850d258de673a637c683411f15b942c3b5820f2bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233245566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b2835fda64de1434fef4455ee3b834e42c25aae5ca83ad6395bea2d1614bd`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:48:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:29:03 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:31:25 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:31:25 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:31:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:31:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:31:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1c21e56e06bf88aefd6edb1d9b40ca84fb99f8862f7f24beff9111809ec55d`  
		Last Modified: Tue, 03 Oct 2023 08:38:43 GMT  
		Size: 141.6 MB (141570687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c85a1bd6fc2d2ac5a2a13565d7f37242d42eb7a89b96d9b46eb747b3e33d991`  
		Last Modified: Tue, 03 Oct 2023 08:40:14 GMT  
		Size: 61.6 MB (61611392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed988a4c2224aaf09daa0c677e67a5aa4ffc98c0424ff8acff4c6deb4d5a88`  
		Last Modified: Tue, 03 Oct 2023 08:40:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
