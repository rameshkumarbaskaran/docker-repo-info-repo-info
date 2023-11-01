## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:8fb59b27af3dd72d1c50598109a418fde9fcf50b9026cadb8441147d881d25f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2fe5c215bdee3813c30b36379b2892196979050b6c1f08f6d4e532564dc69946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf33c83b8efdbb707e3a28882b7922b12057d20f62cf635611ff0111d234878`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:18:21 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:18:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:18:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:18:22 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:18:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:18:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:18:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:18:45 GMT
RUN boot
# Wed, 01 Nov 2023 01:18:45 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d820ac6719f8f726f9f5960926f44b9b78299a2dbf0eb09b456a04c7c8a15a24`  
		Last Modified: Wed, 01 Nov 2023 01:36:59 GMT  
		Size: 145.3 MB (145266659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05353cc5f6c2050a0751a5b862e9a1d9d3fbc33cc6174aba872c7a4f43ee4985`  
		Last Modified: Wed, 01 Nov 2023 01:36:46 GMT  
		Size: 2.4 MB (2368718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3108c02f512dac8fc1a469d5f55b829110c0fb093b1b4dd30fc0b1da7ec2f4c`  
		Last Modified: Wed, 01 Nov 2023 01:36:48 GMT  
		Size: 58.8 MB (58820361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89cf19b860790d52616b176edde9d21c8238f5aee74e81dd7122632804135e38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c17f8c40be5eddef6fc43fd157222453f8d9a29b9900ce4b18a8bd63fa83174`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:57:56 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:57:59 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:57:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:57:59 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:58:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:58:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:58:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:58:22 GMT
RUN boot
# Tue, 31 Oct 2023 00:58:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a314cc05ddbde5072f40f29d8bb5b7ee277835c4cdd222b0e3cb1fc866cd351c`  
		Last Modified: Tue, 31 Oct 2023 01:17:58 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e509e41aca71233b843df12cd3dce57bfacc0633598762d9b8c26f2f76fc60`  
		Last Modified: Tue, 31 Oct 2023 01:17:49 GMT  
		Size: 2.4 MB (2357450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b83d19e864f8f82d3bef9d5f4a2f91b3eb89fcc42da63edf2f3b218ee25d1a0`  
		Last Modified: Tue, 31 Oct 2023 01:17:52 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
