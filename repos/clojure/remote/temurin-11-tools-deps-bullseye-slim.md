## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:7612d2090d8f15a376a5c75946657c061ff5bad24656b9de048f2424be5eff6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0ab61a34070675897008a1e7aac0dda8b643bd6d6ecccdd19e4a16cdc6b357ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238188688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ada993b017696e497d1225190c2f0e248298e7d2e6a9e98923989ffc6ca0b3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:18:55 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:18:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:22:03 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:22:03 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:22:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:22:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:22:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0c2457a667e342734343cd296f94de2032329a37ee32ca0f48794427a59f05`  
		Last Modified: Wed, 01 Nov 2023 01:37:19 GMT  
		Size: 145.3 MB (145266641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392b0d3599abd7cc75adc7b62901c5353052889a1ebb4253def282b6ab320324`  
		Last Modified: Wed, 01 Nov 2023 01:39:23 GMT  
		Size: 61.5 MB (61503516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6481a0d9657a29ecbc5e89247b04c57f9bd00ba03b9851a8b4e0d2e6df81b8c3`  
		Last Modified: Wed, 01 Nov 2023 01:39:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8426d612f070a4eff5c340f83c7ae7ba73738d84f4b97f66699dfca98524bdc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233686906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e5582d1100793c90be4b2ac3824dce523cafc40bee5d5d5c1d77ee7768c9e1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:58:29 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:58:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:03:06 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 31 Oct 2023 01:03:06 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:03:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 31 Oct 2023 01:03:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 31 Oct 2023 01:03:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1574a555514b1c133c3be600625ef18feb9a4fe8cac6b809f10df06a43b9ed`  
		Last Modified: Tue, 31 Oct 2023 01:18:17 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f7bdb8c41977a4b34628503d1bef3a1f55d358101b42ce5cd426621ef86256`  
		Last Modified: Tue, 31 Oct 2023 01:21:10 GMT  
		Size: 61.6 MB (61620251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949858acc4967b0dddc39afca7b6e606ae12e1e3c01107a16cea0c28f6e58e40`  
		Last Modified: Tue, 31 Oct 2023 01:21:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
