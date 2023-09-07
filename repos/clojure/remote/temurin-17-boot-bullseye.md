## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:3b329b5e899ced5b8a710a74a86cf2569c8d0bfe07c78202feaafffbaf0d18bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f691bf3ed3d843ad44049a78b6e0307ee823aca25b867a91e174de120e5a1fb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261014947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce82e522f96232a91f0f5328e1aa320b58246e08e6c8023ca0aa363083a886e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:23:42 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:23:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 03:23:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:23:44 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:23:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 03:23:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:23:49 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 03:24:07 GMT
RUN boot
# Thu, 07 Sep 2023 03:24:08 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:24:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:24:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f659b2aacdd3e2363ebb3332a830f2dcd93164a10995d976ac13e700435f5`  
		Last Modified: Thu, 07 Sep 2023 03:33:07 GMT  
		Size: 144.8 MB (144775757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d4e0642c0a2744d6ac7f362ed9f7adb9a01154e767c4fd69fa997707b202a9`  
		Last Modified: Thu, 07 Sep 2023 03:32:56 GMT  
		Size: 2.4 MB (2362046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fa48699b8a4017d46e47df9d3091388a7deddff00fd8c69e95b7e2eedbbb8c`  
		Last Modified: Thu, 07 Sep 2023 03:32:59 GMT  
		Size: 58.8 MB (58820499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a193c404a92ec2c3482f7e6bf1a6521fe42e7f9ae96ff30e773206c750a0edef`  
		Last Modified: Thu, 07 Sep 2023 03:32:55 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:395d27762fff1dbac7296025de49316e47b00fef1ab7951aaa982f70deb631c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258420749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d043e872f4994ec1339f1e9f8578ee8b8a582c96069c49b3cc82d41102aad67d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:47:28 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:47:31 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:47:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:47:31 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:47:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:47:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:47:36 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:47:52 GMT
RUN boot
# Sat, 02 Sep 2023 01:47:53 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 01:47:53 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 01:47:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c782a1c2165dbdac384abd088ebc99d9f013b55fa39e22661861b6b10083b60`  
		Last Modified: Sat, 02 Sep 2023 01:55:28 GMT  
		Size: 143.5 MB (143543490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48927940444fbc331a2f2d983631e5a7e0711e10cf083e07a5a5586539b2609b`  
		Last Modified: Sat, 02 Sep 2023 01:55:19 GMT  
		Size: 2.4 MB (2351444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483f1cf05ff1e280ec4615803f92f6654889dc21b06f35ce9efdce0c2302098`  
		Last Modified: Sat, 02 Sep 2023 01:55:22 GMT  
		Size: 58.8 MB (58820637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e553780940c0c73ac4e2c1ea1e108193ffa056d918ae285f3c28288464f188`  
		Last Modified: Sat, 02 Sep 2023 01:55:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
