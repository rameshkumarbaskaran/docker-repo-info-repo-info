## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:a86c2ee5006401689742fdb00d0cbf3a8c6f29601fe5cb6e807e240b5707e579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b6c524aa4cd6dbaecb57a27df81831b9192ec72cf22506714297d8bb5bbd8a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236738478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb96cda05d5feabd9f66098590d1e9d118b1eddda2f66d4a70ace8936288490`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:17:46 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:17:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:17:47 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:17:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:17:48 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:17:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:17:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:17:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:18:11 GMT
RUN boot
# Wed, 01 Nov 2023 01:18:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d63825152d5cbdd4aca989095ba3c4b2885c009fca2083969b63ead3b1ec3ae`  
		Last Modified: Wed, 01 Nov 2023 01:36:36 GMT  
		Size: 145.3 MB (145266659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a3b1b689ca11106462d75934f6959996cd5821172560f4acd45900e4457239`  
		Last Modified: Wed, 01 Nov 2023 01:36:25 GMT  
		Size: 3.5 MB (3501673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45acfbe193bdb64b92358ed9abb1e74d89fb1e0c7bdaa37138015721a1c335be`  
		Last Modified: Wed, 01 Nov 2023 01:36:28 GMT  
		Size: 58.8 MB (58820310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47850e4ba2b580eee75dbbb600c5543e418c232bf795d13c7824a6073de02342
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233326583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38367c4bd711718b4288005e36bc5e8bb01336959c86f42f7e7d8878c9ebe9e3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:26:48 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:26:51 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:26:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:26:51 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:26:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:26:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:26:56 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:27:12 GMT
RUN boot
# Tue, 21 Nov 2023 07:27:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7380b182fb0ab44680e2ae8a99d8a7c4ea84bd6ac7e36e717f150191d6d29339`  
		Last Modified: Tue, 21 Nov 2023 07:43:19 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e295624045a2964b5e58518a1f1fbc0f1c2c5f05c87cdb24f1636d3baa9750`  
		Last Modified: Tue, 21 Nov 2023 07:43:11 GMT  
		Size: 3.3 MB (3324896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556617924c1477410f11a3d22bc11d77ed3745aaef5830646d39e60c3d5ea177`  
		Last Modified: Tue, 21 Nov 2023 07:43:13 GMT  
		Size: 58.8 MB (58820457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
