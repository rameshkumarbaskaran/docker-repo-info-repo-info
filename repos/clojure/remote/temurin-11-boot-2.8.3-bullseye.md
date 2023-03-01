## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:cb004705f010b14f64630e1ffd7a05879b098c26a99894109b5caa7cc96139e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e45572ec5b7acc604a3d0273b837bdacd4eded29f453cf93103c2cb1dfac094f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314704365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1c9833dfe683a33aa0c243455c11170c700da3a03bdae7a457fab0e65e814f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:05 GMT
ADD file:b03d13d345c29f69557f410c8504e748226756d1f48e5abdb63cd40179b2640c in / 
# Thu, 09 Feb 2023 03:20:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:25:04 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:25:06 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:25:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:25:06 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:25:12 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:25:12 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:25:29 GMT
RUN boot
# Thu, 09 Feb 2023 09:25:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1e4aec178e0864db93a6f97a20bde3445871a4562c1801185eca1238d3a0e80d`  
		Last Modified: Thu, 09 Feb 2023 03:24:47 GMT  
		Size: 55.0 MB (55046771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fa5505d5f9a403b5fa799c74b7639e1188ddc30c0db155b99238ff035c03ed`  
		Last Modified: Thu, 09 Feb 2023 09:38:26 GMT  
		Size: 198.5 MB (198475422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356d56fdf570046c64cfef98607a85390634d5bd87538e8008b3cfb278e8b374`  
		Last Modified: Thu, 09 Feb 2023 09:38:11 GMT  
		Size: 2.4 MB (2361639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90bf9a9ba2bf48a6fd6879d38261dd902a3265fc44e5ed5064724ce5bbec65a`  
		Last Modified: Thu, 09 Feb 2023 09:38:14 GMT  
		Size: 58.8 MB (58820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:130aaf071f79b651096a84bf25f9fc177ca7b08e3f9e9ae0f0969553e0fd1976
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310115048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65df673505500c92ee3463f50a242d08d3b99bfa2e21c8ce0c239b3a57dadf57`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:04:01 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:04:06 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:04:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:04:06 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:04:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:04:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:04:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:04:28 GMT
RUN boot
# Wed, 01 Mar 2023 03:04:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db5f99a046fb93d70e363d58ebe237b913e09a889f35b330f65e0bfa4627f3c`  
		Last Modified: Wed, 01 Mar 2023 03:15:41 GMT  
		Size: 195.2 MB (195240319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e8ed13cb2c61cc3df0df1f561ffb2ea74ef7bcad3057e758d7a954993350b`  
		Last Modified: Wed, 01 Mar 2023 03:15:30 GMT  
		Size: 2.4 MB (2351022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be609b0d2928b4f0b0f06c0305df464086a410a6084ef30c091859939f298456`  
		Last Modified: Wed, 01 Mar 2023 03:15:32 GMT  
		Size: 58.8 MB (58820492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
