## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:b73e723ec1ef546344684770f7bfa83554d04b5a48a2c2964d25da83c92f21f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6869a5fd70eb40cd84e7f378c2ee10063d455d9aec4106d1e2bdc3ce83090ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145945059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071404a1e7b371d40da4a8c0fe6e8a1a47d5e7871fb96ae21bbf40f496269279`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:22:39 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:22:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:22:39 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:22:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:22:40 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:22:45 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:22:45 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:23:03 GMT
RUN boot
# Thu, 09 Feb 2023 09:23:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff09d33db7932dfdb13e1ebfdd9d02620a26713de0236d8aef1f5d2e115b133`  
		Last Modified: Thu, 09 Feb 2023 09:36:59 GMT  
		Size: 54.6 MB (54635563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0d2df04ebc3f16cfa2fdfd3b38c2cc57f43e096aa636ca6890150d6ee862df`  
		Last Modified: Thu, 09 Feb 2023 09:36:52 GMT  
		Size: 1.1 MB (1077361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3226138d3d8ae22581284220c2ab32e76f9d06c04f982ff80d98ede98c3e421`  
		Last Modified: Thu, 09 Feb 2023 09:36:56 GMT  
		Size: 58.8 MB (58820325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2dc8211e3d71eaf1e0faef70eb2c3da4e2480f2e3d54801964761e7c845ce760
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143675745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3499c3fbcde931e1ee8a0cf0387472e2f159e364c9521b1df4620a3df1219231`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:02:03 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:02:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:02:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:02:05 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:02:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:02:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:02:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:02:27 GMT
RUN boot
# Wed, 01 Mar 2023 03:02:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ed8d1b5c6c501960add7e45237e7cb7c527399c9fe073375eb66890797d9b9`  
		Last Modified: Wed, 01 Mar 2023 03:14:20 GMT  
		Size: 53.7 MB (53727906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b5192d322c72ac1942a42e12b349b6632720946eb54472879c5db6d7b7dec`  
		Last Modified: Wed, 01 Mar 2023 03:14:15 GMT  
		Size: 1.1 MB (1064601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce4553c2f0d322233ac3dcb0af1dcaf3dac59ee6f754696fa4ead955032cc36`  
		Last Modified: Wed, 01 Mar 2023 03:14:18 GMT  
		Size: 58.8 MB (58820424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
