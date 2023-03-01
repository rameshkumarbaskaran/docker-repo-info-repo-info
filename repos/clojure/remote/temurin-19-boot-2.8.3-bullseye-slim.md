## `clojure:temurin-19-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:b9173546b29dcc049284d1becc5e1ae786c98a24190aa0c2b9f6881113cd70b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c735e3419d0388e8040308a1a9adfde2ae0c37f2a3462463fea21d9cacd6659d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292423015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbbfde44a246ac5da9d47aeeac4e00093597e4e01b258af1d1350859c4bea49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:31:41 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:31:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:31:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:31:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:31:43 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:31:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:31:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:31:49 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:32:06 GMT
RUN boot
# Thu, 09 Feb 2023 09:32:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 09 Feb 2023 09:32:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Feb 2023 09:32:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4864f8db9c8a9f2cc75ddf386c4ed7fdb7fd8a6d6a8e917a1fefd0d654a89ada`  
		Last Modified: Thu, 09 Feb 2023 09:42:47 GMT  
		Size: 201.1 MB (201112993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9ed75144e162603904a4db6fa6e661f6ee84616bc66ab86bd06c51072eaced`  
		Last Modified: Thu, 09 Feb 2023 09:42:32 GMT  
		Size: 1.1 MB (1077357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69457bdc975b28256668cfb062646c8c3168fd290684b5a239ebc0639239a3a`  
		Last Modified: Thu, 09 Feb 2023 09:42:35 GMT  
		Size: 58.8 MB (58820454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae893ac2a26a444a1d41f85d96277add09779b62df0a361b6b438210f8d75ee6`  
		Last Modified: Thu, 09 Feb 2023 09:42:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f29d605f91295e9c727b90f0ccc1472f26a59c349bdacfca89c8339f4d77e1c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289803473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d2c8067eb2c7fa9b74196ee2a016681052ded75d6d4934753d0b28e49e03f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:45 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:09:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:09:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:09:49 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:09:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:09:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:09:54 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:10:10 GMT
RUN boot
# Wed, 01 Mar 2023 03:10:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:10:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:10:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee23dab4c9395b25d6fc9f10fb3db021a5fb12f2747057b25dfcd66add5df0fd`  
		Last Modified: Wed, 01 Mar 2023 03:19:32 GMT  
		Size: 199.9 MB (199855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240c0137fdc38d9314ba6eb91b44574ea66a1e62051a9987a1e92375b9c17087`  
		Last Modified: Wed, 01 Mar 2023 03:19:20 GMT  
		Size: 1.1 MB (1064586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333431c7d4ac1a8d242676e73239ec35e620573bace9efd1c14419ce8a2a6212`  
		Last Modified: Wed, 01 Mar 2023 03:19:23 GMT  
		Size: 58.8 MB (58820472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f5f0a50dc1315220e9ff587cf356799f20e1dd079c3978dcf02cd5e40e4d6`  
		Last Modified: Wed, 01 Mar 2023 03:19:19 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
