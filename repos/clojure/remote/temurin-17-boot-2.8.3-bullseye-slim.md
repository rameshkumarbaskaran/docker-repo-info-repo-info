## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:95ac3c9d108ad6ef2b3e9b6df70d470b879956da2d3c029bf263efa12ac0c60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d77876351a3debe1f7ece59a68025de522985b13359f3a244c634ad41346c8a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283896353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953a5d1a03d029cc98aba42118d7dfe24d06e13d3c465e6266ed34c836cadc68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:24:32 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:24:34 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 11:24:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:24:34 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:24:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 11:24:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:24:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 11:24:56 GMT
RUN boot
# Wed, 05 Jul 2023 11:24:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:24:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:24:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafbbd507c7f35e198981926b1a326f224d7e89d5a693df01bea8a92ba4e7d1b`  
		Last Modified: Wed, 05 Jul 2023 11:36:02 GMT  
		Size: 192.6 MB (192580435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576cfae513c3806cf2c252e0ad27ac0c2f0020829145a355b2bca624c41c8fac`  
		Last Modified: Wed, 05 Jul 2023 11:35:49 GMT  
		Size: 1.1 MB (1077536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5454bd671bdf9f23a8eef1ff97444082a775dff7b010d8da75f98aa030e18100`  
		Last Modified: Wed, 05 Jul 2023 11:35:52 GMT  
		Size: 58.8 MB (58820595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a37c483dd932dce0d4f07339301bb8d8ea0ead46a213cd3cde32b2f1e3b6f70`  
		Last Modified: Wed, 05 Jul 2023 11:35:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:abac2737a209632b8e0815494c0b02d9bb36541b9f2d23e3f55e1146b88add84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5f8d7ecef098db040053519a2529702d11612efb3cd6f1f67027a95cd5b9a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:39:58 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:40:02 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 03:40:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 03:40:03 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:40:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 03:40:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 03:40:07 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 03:40:23 GMT
RUN boot
# Wed, 05 Jul 2023 03:40:23 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 03:40:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 03:40:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a44711a84ae8605b1c1f0f04cf29732536ca2ecfae7b5a7b10134f3584ec4`  
		Last Modified: Wed, 05 Jul 2023 03:49:53 GMT  
		Size: 191.4 MB (191387679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42984f51ded3ed2ad0bf33242e6b1a3efa08b7e2d7de2deca545680c2933188b`  
		Last Modified: Wed, 05 Jul 2023 03:49:42 GMT  
		Size: 1.1 MB (1064805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ff62a9d3a23fb5e3ccd7cd7cbc5c920be75729d3e053d9461cf549c84121f8`  
		Last Modified: Wed, 05 Jul 2023 03:49:45 GMT  
		Size: 58.8 MB (58820398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd08015725cf05730f58de96ceb1a742975a498c81e3c24271051207dd6f58a6`  
		Last Modified: Wed, 05 Jul 2023 03:49:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
