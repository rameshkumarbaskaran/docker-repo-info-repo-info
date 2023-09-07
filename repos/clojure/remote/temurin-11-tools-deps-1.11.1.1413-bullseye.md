## `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:3769ff6ca478a55254b1dbd679c1acf17c089aa4a795b35b08b9210ee8604412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6766da3023064f242c2fe672c232617303be14098e378d5e89bb54bef9ec52c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271760634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94c8cce1421c94f195b4ead4547f445d460b49f76fc2a3b86399afc462c44ab`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:20:55 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:22:50 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 03:22:50 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:23:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 03:23:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 03:23:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8362383bbb2a2ea92c13e5f54adadd9254bf381fbb68440756c92f4b29b02058`  
		Last Modified: Thu, 07 Sep 2023 03:31:24 GMT  
		Size: 144.8 MB (144826039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7f6d6eccfdb35bb0e77c40e9a551647639198945268bd00a64f177b3a7acc1`  
		Last Modified: Thu, 07 Sep 2023 03:32:21 GMT  
		Size: 71.9 MB (71877733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f57038c74c67899ef2c8ab0ac7d2abcbc2ba38ccf023f8e90807f7af4e05a93`  
		Last Modified: Thu, 07 Sep 2023 03:32:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49df5b68b7e7b4c5010f94f32e07bfa0feda5142d75d369964148e400507d7ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267273833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d549e7bcb12eb2ce1362bc89f2029edb509b950ae6d4d060176e78e7d840517`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:43:53 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:46:28 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Sep 2023 01:46:28 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:46:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Sep 2023 01:46:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Sep 2023 01:46:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e4e3a8bbfd2bdf093ae59fc74ef766b5e27c2748069f457d192d1719121d34`  
		Last Modified: Sat, 02 Sep 2023 01:53:12 GMT  
		Size: 141.6 MB (141570380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be118cfdcade305e8a5111ac50f573481ddd614eb60ef654556fe58585c458c7`  
		Last Modified: Sat, 02 Sep 2023 01:54:31 GMT  
		Size: 72.0 MB (71998055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5e2365ff1d842171fbcdb71109bd19445d0ebf5bb4087a9464d5e70ab33a8f`  
		Last Modified: Sat, 02 Sep 2023 01:54:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
