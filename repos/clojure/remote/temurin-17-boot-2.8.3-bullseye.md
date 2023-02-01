## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:d9f7bb51160f929475238267795253c01612ddb83f83ae38cbfc8c41442862d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:269f9ea64eb534221d8b18b7c70245abaeda3bb0b67aa55d8c05dae56aea666f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308645166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c3ce21705df9573be5cd5ccedd73be7a30ffc1db66d4c10921a9173d34fdc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:29 GMT
ADD file:917750a82b29f8f7f88a121017bd9dfeb0fbcc8f0697a009f08b6b58246eff4b in / 
# Wed, 11 Jan 2023 02:34:30 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:18:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 03:17:31 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Wed, 01 Feb 2023 03:17:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 03:17:33 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Feb 2023 03:17:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Feb 2023 03:17:33 GMT
WORKDIR /tmp
# Wed, 01 Feb 2023 03:17:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2023 03:17:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Feb 2023 03:17:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Feb 2023 03:18:04 GMT
RUN boot
# Wed, 01 Feb 2023 03:18:05 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Feb 2023 03:18:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Feb 2023 03:18:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bbeef03cda1f5d6c9e20c310c1c91382a6b0a1a2501c3436b28152f13896f082`  
		Last Modified: Wed, 11 Jan 2023 02:38:42 GMT  
		Size: 55.0 MB (55025206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0699e5bbdef14668bbceef793e64bea067346a8ac79edc3b4b14dfee1d1be3`  
		Last Modified: Wed, 01 Feb 2023 03:33:35 GMT  
		Size: 192.4 MB (192438145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a3c192801029ba27ce2628b6b5f146a6675715a2b4f70d1070fe153d797f8e`  
		Last Modified: Wed, 01 Feb 2023 03:33:20 GMT  
		Size: 2.4 MB (2360735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d01d7917d1fb5bd5d2849fd9551d0609efe300aab11696631a78a32e9b55f2`  
		Last Modified: Wed, 01 Feb 2023 03:33:24 GMT  
		Size: 58.8 MB (58820680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22369836feaf414fc3cfad532b70ddabcc20bd0104851735d8bdb18059a5d735`  
		Last Modified: Wed, 01 Feb 2023 03:33:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9fe8402695fe9e3a6c1bbadad704c80c479500e60f56e9a62c8320ba077cca86
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306113640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d945e430ffa6932c677f8a5ef3b0b8dc77434e23795a6828f9781317e89fd23c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:24 GMT
ADD file:9e185c2d9ca8a231a39ee2b1761fcdff75065252d25a65a207acb7a319c1cf23 in / 
# Wed, 11 Jan 2023 02:57:25 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 20:54:01 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Tue, 31 Jan 2023 20:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 20:54:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Jan 2023 20:54:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Jan 2023 20:54:05 GMT
WORKDIR /tmp
# Tue, 31 Jan 2023 20:54:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Jan 2023 20:54:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Jan 2023 20:54:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Jan 2023 20:54:26 GMT
RUN boot
# Tue, 31 Jan 2023 20:54:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Jan 2023 20:54:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Jan 2023 20:54:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c345c9e441f5f49235768af74b8ab37743652d38958afaa000edd56d7b2f0540`  
		Last Modified: Wed, 11 Jan 2023 03:00:56 GMT  
		Size: 53.7 MB (53681859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f61d91708311a5923680a9fa5ce56fc7a173443a91b20c1941a3baab459e19`  
		Last Modified: Tue, 31 Jan 2023 21:07:15 GMT  
		Size: 191.3 MB (191260441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefd809c14a6ec784cfb1ee90836e5f999f4cf2ae94ce5167b9f58432bebca37`  
		Last Modified: Tue, 31 Jan 2023 21:07:04 GMT  
		Size: 2.4 MB (2350670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01abbdc1d447d9c300ffadc75ca1e4a1c84125856f249fe8547dca652c5aef7a`  
		Last Modified: Tue, 31 Jan 2023 21:07:07 GMT  
		Size: 58.8 MB (58820268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043a984918a0cb8bdfe9072aefa9ff7f1b0ba7fa902d8b5f91904cc8dd46ae4f`  
		Last Modified: Tue, 31 Jan 2023 21:07:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
