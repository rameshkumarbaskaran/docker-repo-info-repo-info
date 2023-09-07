## `clojure:temurin-8-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:ca68a30f44d2e836922db88287f06594b4b58bd36f696d2fb8758de084c69a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1413-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a6f270b4314a58cfb6d7adab1786eecfdebec0bc87ec9c6a298b7c7a517043ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230519640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fa488bf282a3515c0438f6dc3d63906aa87bf2eac610962eb92145a0f71109`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:17:26 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:17:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:20:03 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 03:20:03 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:20:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 03:20:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 03:20:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b481a024ba4d33f0e597e2fced4d71eab6fc3c8ebf663470405837b953224`  
		Last Modified: Thu, 07 Sep 2023 03:29:35 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457cfded810730e66caa978fdbf48a5862f61deb8daba359b2f9ae174930f3b1`  
		Last Modified: Thu, 07 Sep 2023 03:30:39 GMT  
		Size: 71.9 MB (71877719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae00e382edb0f8ff17119dc321f99680c6ae5aba02568c5b8d59a14aab7e389f`  
		Last Modified: Thu, 07 Sep 2023 03:30:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a49b6c0335cf51cea014be6731e3dc24a834f5981a2cca7824f3cd93cbfb2f07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228393682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041a0e9ce06c35cfc4a58ba9c466f1eb63e179c6c3285aaa73054168ef0a4229`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:46:16 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:46:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:40:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:40:19 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:40:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:40:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:40:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e72ffee157aface2093ca7b44ca1e9d7d8010e8b3344c5760c1ae633be3d0`  
		Last Modified: Wed, 16 Aug 2023 01:56:15 GMT  
		Size: 102.7 MB (102690463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748cd1a0103b904db491d832eb8a776e6e4a331fdde30a01908d81bf07e00a8e`  
		Last Modified: Mon, 28 Aug 2023 19:47:19 GMT  
		Size: 72.0 MB (71997821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03916d44b232125c3ec91166af93fcca3ddf3d81e34c54a652c5e4f880b0b41a`  
		Last Modified: Mon, 28 Aug 2023 19:47:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
