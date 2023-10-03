## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:2bee6eb9ac6329eb6b859955c64a69012c4250722e777e091454da07cdbdd355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:403c86ba737b9a179ead7eb7cba8dceee346162b237b2b20856d9250b298ffb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261015458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5896fbbd48662af390c5f0171feb7f4474c3f56e0b905ff123b5844e0fc80b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:43:41 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:43:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:43:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:43:42 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:43:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:43:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:43:48 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:44:06 GMT
RUN boot
# Tue, 03 Oct 2023 08:44:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:44:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:44:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a366a404f6bbe3f097947a53809bf4f2f44e369fe03fba1600160364fd8b8`  
		Last Modified: Tue, 03 Oct 2023 08:56:31 GMT  
		Size: 144.8 MB (144775733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e48a9b04cf340e269ab41fe11386f959c81d34029ed367349a33969f93d3a5`  
		Last Modified: Tue, 03 Oct 2023 08:56:19 GMT  
		Size: 2.4 MB (2361964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8dd5f86009885096ce0c8a3ed114631263b3bc70c92f61925c08ef735c40ad`  
		Last Modified: Tue, 03 Oct 2023 08:56:23 GMT  
		Size: 58.8 MB (58820647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c76e3c17884fced9d7e75be5f3ce0c5f375dc6e97a6796a251d7fbc795ff0a`  
		Last Modified: Tue, 03 Oct 2023 08:56:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb6d125193925d1e288ccd9d5e2471ab9850928d13125ad67ec49910d4b56a47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258420835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33227d90b755bb2ef61f6d5d39f6ddf018797ea5b261241819a18cf6db9768e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:20 GMT
ADD file:46dcdcde338d2c01fed5db3fac9041736d9305145d8fc2039dd5b3714d38ede8 in / 
# Wed, 20 Sep 2023 02:44:21 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:47:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:32:04 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:32:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:32:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:32:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:32:08 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:32:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:32:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:32:31 GMT
RUN boot
# Tue, 03 Oct 2023 08:32:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:32:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:32:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:31f5dc1f52c865588c43d8ec718f14d430e149b28f0b28232da825da7ae28f76`  
		Last Modified: Wed, 20 Sep 2023 02:47:53 GMT  
		Size: 53.7 MB (53704892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f2e89c1f4660d2a5b13696facffb72e0a5d41487f6b725e2eb710509b3c64`  
		Last Modified: Tue, 03 Oct 2023 08:40:54 GMT  
		Size: 143.5 MB (143543519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248d91be23bce9259e05071c10204471bf71f863534c0a541e4a028aa728289f`  
		Last Modified: Tue, 03 Oct 2023 08:40:45 GMT  
		Size: 2.4 MB (2351472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d275073a890fe8615a37f629489bd223287ab18141857079e31c286c03da68ac`  
		Last Modified: Tue, 03 Oct 2023 08:40:47 GMT  
		Size: 58.8 MB (58820554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd73de6d2fe765fad22df1425beb8a8a5c446d9d02baf7fe432cc9e7c989f00`  
		Last Modified: Tue, 03 Oct 2023 08:40:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
