## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:19430fc1038913b14726f8f7edf3543c8086a684465a65d9ea6709803091c175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:127c6e7fa462a42a6461070571c422c13cd60d2d8fd381d6903f144700c52489
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6e770d8f6864121595fcc4c431d5b866e1577caa231e2b9983549b6cc48caa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:51:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:51:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:51:00 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 01:51:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:51:00 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:51:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 01:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:51:07 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 01:51:25 GMT
RUN boot
# Thu, 02 Nov 2023 01:51:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae3bc407ed44ee4c19e2acfaafba1a8237df1bc1f1bca7853c10d12070957d`  
		Last Modified: Thu, 02 Nov 2023 02:03:16 GMT  
		Size: 103.6 MB (103598251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0179f72fd84b50b99e6cb97f31a09b9531caadde016ceab0d33ebef3b876a28d`  
		Last Modified: Thu, 02 Nov 2023 02:03:08 GMT  
		Size: 2.4 MB (2368697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0711c4965ec79bd328e0ef4d22bdc61956ffea6375e1e45849c2e53e1e6d83e0`  
		Last Modified: Thu, 02 Nov 2023 02:03:11 GMT  
		Size: 58.8 MB (58820339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58f83e754b08769e9bb308ba4a8adafe1cd2e61e74bf35492c463a5d8aa05213
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217587031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a144d5a1ba6236ce3c78eeea9b345bca1c58676c832a89173c7d34847fb1d0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:29:15 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:29:18 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 03:29:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:29:18 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:29:24 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 03:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:29:24 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 03:29:41 GMT
RUN boot
# Thu, 02 Nov 2023 03:29:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a75e620a2c6e0a54df04b768280b9c28cb06717d56b0afd14125c17caeab1f`  
		Last Modified: Thu, 02 Nov 2023 03:38:39 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da215b8cf1a2ddd3d7d187903a6872512445c1cfdee95ba417006f520b3486b6`  
		Last Modified: Thu, 02 Nov 2023 03:38:32 GMT  
		Size: 2.4 MB (2357351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e66fc6bb3c25dfa60008861efde71e9ee72e61d829bec5305ac580c02a6917b`  
		Last Modified: Thu, 02 Nov 2023 03:38:34 GMT  
		Size: 58.8 MB (58820392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
