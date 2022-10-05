## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:f9f33078bf5e181687bc1a6360bb4d52895b83a4b65fb5c9c5a4f8336c7c82a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9afdb38b79f944f5bca3879003bf24d5930cab7a86c5ead50eff93b167fc404f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314352493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee396b7c8de89a65bee1d92ac2e1e5cf1d39f1f3a5c2a75a8e202c9df43713f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:33:50 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:33:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:33:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:33:52 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:33:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:33:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:33:59 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:34:23 GMT
RUN boot
# Wed, 05 Oct 2022 01:34:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ca2823c2d209cf0f2e558aa4af2216e66a915bea0f57552265e9d46d73fa6`  
		Last Modified: Wed, 05 Oct 2022 01:47:40 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e665f838905a407e09136eee0a80f95b68b6e3cbb2ccf737d83dd485a4fbba`  
		Last Modified: Wed, 05 Oct 2022 01:47:25 GMT  
		Size: 2.4 MB (2360748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387178cbe4c62530b8d96d4d2de501075a3f82c5b97bf9b0a5e49f8bc1da0e67`  
		Last Modified: Wed, 05 Oct 2022 01:47:29 GMT  
		Size: 58.8 MB (58820610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39b8bd86d498c2fb240daef353535f3ef901597671da3fe22453ba163d60862c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309528963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27fbc7a3b110ad99b27df446ac9b45b431db21bc902bfc9e3df0eb9f51ae035`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:56:58 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:56:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:57:00 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 00:57:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 00:57:02 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:57:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 00:57:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 00:57:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 00:57:26 GMT
RUN boot
# Wed, 05 Oct 2022 00:57:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cb3f012989325cc0cd47bb9a1464650ba884c67cba33ababc47396363e616e`  
		Last Modified: Wed, 05 Oct 2022 01:15:43 GMT  
		Size: 194.9 MB (194867814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60331a45431d17049460de0b381186c454b4c09d2e635f7b96782f9adbf34d44`  
		Last Modified: Wed, 05 Oct 2022 01:15:08 GMT  
		Size: 2.1 MB (2144443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e69e731b25a7d33cb1896ff25fc99acaae773d9b4967ac43f9c5a91e946b8cd`  
		Last Modified: Wed, 05 Oct 2022 01:15:14 GMT  
		Size: 58.8 MB (58816081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
