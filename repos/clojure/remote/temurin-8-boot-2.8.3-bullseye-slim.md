## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:a32861d607ac14e48859bdb17ea601b3407c0ca5817f15c367f6c733e67e8884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a90fd898d5543e929b03e04e6d4c70e6b6f73257cf5033967b0d6d1e6f7d1426
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194916125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9477d499bf4100d5434048806f0c701cbe48e81e01b82af9d85872905338d0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:51:34 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:51:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:51:35 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 01:51:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:51:35 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:51:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 01:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:51:41 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 01:51:58 GMT
RUN boot
# Thu, 02 Nov 2023 01:51:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c15742b5535ec5ec2a9edde367698d18fe8703c470733bb3b4614ce245fdb3`  
		Last Modified: Thu, 02 Nov 2023 02:03:33 GMT  
		Size: 103.6 MB (103598259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c985028f95d5cf2ff9d73b72dab74c3dd8f2a0c10b1536cf3b1f207f5063423`  
		Last Modified: Thu, 02 Nov 2023 02:03:25 GMT  
		Size: 1.1 MB (1079478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bab54de7e7b917b901e8830dc2c713830421d0837df3d358fee58d0a3adc00`  
		Last Modified: Thu, 02 Nov 2023 02:03:27 GMT  
		Size: 58.8 MB (58820473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:455f96514896730b77a6a60a60a3b5a48150981ef3d6da88d5ec4fbbc066cafe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192652874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e707217a365d4a0d645646e993e3391523d3eb59b22c8d16075f538c004c7fd`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:23:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:29:43 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:29:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:29:46 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 03:29:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:29:46 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:29:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 03:29:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:29:51 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 03:30:08 GMT
RUN boot
# Thu, 02 Nov 2023 03:30:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5c79e0d960ea2001fd6bcca81c33c59a0e3ec3c1a90343025509018a51c36f`  
		Last Modified: Thu, 02 Nov 2023 03:38:55 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1cc6014ebbf0c7927552b3699af5c25dca325b79ca8a506ee483e7545ad669`  
		Last Modified: Thu, 02 Nov 2023 03:38:49 GMT  
		Size: 1.1 MB (1066866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6cb81870531db27defa9263763bb05c92d778bc9646169c88e0cb7304d642f`  
		Last Modified: Thu, 02 Nov 2023 03:38:51 GMT  
		Size: 58.8 MB (58820572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
