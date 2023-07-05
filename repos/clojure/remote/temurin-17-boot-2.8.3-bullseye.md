## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:6d1fe7a83ee58ae02ae6429554c6301d8ca8bb8b96bb0c7bcf47fc6d8b519968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7d83fbbdd3eb52d58a26edbd5e5bc4b9f52ef5904193d6dd04bbfbc4a14dfa02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308818555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f509d593bfffadbec94a2ee801b67871761b3a08d34cbdee31e0b40953dbd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:05:49 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:05:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:05:51 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:05:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:05:51 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:05:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:05:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:05:57 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:06:14 GMT
RUN boot
# Tue, 04 Jul 2023 04:06:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 04:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 04:06:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d5749ce62c0fb43ce9ee4298e4f571f0584facdde1f4b6b77b68dcf21129c2`  
		Last Modified: Tue, 04 Jul 2023 04:15:06 GMT  
		Size: 192.6 MB (192580329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867a42286c8fd64788bcca9ecdbc386ad3706ec5ab9af2f0b17a4c49597bce42`  
		Last Modified: Tue, 04 Jul 2023 04:14:54 GMT  
		Size: 2.4 MB (2361998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f131ac5030f2260ecf46ebac6600983427ef72bf57ed714fb3e3e3f068a602`  
		Last Modified: Tue, 04 Jul 2023 04:14:56 GMT  
		Size: 58.8 MB (58820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86200f2de86cafe4a518ec081a6f7b8d8286bbba1570314c826c5a43e6d629f3`  
		Last Modified: Tue, 04 Jul 2023 04:14:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73814ed5b7e85a5e84cea778a44642555cb6d8c0381ddfca80b12c241a2c9940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306263989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f5aa3a12dee7999eda9db378e065ea1fe31c8c7895ae9b725be20601012d04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:39:26 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:39:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:39:31 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 03:39:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 03:39:31 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:39:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 03:39:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 03:39:36 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 03:39:52 GMT
RUN boot
# Wed, 05 Jul 2023 03:39:52 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 03:39:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 03:39:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86dfcaa48ab17da652aa675b61970ff9dcd21d8083194b6bcaf57290c706ca0`  
		Last Modified: Wed, 05 Jul 2023 03:49:34 GMT  
		Size: 191.4 MB (191387642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ca7f3df05ac12a7f2e7ef5cbd0fb9c8e71b0f4d313a25edb18421fe35744d0`  
		Last Modified: Wed, 05 Jul 2023 03:49:23 GMT  
		Size: 2.4 MB (2351410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa23b9d186dee32ae02f4b381e4aea2d9eefd68c6e2c9473fdfef79447640b`  
		Last Modified: Wed, 05 Jul 2023 03:49:26 GMT  
		Size: 58.8 MB (58820558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953a897f77a8f2b7b82e4f24992e5a226e44435036ce6f2ac064091924ca981a`  
		Last Modified: Wed, 05 Jul 2023 03:49:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
