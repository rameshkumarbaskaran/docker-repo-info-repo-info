## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:3472841301b51de8fea249d1f993056c1b081a5cbf28f7dfb88b53f501cddd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:317c38379b5e121e29c5d712bfeed6d2cbcd876255740d236a2748192418de9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283457555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a7e4f39f89103d984ab6fb99de3ce46ce44a7c8f209d444d782337492f187a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:15:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:15:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:15:25 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:15:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:15:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:15:31 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:15:49 GMT
RUN boot
# Wed, 02 Nov 2022 20:15:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:15:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:15:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e435137c33bf2d5264f4419a0df33d23026c107f41d6a5453722e7e08b0e0c`  
		Last Modified: Wed, 02 Nov 2022 20:27:33 GMT  
		Size: 1.1 MB (1078984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c722a0d0c20c70bc8461024e006dddc9541300373425fd7fba8b1b0d52940df9`  
		Last Modified: Wed, 02 Nov 2022 20:27:36 GMT  
		Size: 58.8 MB (58820575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc200052c554a413213af10d906ea15781c03cb05656bc66bb282f6e449579bd`  
		Last Modified: Wed, 02 Nov 2022 20:27:32 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5a2c94b1c3e4964c0f18a18aa26404bf7e6587bb682adc08130c8511e5cece6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280855376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92795601a24712f6beb2d7d5a8e5ac7ae73cd3c1cc4435fdc1651d31ed3b7471`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:50:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:50:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:50:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:50:45 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:50:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:50:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:50:50 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:51:06 GMT
RUN boot
# Wed, 02 Nov 2022 20:51:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:51:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:51:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29301a7fe3ff8fb2f0a794ad28b2a49d50527030bb36015f6a18e3d1510097f`  
		Last Modified: Wed, 02 Nov 2022 21:01:24 GMT  
		Size: 1.1 MB (1066350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaf5ffb60573935bb54c4d2141866bfc53f43dc7d8ffabbf7e8a3bc2b793944`  
		Last Modified: Wed, 02 Nov 2022 21:01:26 GMT  
		Size: 58.8 MB (58820623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cb4bd8bbe4ac32f17b4f6c8b0caa5673ec82a3f747437f240cb774dcc5e5e3`  
		Last Modified: Wed, 02 Nov 2022 21:01:23 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
