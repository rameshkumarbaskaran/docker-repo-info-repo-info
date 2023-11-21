## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:88ce1287a66fc76d402a19bac5a5931d773af077658c24f7a74961299c136314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7d52dcf877c985ae4a66f5a60a883f0533929284db5f32625f1bdb08e1d359dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dc4841af8afe250e5dfc12e4d66d87ae4024a8b4d2bc805ff7fdfdb1b47576`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:19:49 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:19:50 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 10:19:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 10:19:51 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 10:19:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 10:19:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 10:19:56 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 10:20:12 GMT
RUN boot
# Tue, 21 Nov 2023 10:20:12 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 10:20:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 10:20:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7214060c30b24ef6b44181a3b8ba481045c5a82c2a66ea626f75e21dae09b6`  
		Last Modified: Tue, 21 Nov 2023 10:35:57 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4eda5ff5f1eb46ca93463ac2895d6c813b1b16efadf1fb04afdccf8ea416d6`  
		Last Modified: Tue, 21 Nov 2023 10:35:45 GMT  
		Size: 2.4 MB (2368670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feae57efe2bd6b4f0350a1d46e318768a4cc15ac73f1b7355a6d793f2c2f41`  
		Last Modified: Tue, 21 Nov 2023 10:35:47 GMT  
		Size: 58.8 MB (58820347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae50084fd28cb8e62e07717d2b0e1569f1e58acda44fb8ca7b2dddd2e0bf81d`  
		Last Modified: Tue, 21 Nov 2023 10:35:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c576d07abbbb8c886ea04796aef7d230eda8a2b70e3910e2e8d87c087250890c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df20294d35487d7107b78f2dc03aa9da7031ce62232d25854a78f271d12e520`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:31:54 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:31:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:31:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:31:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:31:58 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:32:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:32:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:32:19 GMT
RUN boot
# Tue, 21 Nov 2023 07:32:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:32:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:32:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d222093186fe627ebded7dede3ff589e904bd1961e248360a27dfa7ccf9ca30`  
		Last Modified: Tue, 21 Nov 2023 07:46:59 GMT  
		Size: 143.7 MB (143681718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa650dc54244f2e84da77a873cbbb3d8ee08d76ab6f6eefadc7e7821f3446a6a`  
		Last Modified: Tue, 21 Nov 2023 07:46:50 GMT  
		Size: 2.4 MB (2357488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a705bfb2d5221fadf9fa4d55a6f231924ee204dbd3769a043dc24fadba41c0`  
		Last Modified: Tue, 21 Nov 2023 07:46:53 GMT  
		Size: 58.8 MB (58820450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e49125a9198f3d3bc3d58796b6a7d347c272cae080f63d039ec4dd37ddd0be`  
		Last Modified: Tue, 21 Nov 2023 07:46:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
