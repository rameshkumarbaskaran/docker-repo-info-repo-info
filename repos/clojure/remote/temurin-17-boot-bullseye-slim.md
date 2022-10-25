## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:7fc7e83f1128b93da95c288d3f083a8636a654c61d6da89e72f74878af43a8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:12e16c1aa77bc4a3df1daec11305139cc32a03f498092a970d8cd70e71f2447f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283457324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c73edc58684b47fc09f9edbb89b27cd6cd0e92bd87cc0705830245cf658a9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 02:40:02 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Tue, 25 Oct 2022 02:40:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:40:03 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Oct 2022 02:40:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Oct 2022 02:40:04 GMT
WORKDIR /tmp
# Tue, 25 Oct 2022 02:40:09 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Oct 2022 02:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Oct 2022 02:40:09 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Oct 2022 02:40:28 GMT
RUN boot
# Tue, 25 Oct 2022 02:40:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Oct 2022 02:40:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Oct 2022 02:40:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83abe3e31fb9e53a1a1e4ee0c8ea2375695563d8ad661be27c808d990fc0da74`  
		Last Modified: Tue, 25 Oct 2022 02:52:28 GMT  
		Size: 192.1 MB (192137443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce2c4f70ac16efd5b7dc63dfb05a068f3b2b0d94d0a50ba110408e6b10fabaa`  
		Last Modified: Tue, 25 Oct 2022 02:52:14 GMT  
		Size: 1.1 MB (1078978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe433518c091e402e17ccde349c77996ba0ba685863b7b57956054d66ffd3b`  
		Last Modified: Tue, 25 Oct 2022 02:52:17 GMT  
		Size: 58.8 MB (58820464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb29444913c08d12170e7e2145a4f8d62a4f9b95d791c516222e426d551d6b`  
		Last Modified: Tue, 25 Oct 2022 02:52:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6257eddeee72929bf6464a29a0efdac5fa783b12e280b1bdbc3fb00aa55da57f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280644330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36706d3eeed93a063669034a56dcb0f39ad32288c80b9fe959f071adc2a52c33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:39:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:39:48 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:39:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:39:50 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:39:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:39:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:39:58 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:40:13 GMT
RUN boot
# Thu, 06 Oct 2022 02:40:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:40:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:40:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3dc1ff9fe9090bfcd1bf503b2798ef1e1ea3dc429e1a3b8095249e5a30705`  
		Last Modified: Thu, 06 Oct 2022 03:01:21 GMT  
		Size: 859.3 KB (859259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e9f090ba7587285084eb58bc5e2db02fd4c9c536d98eed40a1cfd964cabc3e`  
		Last Modified: Thu, 06 Oct 2022 03:01:25 GMT  
		Size: 58.8 MB (58816036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220f891db70aa9b7089d64feea5ed49279de1c6acf5d799d985421c96b229d5b`  
		Last Modified: Thu, 06 Oct 2022 03:01:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
