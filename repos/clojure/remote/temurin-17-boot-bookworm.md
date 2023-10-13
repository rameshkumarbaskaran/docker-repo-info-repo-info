## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:f5b940512ed72c8c6f4da59658e096da2ed291fbda768e4062f1c658d640f7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c4f5250830f74b89462ac74e1d805d986372a02b0fd09d8f53fb07a061ed3eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258711297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7252051ac456b9a3f10098f251c9a90b8fd04a5e671223dd2ee74320bc0c93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:34:01 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:34:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:34:02 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:34:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:34:02 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:34:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:34:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:34:08 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:34:26 GMT
RUN boot
# Fri, 13 Oct 2023 01:34:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:34:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:34:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297dc0c7fb70cdbd48c6c16e128659b9836a465fe2755e7b24f636c965ca5b1`  
		Last Modified: Fri, 13 Oct 2023 01:48:16 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d72726ed0dd2f667acc72901d01be1660048ac4f7863409ed04a64e5d121ebb`  
		Last Modified: Fri, 13 Oct 2023 01:48:05 GMT  
		Size: 5.5 MB (5532602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bdd9516c5c3e0a12380c9e7325cf0857d175091e63d695ce57d1e7d00ba906`  
		Last Modified: Fri, 13 Oct 2023 01:48:08 GMT  
		Size: 58.8 MB (58820333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220651609596690b1c30d057286e93b26473f40b19005927915aca9cee86a5cb`  
		Last Modified: Fri, 13 Oct 2023 01:48:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8479dd2033e6b549c4d63fecb5154ad6c0ea45daefb76a2e928669263a3b7d31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257332601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bee54f6efb47f2addcb76654b0ac2c5da61574c04e278df504e98829fbee99a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:04:48 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:04:52 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:04:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:04:52 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:04:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:04:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:04:58 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:05:16 GMT
RUN boot
# Fri, 13 Oct 2023 01:05:16 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:05:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:05:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c0a26165e5e4720ee0810ab66a47633c5cc6f56db237748131b4b79eaf45df`  
		Last Modified: Fri, 13 Oct 2023 01:16:57 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7644643d58f37e247b39b5a41ce04bb6c3f17e67227740d94a46f3ac84d70c7`  
		Last Modified: Fri, 13 Oct 2023 01:16:48 GMT  
		Size: 5.4 MB (5355561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046eb2eb9d80d66a9976be15e0270bad2f661ffda456673b3554a0e1bb031ead`  
		Last Modified: Fri, 13 Oct 2023 01:16:51 GMT  
		Size: 58.8 MB (58820542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e4ab75084d62b420aec6b104a5bc37144b27bac253d8367b775cbf0f9b0130`  
		Last Modified: Fri, 13 Oct 2023 01:16:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
