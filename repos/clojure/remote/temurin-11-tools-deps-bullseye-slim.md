## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:2d33e28080670555e2bfc4bda4a2c6d47e590cea07136dbb784e58967c9f3183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:66dea8de495d2924feb0a421cb6dfb1377bbac7bc6d7977bc8d5a66656cafdd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291015629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59711c412ea54bfea0698b3b06326ce912e56deda5fdd5d4e875596a767e936d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:34:29 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:36:28 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:36:28 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:36:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:36:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:36:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd943cda847b9f3402014ae85cb3f413d8a8197a5743326a30702a399bd52788`  
		Last Modified: Wed, 05 Oct 2022 01:48:04 GMT  
		Size: 198.1 MB (198124862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab92fbc096fcc5b2fee2eecbd50e99c0a7cb2c432448be7b7934b7f16f3e466a`  
		Last Modified: Wed, 05 Oct 2022 01:49:05 GMT  
		Size: 61.5 MB (61470046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e9a170da62c3d84a4ca7db3bb19da9b205301cf0a4d4a0f50fcb7f2ba8cc0d`  
		Last Modified: Wed, 05 Oct 2022 01:48:57 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5f3f95fba74d1a080c3a851bc913598dff173c7acfd3eaf71cf0004c6abe3aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286325360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9e720399400f7e31da2840af08b0ac3cf6fbb1ce41f95085e1ef622815d662`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:57:35 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:57:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:59:57 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 00:59:58 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:00:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:00:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:00:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36823226c948e675df283a37335f66a71f8cd0ad8b4c380702959a9b3a6be822`  
		Last Modified: Wed, 05 Oct 2022 01:16:11 GMT  
		Size: 194.9 MB (194867812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bd021c4ec25f7b058938e8c61211eb29ada3fc1373c10432e73f2817b57760`  
		Last Modified: Wed, 05 Oct 2022 01:17:23 GMT  
		Size: 61.4 MB (61392537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a28c489bd22cf26568b4b28d38fb19a4529f3fc478b5f5ce2eddd5f0be22c`  
		Last Modified: Wed, 05 Oct 2022 01:17:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
