## `clojure:temurin-19-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:0afc3664857b7ebd9d5445a76d247e109b5f00de4b5f68143fd21beb2e27c600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57315e02213f9905696231629bafd7df88c50aac2ef860a9aef5cd2a99a28dd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317071647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96b7e849cd01d54c5e00f45c03bcaa7b7bf7c3b98c289a5fb5a0fe369f78c4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:40:10 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:40:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:40:12 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:40:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:40:12 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:40:18 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:40:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:40:18 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:40:38 GMT
RUN boot
# Wed, 05 Oct 2022 01:40:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:40:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:40:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39dc413a8bf8accdfa9d56cfc7b9aa47547fa5bfec61a15afe8626681e3df2ff`  
		Last Modified: Wed, 05 Oct 2022 01:51:46 GMT  
		Size: 200.8 MB (200843783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae44a6802a374fd6be8e6364c6f44a0cdbefb8199367a16745d10e513ffdb57`  
		Last Modified: Wed, 05 Oct 2022 01:51:31 GMT  
		Size: 2.4 MB (2360755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc99671ff734cd8a2192cbde2349bb11809719a3b38942f4af2afa2cf199e07c`  
		Last Modified: Wed, 05 Oct 2022 01:51:34 GMT  
		Size: 58.8 MB (58820462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dbf225bb21335849c746bfe8c937cc711209a1deb3658cb87e453ab5d40781`  
		Last Modified: Wed, 05 Oct 2022 01:51:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6b1aa703f4f522f6afa1eeb525d92a4903b7ae9a644e7952a850629b72dbfab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314244063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a098f713502ed44634918ef9a5a885af2def341b0bad25af8670a9325c2b7f34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:04:33 GMT
COPY dir:58f6c37df253d3555e493197f96e3f21593e31d3faf1967e0a7b9d8f0ae9e30c in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:04:34 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:04:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:04:36 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:04:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:04:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:04:44 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:04:59 GMT
RUN boot
# Wed, 05 Oct 2022 01:05:00 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:05:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:05:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf37d84f42eaa21611ea540fea88bea6b18861b24ed7b7691a2ba8a5f87f4fc`  
		Last Modified: Wed, 05 Oct 2022 01:20:34 GMT  
		Size: 199.6 MB (199582867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0db1c0fac3f4dc518aeed489e7268c34d18f36efb48ff6ba609020436aafefb`  
		Last Modified: Wed, 05 Oct 2022 01:20:15 GMT  
		Size: 2.1 MB (2144477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82922abde58e2062a31754937aabb3d79344ef0610f826851d6c4538e6a9f485`  
		Last Modified: Wed, 05 Oct 2022 01:20:19 GMT  
		Size: 58.8 MB (58815696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f93adfbcf9b6a92cd9d6e97260e7275e9332dbbe2446ceb7463435844012da1`  
		Last Modified: Wed, 05 Oct 2022 01:20:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
