## `clojure:temurin-19-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:2ca260fabe54f59acd300fdd76c7f51fb43ec301a89eb22bf08f06c7880a9954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c1fb3f23969286268d7c91975ee1d8e20cf06624282950c993d7437531f38b4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317332691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8427a0034f31b954f3faf7da97df03b0e356c69b0d8ab7da34af255ca5309293`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Nov 2022 19:50:54 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Tue, 08 Nov 2022 19:50:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Nov 2022 19:50:56 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Nov 2022 19:50:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Nov 2022 19:50:56 GMT
WORKDIR /tmp
# Tue, 08 Nov 2022 19:51:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 08 Nov 2022 19:51:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Nov 2022 19:51:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Nov 2022 19:51:22 GMT
RUN boot
# Tue, 08 Nov 2022 19:51:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Nov 2022 19:51:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Nov 2022 19:51:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7234d89610b4a16d903abead0c04715b2957b47183fec8ab6f88c4f3538cff68`  
		Last Modified: Tue, 08 Nov 2022 20:00:47 GMT  
		Size: 201.1 MB (201103429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cb5ee206fc26eb73b815485806e272b29b1b9c67c3dff04bfc21558c62db0f`  
		Last Modified: Tue, 08 Nov 2022 20:00:33 GMT  
		Size: 2.4 MB (2362129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e786c61c21663b908ebf3b24a542c516cddc83d8ad2d3659a915545424499a1d`  
		Last Modified: Tue, 08 Nov 2022 20:00:35 GMT  
		Size: 58.8 MB (58820402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a1e3b79f3e2356d8787e32aff9f85ecbd24748481302925ff9856423d72686`  
		Last Modified: Tue, 08 Nov 2022 20:00:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:443998f08b5a58c125045519de382ff545a348cde3d5ec541d34c89c79b091a2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314457535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea81bfca1ec24cc33024a6f489db1979ebcd217ad4d1774bad565fec489c5a10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:48:52 GMT
COPY dir:2fc3a52010e404362374a6fbc2449d1ef85a3bc7bb00efe969cabc1864797789 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:48:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:48:57 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 15:48:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 15:48:57 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:49:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 15:49:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 15:49:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 15:49:19 GMT
RUN boot
# Wed, 26 Oct 2022 15:49:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 15:49:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 15:49:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997f9b1128d353add7d065052afcf1047aea6a037bed4d3396015998ab5e3ca`  
		Last Modified: Wed, 26 Oct 2022 16:05:23 GMT  
		Size: 199.6 MB (199582421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b312baa922120bb4f1f7f46bd7e222092da70352ff1b52d25e1305107bce0586`  
		Last Modified: Wed, 26 Oct 2022 16:05:11 GMT  
		Size: 2.4 MB (2352312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be67257c8efc0db1683cd803abf35823d170e0c26bd88e5498c3baf8d6d9c194`  
		Last Modified: Wed, 26 Oct 2022 16:05:13 GMT  
		Size: 58.8 MB (58820435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc2ae603a1dd8ee727ac7d84f34368ddbe98dd3ecea8b9e2eb74c6bf4bc11ee`  
		Last Modified: Wed, 26 Oct 2022 16:05:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
