## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:10cc7e5f09a99262edc7b32960683aefacad0451f3fa46df160fffdfd840bd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1fe00aec137b5f8b6871aae1ecc75742387991c35528d1d304e5b60017f2abc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314787074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268e40203262e40d2556934ebbf1fea57951b32efdb16057d8c409c6417d2a3d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:03:00 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:03:02 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:03:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:03:02 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:03:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:03:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:03:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:03:26 GMT
RUN boot
# Tue, 04 Jul 2023 04:03:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b5fb32c7c13fc3044e1370f05931aae1497f5be699a0ec5bf4c0e665c4881`  
		Last Modified: Tue, 04 Jul 2023 04:13:22 GMT  
		Size: 198.5 MB (198549439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3def4527e47ef333285ccaa3b9cbbe86fe95f3dbf96acf1f91a257015dba13`  
		Last Modified: Tue, 04 Jul 2023 04:13:09 GMT  
		Size: 2.4 MB (2361935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b97c71b5d05d701a169e501fe9ae9e90ba8fab91e7e8f16d079d9ab7a68bf9`  
		Last Modified: Tue, 04 Jul 2023 04:13:11 GMT  
		Size: 58.8 MB (58820400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cddb6a97d25f6bb310f2513142fa78d2614b04cc69741863ad431df086d513c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310200157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938afd346d234ef5f4a0a358acc4a8da5d324bde84444d16d25560bdf710e314`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:35:08 GMT
COPY dir:46f070668c95bcfc449ea3e3aa03838e4c3f9939658e6aebe91ca179e673aded in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:35:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:35:13 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 03:35:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 03:35:13 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:35:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 03:35:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 03:35:19 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 03:35:37 GMT
RUN boot
# Wed, 05 Jul 2023 03:35:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c920af0a750cfe7216c4049f78b2268ce2ca834ae686e6958f0239f3f792261a`  
		Last Modified: Wed, 05 Jul 2023 03:46:39 GMT  
		Size: 195.3 MB (195324201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68132594b49b4f1b7568a81ebb8cab010723982f9cbde6cb20ad6ddef419a9bb`  
		Last Modified: Wed, 05 Jul 2023 03:46:28 GMT  
		Size: 2.4 MB (2351394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9805f9c34a1f730b09404f9c9d0ad87a131a02b9f4e6adc6581d11115927cc`  
		Last Modified: Wed, 05 Jul 2023 03:46:31 GMT  
		Size: 58.8 MB (58820583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
