## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:fda5a91491e5b4c36a40edef1e0a88082c5fb7250af2f8c5bd08d421b40395b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:35ade6ad89116fb5cf734ff78a6fb3ad6ffd70f1bd5b94bc28bdac05f29d3ffd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308365559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f3906de96c7b4427cc5b9fdada7ed46041eaea86400aac64154a26da861a1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:37:02 GMT
COPY dir:4a40d0ddbd507a7d3b3a97117be800fbf93534cac954d63629e4fb22f3cd41ad in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:37:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:37:04 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:37:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:37:04 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:37:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:37:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:37:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:37:34 GMT
RUN boot
# Wed, 05 Oct 2022 01:37:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:37:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:37:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246324c7fe2aef771872cc58b2263426b55fe7dac3971cdd927d7d8f31e97361`  
		Last Modified: Wed, 05 Oct 2022 01:49:36 GMT  
		Size: 192.1 MB (192137613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb23de530cd0a2ee4af4140f49dcffd1f7503addb50f8e39dbce7103d8f1ffa7`  
		Last Modified: Wed, 05 Oct 2022 01:49:21 GMT  
		Size: 2.4 MB (2360752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0add84492a7e7ffba419c20ff7e2ac1ebe9c68ac7b25bd535dfa7cda3b3b8714`  
		Last Modified: Wed, 05 Oct 2022 01:49:25 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd0d5008c70148537e1c031260659412f68761267a694f4f1f24e7b7da335a1`  
		Last Modified: Wed, 05 Oct 2022 01:49:21 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3ee6438b051cf0fc1aa0ed1484a00e2b6e342a6cac51f0e371f6d24fe0270c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305565578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767e94598ed26f4e7039ad055c317d171fbc57d4ab50949b2f6c68fb06a6fda3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:00:39 GMT
COPY dir:e8b09aac8a69a5f07df362ceeac55cf5f3321b4ba40e9b02e12250e34b34e83e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:00:40 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:00:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:00:42 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:00:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:00:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:00:50 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:01:06 GMT
RUN boot
# Wed, 05 Oct 2022 01:01:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:01:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:01:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132b7e60c64f8a4fd0d535e40cea1fe52e0d5b1669f1b30376daf898759039f9`  
		Last Modified: Wed, 05 Oct 2022 01:18:02 GMT  
		Size: 190.9 MB (190904260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95b8b34303697c29d9919c51f6af2fe16d66c4df96f030b9f1441d386ed4714`  
		Last Modified: Wed, 05 Oct 2022 01:17:46 GMT  
		Size: 2.1 MB (2144347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c4b1a9a136d6bce30451a9a6c55556b9709aeb9a5bed64d7322782e66aca6e`  
		Last Modified: Wed, 05 Oct 2022 01:17:50 GMT  
		Size: 58.8 MB (58815945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2546f02a19c61c6f14f91b20e80a47b77e4c8f09f3dfb8cda67eb6ca59d0b0`  
		Last Modified: Wed, 05 Oct 2022 01:17:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
