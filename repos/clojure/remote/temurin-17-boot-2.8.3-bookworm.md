## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:cba041bad0d741132fea25ad7d9967bf9766aefed59bdca59a455499a5a5b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:62a97297528cc69e198a08ecd22cb8c656c53399df2046a818f6e61f2f5024f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258807232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed7a1470bdc86503b767f321bb8f416acd1a1649939474159e4b140053f38e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:18:47 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:18:48 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 10:18:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 10:18:48 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 10:18:54 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 10:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 10:18:54 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 10:19:11 GMT
RUN boot
# Tue, 21 Nov 2023 10:19:12 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 10:19:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 10:19:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a59c8aee6beabb9a28978d412b9cda10c78ebfad3f1537ffb2d4299e1e9b0`  
		Last Modified: Tue, 21 Nov 2023 10:35:15 GMT  
		Size: 144.9 MB (144873904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98ba6a4a2e52463c699ee5e38db12141a44f1770408e20c956915901bf4d037`  
		Last Modified: Tue, 21 Nov 2023 10:35:05 GMT  
		Size: 5.5 MB (5530348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf26582829883de429ca0ab047f02484540d33c34ed06f0adb4312555e64085`  
		Last Modified: Tue, 21 Nov 2023 10:35:07 GMT  
		Size: 58.8 MB (58820356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c228d95ad7e7d8068d234fdae54c083e0d376c467a330672405e5473583df40c`  
		Last Modified: Tue, 21 Nov 2023 10:35:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:795932e7371c59357eee1ca354bd6d3b5cd231838b90c2d2631a51b7a1f0dfbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257468595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5191b5ec28ea91f05c6d37e75cea4d41365d9183d7b126620003102989328c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:30:54 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:30:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:30:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:30:58 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:31:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:31:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:31:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:31:20 GMT
RUN boot
# Tue, 21 Nov 2023 07:31:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:31:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:31:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb7eea93e806cda12688c1cef1abab3769a83178187c1b5813f675ffa83e80f`  
		Last Modified: Tue, 21 Nov 2023 07:46:23 GMT  
		Size: 143.7 MB (143681765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b52823e9078733a1d076bdcd536e0130aae8752ae432c8fad250890e3a8be4`  
		Last Modified: Tue, 21 Nov 2023 07:46:15 GMT  
		Size: 5.4 MB (5353254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e07380d64e9ed9342c1a721b5a246a89ee35edd40b56a97f52a8331ef321af5`  
		Last Modified: Tue, 21 Nov 2023 07:46:17 GMT  
		Size: 58.8 MB (58820526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df355d1454b14e819e1b929adb734630f8567d461cbebdb88b83f47a6a81e8`  
		Last Modified: Tue, 21 Nov 2023 07:46:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
