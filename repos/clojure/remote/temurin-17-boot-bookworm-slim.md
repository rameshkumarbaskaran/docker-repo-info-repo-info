## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:5cab9d837c05e9d4b25cbd61db546630d08eba01bc6ea5c2ffdca220cd02ab80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:244f63c824eb8916b27a6265ea847ff6db43a57b271e61a1ea55360d4a60bafe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236346190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bda680e08e47694c70fa6e43a48b7bb2a30f31c7bad892ca1098d8b6a0e96a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:23:04 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:23:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:23:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:23:06 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:23:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:23:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:23:12 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:23:30 GMT
RUN boot
# Wed, 01 Nov 2023 01:23:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:23:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:23:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f66d533080f21b1abb7d6c1122fda3614b0c857f92230dfc024d06a8a930ab`  
		Last Modified: Wed, 01 Nov 2023 01:40:08 GMT  
		Size: 144.9 MB (144873950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bca7151c3e23c890b23a07ee852803cd3a0f2afebb178cb3d8311fb8225ba4`  
		Last Modified: Wed, 01 Nov 2023 01:39:58 GMT  
		Size: 3.5 MB (3501668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a148b4f2571acaf9b5be91c127f2b3b96d642f6c6433bd019b0a400c9f83d`  
		Last Modified: Wed, 01 Nov 2023 01:40:01 GMT  
		Size: 58.8 MB (58820335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123a5fa0af7d3d45f06c770b140ae3b99f80a189c840bf744fd1ffdd5f7c954b`  
		Last Modified: Wed, 01 Nov 2023 01:39:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6723eb2485aec04dd4fd88eafab110f16b2d6e921d5c50cd141f99b1148e35b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235006573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b593158ce97c5e193261eb16eacfed43fc83b9d26ad8a7372f23215395cfde5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:31:26 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:31:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:31:30 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:31:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:31:30 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:31:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:31:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:31:35 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:31:51 GMT
RUN boot
# Tue, 21 Nov 2023 07:31:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:31:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:31:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57321419cbc0b91c4f574eb475696a6a8ea5a9c5e49839ad0830ecb15d557aa`  
		Last Modified: Tue, 21 Nov 2023 07:46:41 GMT  
		Size: 143.7 MB (143681713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3688dc2d03ec03e8d38b1ba9a2517d32b7aec88ab1266a1073d4ba33012aa7ca`  
		Last Modified: Tue, 21 Nov 2023 07:46:33 GMT  
		Size: 3.3 MB (3324894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15523b9f2b5a0161b9eef1bd249f6520c17dd519dd70c8a92d486053a13cc842`  
		Last Modified: Tue, 21 Nov 2023 07:46:35 GMT  
		Size: 58.8 MB (58820290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3705bbe4432e1521f7269fca70ee316c005cc88db0c238f0829bdeef35cb5e5`  
		Last Modified: Tue, 21 Nov 2023 07:46:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
