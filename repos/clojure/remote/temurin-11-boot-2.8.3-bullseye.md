## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:558c05bb492655e42d61f752e4fdc2715170d39623aef2fb8610d16c855a0133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:19df16062c070d394dc7d799f488b97b3f3b3d0ff3b2ae40b1c329a605e5117c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314786934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bf8b2ebceca2e60208c50d815e92849d1a24d4ded55f9e9bd1e52621ff5e47`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:54 GMT
ADD file:e530b0563ea53d97b2f28e62149a665900196f86611df99a88c7a8ab2097b95d in / 
# Mon, 12 Jun 2023 23:20:54 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 06:27:03 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Fri, 16 Jun 2023 06:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 06:27:05 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 06:27:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 06:27:05 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 06:27:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 06:27:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 06:27:13 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 06:27:33 GMT
RUN boot
# Fri, 16 Jun 2023 06:27:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:93c2d578e4211e82e47e7ada9ed05d1869a2362c6f7509f2ee8d91ccebfb7fbd`  
		Last Modified: Mon, 12 Jun 2023 23:26:08 GMT  
		Size: 55.1 MB (55055162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8c24b5943dc6c4a62b9884ce3454e4dfe1bb499e59a5964d1812eaa527c2d`  
		Last Modified: Fri, 16 Jun 2023 06:40:29 GMT  
		Size: 198.5 MB (198549402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da026d37b17cdc5cd224b53be153d41ca3b422c731f7bd30cedc3915ca92c71`  
		Last Modified: Fri, 16 Jun 2023 06:40:16 GMT  
		Size: 2.4 MB (2361954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df5366e423f1f654be45775657990c9f6042653480c9654881c1d786ac7493`  
		Last Modified: Fri, 16 Jun 2023 06:40:19 GMT  
		Size: 58.8 MB (58820416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d04067274042e13cc6c1486418d4dbf6492195e58289eab714146db12bf08744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310200225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92afdfe414f409f8b5172cbf2ed330ccd2f75829c027f25356b35b4eb0eede`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:41:42 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:41:46 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 04:41:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 04:41:47 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:41:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 04:41:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 04:41:56 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 04:42:14 GMT
RUN boot
# Fri, 16 Jun 2023 04:42:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b429dc913a313200e2709dc18ae8c848cf538439e00d089ddee5b4541385cd44`  
		Last Modified: Fri, 16 Jun 2023 04:54:03 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf71a08da7f244340b9830b1ca93d79f63ac4fa070dc7c70c3abeefa93dcf31`  
		Last Modified: Fri, 16 Jun 2023 04:53:52 GMT  
		Size: 2.4 MB (2351346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84315f8cf675e5ebc8e532fa123e6a35f24c1eb9a5c3d9a0b512bb8294e4ade9`  
		Last Modified: Fri, 16 Jun 2023 04:53:55 GMT  
		Size: 58.8 MB (58820555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
