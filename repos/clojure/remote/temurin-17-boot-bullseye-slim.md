## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:a2ffbea08687a627e13a8253ca02fd57811ad1fe604371c2fe4f6bff8acd470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c11758c045c9845638e4562b36458a12a407fcf55626bcc6264fe3bc87a3ccce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283882459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a813a2419a1be8a8f7ed72d50fed76e552ea6b30bc47e9896196a40f226d89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 08:10:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:10:23 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:10:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:10:23 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:10:29 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:10:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:10:29 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:10:46 GMT
RUN boot
# Tue, 23 May 2023 08:10:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:10:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:10:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432f099456cdedc7ddcd307e305c6b0fac23b7a57290e296b721fc518e6154f2`  
		Last Modified: Tue, 23 May 2023 08:18:37 GMT  
		Size: 1.1 MB (1077537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8dd2eb442bbe5a033c4ad126b2f856ae534600895a064f3eed374d099e5c24`  
		Last Modified: Tue, 23 May 2023 08:18:40 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84221829bb0c20f84f0b2b0fb6d1b08f1a4c438f8992bd4186ac7182aeb27bd2`  
		Last Modified: Tue, 23 May 2023 08:18:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:170b6200ca2d8f7dd39e81636aacfedaecffd5f85a0db97bcc736d696ec7cd35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281326065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b06c9aaed3ffee9598232918416793b5d270b1dfb7ce29c19fcac99533e781e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 01:29:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:29:55 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 01:29:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 01:29:55 GMT
WORKDIR /tmp
# Tue, 23 May 2023 01:29:59 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 01:30:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 01:30:00 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 01:30:16 GMT
RUN boot
# Tue, 23 May 2023 01:30:17 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 01:30:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 01:30:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26a475f0bd1bc0d41f2e019efe3a7311e5d5b55010eb4121c1d274954899aba`  
		Last Modified: Tue, 23 May 2023 01:37:11 GMT  
		Size: 1.1 MB (1064807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8f990a11fd0c5edb68b93f59ea42ed1698d8b08cfd912682a03c54f6f4f30e`  
		Last Modified: Tue, 23 May 2023 01:37:13 GMT  
		Size: 58.8 MB (58820421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c2e108839e3c55feba645877dd055c2864615866ba32bb200efa518b4f25de`  
		Last Modified: Tue, 23 May 2023 01:37:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
