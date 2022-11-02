## `clojure:temurin-11-tools-deps-1.11.1.1182-bullseye-slim`

```console
$ docker pull clojure@sha256:c80b2dfdb9c029f0d1b3fd795cec00269549d21e1f03bcdbda3a5c8d091da685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1182-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:606d5605393721917f02498ab7aff20e5bad0b5b1e340fc1d5b2beb40c2e3d42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291018628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7082dff7ce2ebae697cc5ae5d46325fe0a58fd2eba382d58ea43160d0dd6ac1d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:11:14 GMT
COPY dir:24028fba84faa85b57bc32be14abf8fad6a4bd4db557cb5499b6d5cf38d97646 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:13:59 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:13:59 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:14:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:14:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:14:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9424e0e92a9d7ac25f2f902e3550e25f0379d53b383d802d0c0a9174fddd9e5d`  
		Last Modified: Wed, 02 Nov 2022 20:24:52 GMT  
		Size: 198.1 MB (198124751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e91cc903054ad56cf2c790404b5f921896cc733aac304e1e3014f4c1e3883e`  
		Last Modified: Wed, 02 Nov 2022 20:26:28 GMT  
		Size: 61.5 MB (61473221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873dada2bdfd7932d5dd3f2e2ca2182cbf6a4916f698a19aef2ed144383195a8`  
		Last Modified: Wed, 02 Nov 2022 20:26:20 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1182-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d7eceb83a0f9ea4f3862105380b5ef086c93d076b89d0dbb3af4d42f3a5e6c9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286524909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b161810374842ebd030a2298170d21028db4d65dd4c471b1d4eff2a571e6002`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:47:12 GMT
COPY dir:e48336735658172388295f760b71f5f10a9b7d3f960c6e4546718a38dd6452e7 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:47:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:49:29 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:49:29 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:49:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:49:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:49:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc966be4bd15170671412b817450394760b037c8e5e3587768bfc3bbd123d53`  
		Last Modified: Wed, 02 Nov 2022 20:58:36 GMT  
		Size: 194.9 MB (194867681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4acc0dffa766373db7cc54acbebca990aad9b4a565613c61284f520d66ec56`  
		Last Modified: Wed, 02 Nov 2022 21:00:11 GMT  
		Size: 61.6 MB (61592699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db57e8957e946bf764cb6f94de6c8cb9b27e687a25dff3c084713e8eafdfd0a2`  
		Last Modified: Wed, 02 Nov 2022 21:00:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
