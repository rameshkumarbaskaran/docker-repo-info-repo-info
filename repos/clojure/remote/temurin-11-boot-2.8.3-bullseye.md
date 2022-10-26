## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:814a3a5ef0c703a853cc1ecd1f3a52cd6bac50c78b4294528f4203090f4f0fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:be65e4e3240ffb28b0ca84b73ee382579cb2e4f04d07ddd1ec26915f8d3bec75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314353546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b20df6463d9c29f671237e1d60b83ecbf5b3446fc6f952c22cc3917fd67570d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 21:49:24 GMT
COPY dir:80db6f3290e8de5c875b6f069ca1d81f6b5c9f4e34668a64373c380a024a607d in /opt/java/openjdk 
# Wed, 26 Oct 2022 21:49:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 21:49:26 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 21:49:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 21:49:26 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 21:49:33 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 21:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 21:49:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 21:49:52 GMT
RUN boot
# Wed, 26 Oct 2022 21:49:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4b022db123128ccb656b9ae699590cbed8128c83fbb885ba312cca0b50a90c`  
		Last Modified: Wed, 26 Oct 2022 22:07:00 GMT  
		Size: 198.1 MB (198124727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4883be2ddf5ce7a1b9e2e045177ec9bb23b0169d8d87c63cfe02c741466d54b3`  
		Last Modified: Wed, 26 Oct 2022 22:06:46 GMT  
		Size: 2.4 MB (2362053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585ea4a33aa9f8de753ed79d5b74646e1bec9ba5e36f2b081d6695c6de86f237`  
		Last Modified: Wed, 26 Oct 2022 22:06:49 GMT  
		Size: 58.8 MB (58820434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f1ef1f4bd872b8c3f4e7a7be7de1627612dcb4b164b7ceef2b12a797ae48f75c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309741625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9905c3d15ef4afc7f91b5153f0718516d388ba8687c584e1e239ef7661b08a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:37:43 GMT
COPY dir:0c9c8c2b9cd43799d246d5824c591352650ad79f5d15544287f00c2deb1e4608 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:37:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:37:48 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 15:37:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 15:37:48 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:38:06 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 15:38:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 15:38:07 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 15:38:24 GMT
RUN boot
# Wed, 26 Oct 2022 15:38:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7a7b51e23fc2e53d8018b07b36bae7b1c261267f2981e18b50be0d7b845881`  
		Last Modified: Wed, 26 Oct 2022 15:57:42 GMT  
		Size: 194.9 MB (194866970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef805b45caa2352f0f6905bf81b99263dbfa1b2fc932d475262693899c9c708`  
		Last Modified: Wed, 26 Oct 2022 15:57:30 GMT  
		Size: 2.4 MB (2352281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6147e6b271780d0ec957d2ebd037f7caf814481713593d41c81e00f327f086f9`  
		Last Modified: Wed, 26 Oct 2022 15:57:33 GMT  
		Size: 58.8 MB (58820408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
