## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:fee51401416ab4e5e2952ff34143a6d194ce61352c5a80105225662af04751aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cad17fb866687fa20530316c6aa874a661e902f4f5a103a85bf5ee8e2221eee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196520380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b739de01898428fdbedcbff4981c677ff5c1ea60a17875de50549f32f210b617`
-	Default Command: `["clj"]`

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
# Thu, 02 Nov 2023 01:56:58 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 01:56:58 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:57:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 02 Nov 2023 01:57:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 01:57:15 GMT
CMD ["clj"]
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
	-	`sha256:15dd32204c6c4961f034d664c7f0c8312348f58138c76cf915e66424d16ac003`  
		Last Modified: Thu, 02 Nov 2023 02:07:00 GMT  
		Size: 61.5 MB (61503590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f721a5f10187a21a2e5f503dc1c26400a317ebb778ba44dacb83e785a960d28`  
		Last Modified: Thu, 02 Nov 2023 02:06:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21c5033fd5d9d3ba6f633764ec25f1aa49f89a91b4d76dfb1e476c850859989c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194386355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e44c56b4cd37f007afa995e5a65f010ce296d8f90107abc18dc64915240904d`
-	Default Command: `["clj"]`

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
# Thu, 02 Nov 2023 03:34:05 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 03:34:05 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:34:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 02 Nov 2023 03:34:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 03:34:20 GMT
CMD ["clj"]
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
	-	`sha256:dc794eafea93f57794aee2e4037b0291ae35094523fee80d7fdb68c669067ed1`  
		Last Modified: Thu, 02 Nov 2023 03:41:42 GMT  
		Size: 61.6 MB (61620303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887ed5b3649174cf4e4e7096159712b6973142d7589cca1d56771cf270d9957`  
		Last Modified: Thu, 02 Nov 2023 03:41:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
