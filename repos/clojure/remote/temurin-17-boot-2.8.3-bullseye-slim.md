## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:b1bb192c8c2af2441574dfe658b4e3ca79155c20310b9b7bb44238ae00c2c4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c9c98d7bf3167b6a14e53edce0044b9c2be841f3a2bc088ca9c1d42c3f9880ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283455808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bf547cc38da72189fe317828d833eebc347c01266c809f71a845b2bca77268`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:37:41 GMT
COPY dir:4a40d0ddbd507a7d3b3a97117be800fbf93534cac954d63629e4fb22f3cd41ad in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:37:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:37:42 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:37:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:37:43 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:37:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:37:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:37:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:38:09 GMT
RUN boot
# Wed, 05 Oct 2022 01:38:10 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:38:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:38:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886809c89616aad77af0691ec37718e30fdcda3a35959fe64d1b37b7e2cfda5`  
		Last Modified: Wed, 05 Oct 2022 01:50:00 GMT  
		Size: 192.1 MB (192137460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e028201dd22642bf74c2c606e5dd1e4a186f1a2903b64a3ffc56c0a796825fff`  
		Last Modified: Wed, 05 Oct 2022 01:49:45 GMT  
		Size: 1.1 MB (1077315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dabb980eb7e8939b89684f37069a83a544a0515ab23de8f588df8e3a5417650`  
		Last Modified: Wed, 05 Oct 2022 01:49:49 GMT  
		Size: 58.8 MB (58820531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abead984700316fcc2e4c79451596e43172a0263c8ac6a71e1084ab37b296c0`  
		Last Modified: Wed, 05 Oct 2022 01:49:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7e18413e992abacba8dc464d62b9f4072ef77aebde858090fe95ce7b91b2da1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280644385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a2636a23944dd903eee74dc5ca26babd3a2860a9247239d2cc2a82be4e442e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:01:21 GMT
COPY dir:e8b09aac8a69a5f07df362ceeac55cf5f3321b4ba40e9b02e12250e34b34e83e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:01:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:01:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:01:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:01:24 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:01:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:01:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:01:32 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:01:48 GMT
RUN boot
# Wed, 05 Oct 2022 01:01:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:01:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:01:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a6c1d832d4d9011c73ee876bbbbdc9b3b0a7d057d4ff04d3b4078597e6a527`  
		Last Modified: Wed, 05 Oct 2022 01:18:30 GMT  
		Size: 190.9 MB (190904314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a13e19f0dd70ab2f622ffaaf3182458bbd0bff90f88987f4d239c804d42d9d`  
		Last Modified: Wed, 05 Oct 2022 01:18:14 GMT  
		Size: 859.3 KB (859272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3248210adf28c29b0793c5c460d0c4d2ae73c3f9908d03ac094aa49a92dd4`  
		Last Modified: Wed, 05 Oct 2022 01:18:17 GMT  
		Size: 58.8 MB (58816005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e2b6b8c780eea6186d562e2a10f82d32930c0e46f0850c696789d3ca499019`  
		Last Modified: Wed, 05 Oct 2022 01:18:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
