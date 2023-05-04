## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:6552918fa6eb646743518b0fafd086dcbcf88e51ed557b9f9b60e33bdd383e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:76a50f2a33c02c65f852481a4829754d7397ac9bdcbf1d028b6af612f53bb4d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314780705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d9170f8b6fe816da231e9556cddd66f6af9509291b966d448b3eb776bdfa5d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:26:50 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 03 May 2023 20:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:26:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 20:26:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 20:26:52 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:26:57 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 20:26:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 20:26:57 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 20:27:15 GMT
RUN boot
# Wed, 03 May 2023 20:27:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127538ce586198e269e9a4ff9f0268aed32fd316a7287fcdb85700312b200f6e`  
		Last Modified: Wed, 03 May 2023 20:36:35 GMT  
		Size: 198.5 MB (198549535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ab9e27586a945aa99c3e6710fbd98bba8646fb2f613932b0a9f96083ff8e04`  
		Last Modified: Wed, 03 May 2023 20:36:22 GMT  
		Size: 2.4 MB (2361635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f5c8f23108d414447d74694d952cfa1620310a2bedb9dbe2bb43d9d63f88bc`  
		Last Modified: Wed, 03 May 2023 20:36:26 GMT  
		Size: 58.8 MB (58820465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e044ae720bb4047f916e9b9e5ade8d9ea5e43c4861800c11893d3a3d4cf6efd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310188542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959fe7a918d60e4352604973ac6f1753cfbe6a5454e5d0c40e67831ab2812c8f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:06 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 10:10:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 10:10:10 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 04 May 2023 10:10:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 04 May 2023 10:10:10 GMT
WORKDIR /tmp
# Thu, 04 May 2023 10:10:18 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 04 May 2023 10:10:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 04 May 2023 10:10:18 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 04 May 2023 10:10:34 GMT
RUN boot
# Thu, 04 May 2023 10:10:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750c5a6a1f6f22a3a543fac8f9799adc5539c91b044752b8b8e66c73d3c5014f`  
		Last Modified: Thu, 04 May 2023 10:19:50 GMT  
		Size: 195.3 MB (195324193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f75db5ff7307ee8710833cb9d3993b6995937a622cfe41a44941d35972cabf6`  
		Last Modified: Thu, 04 May 2023 10:19:36 GMT  
		Size: 2.4 MB (2351152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40701ea4688eb1f5e829b4c0424f351ffdac4a7be2060bc5d4de16bbbb34b77`  
		Last Modified: Thu, 04 May 2023 10:19:39 GMT  
		Size: 58.8 MB (58820492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
