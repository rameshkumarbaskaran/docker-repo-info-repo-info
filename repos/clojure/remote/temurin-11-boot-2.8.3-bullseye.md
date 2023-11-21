## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:4214579ae1f331756a39c5780f7f9b30f34ec6b0ca89fcbe1d6408f133e27b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

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

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:09ff869ec2332a35f2058ba224819ed8300dfdabefb8c97a583284e5bb96b6d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d11dc8a136aff235a1de48ef2f2abc073e9306dd27e678b7b9e67faabc531f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:16 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:27:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:27:19 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:27:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:27:20 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:27:24 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:27:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:27:24 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:27:41 GMT
RUN boot
# Tue, 21 Nov 2023 07:27:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55c92be40caea1a03c3b8373d2ab9d08188bb25df2b9a9abc8e846cc50c348f`  
		Last Modified: Tue, 21 Nov 2023 07:43:36 GMT  
		Size: 142.0 MB (142001943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c5c048592f5c7d52ca492941f2f1e690bcd7d9e2c9d91026820d3cc6a14cb`  
		Last Modified: Tue, 21 Nov 2023 07:43:28 GMT  
		Size: 2.4 MB (2357435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1645c15e5a149a30561763dde1d9a2672336ead58170b87133317f3e6d63970`  
		Last Modified: Tue, 21 Nov 2023 07:43:30 GMT  
		Size: 58.8 MB (58820422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
