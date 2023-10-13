## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:c39f51e19b0733b12ca29c15bfc892b41d81303936647a84820bfc19abc397e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:abb187867d423257b5c8d647b588f083c6e35ff836c4dfc8359cd7da11250819
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258711345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab7316c38700fef4beb736a652bd336661ec4666a8bb53e15b465cd5452e58a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:52:06 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:52:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:52:07 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 12:52:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 12:52:07 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:52:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 12:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 12:52:14 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 12:52:30 GMT
RUN boot
# Fri, 13 Oct 2023 12:52:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:52:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:52:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f6291b22d70cff059b865d89b1554735b685fb268c97387261bac2bd8f0ee2`  
		Last Modified: Fri, 13 Oct 2023 13:09:53 GMT  
		Size: 144.8 MB (144775717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1e6286b2475d1fecd59f23f7c9cd15afdcef3df038e6a679efffad23027303`  
		Last Modified: Fri, 13 Oct 2023 13:09:42 GMT  
		Size: 5.5 MB (5532693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d195d4d8fd7c566e9634dc5efde31a6eea371aae8ce2d932a8c800050cdd71`  
		Last Modified: Fri, 13 Oct 2023 13:09:45 GMT  
		Size: 58.8 MB (58820310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b314b2565aa82dc928b82758f56be4423b99f913b98cfa2f875103db9e8f95`  
		Last Modified: Fri, 13 Oct 2023 13:09:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6b70c111964d0686e9291af062842f1d76a739443de114be6a63393ecbd88783
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257332580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f7bc8850cb1bc3766ceb5fb7ff1c8e6063797a5dc8eaa54b8b88f58e3b79d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:18:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:18:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:18:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:18:44 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:18:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:18:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:18:49 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:19:07 GMT
RUN boot
# Fri, 13 Oct 2023 10:19:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:19:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:19:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d651a3fb90463baef37e8108569d81355c0974d68da3cce0e70482f66c93d`  
		Last Modified: Fri, 13 Oct 2023 10:34:04 GMT  
		Size: 143.5 MB (143543493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54561214b0a54647aa2a297566bba99b4156f5629829970d4c94bee9f95b05a7`  
		Last Modified: Fri, 13 Oct 2023 10:33:55 GMT  
		Size: 5.4 MB (5355512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f88c8fe7289ab64d648a3bc6c90653d564519d97d6b4e8d698c10adcbb80dd`  
		Last Modified: Fri, 13 Oct 2023 10:33:58 GMT  
		Size: 58.8 MB (58820598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49242bd272a1a231d4cabd25d73b301578704f65982eb43ffeb165b17aecff7`  
		Last Modified: Fri, 13 Oct 2023 10:33:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
