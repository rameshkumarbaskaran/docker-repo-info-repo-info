## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:91e57c9b03d693acbe874a47c4861b532f187db8e117ed72dc44a0b2d93b49a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:980be92418e9b9979bd858f1c2e7d6563b7af02695f5c1cb90c23e9a1805ee6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261064861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0583b3d282fe856a6a598812451cec9fdfcddb353322194cddfe2a4103602d5c`
-	Default Command: `["boot","repl"]`

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
# Thu, 07 Sep 2023 03:20:56 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 03:20:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:20:57 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:21:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 03:21:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:21:03 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 03:21:22 GMT
RUN boot
# Thu, 07 Sep 2023 03:21:22 GMT
CMD ["boot" "repl"]
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
	-	`sha256:62e0582b58fe4b8ca74a9bc82538fd31957a0c2f995d877d8fcc513342b9b724`  
		Last Modified: Thu, 07 Sep 2023 03:31:13 GMT  
		Size: 2.4 MB (2362087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53438f84b4c6ddcdee4b60bf17639a04b54caa0e9dacafaf687cbf574450eb8`  
		Last Modified: Thu, 07 Sep 2023 03:31:16 GMT  
		Size: 58.8 MB (58820490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:180dc85a5c5617b5cb68447f7887c6a8ebe42fafab2f283dbb1003d62abb2aac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256447187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1784c706dc867f4aea147072f33baeb54a8cfa232c7962ebcc8aa050c99ea33`
-	Default Command: `["boot","repl"]`

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
# Sat, 02 Sep 2023 01:43:56 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:43:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:43:56 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:44:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:44:03 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:44:21 GMT
RUN boot
# Sat, 02 Sep 2023 01:44:22 GMT
CMD ["boot" "repl"]
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
	-	`sha256:45c5d1cd432757a32b7e23e3061b5bb2748eaa9dfedf7497d88be9e5e34540ca`  
		Last Modified: Sat, 02 Sep 2023 01:53:04 GMT  
		Size: 2.4 MB (2351483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb07bb527fd33975fe235895f466438f89f0ae1fbdb69eb8a00ee2d745c094c0`  
		Last Modified: Sat, 02 Sep 2023 01:53:06 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
