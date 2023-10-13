## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:5283dbfc245dfd308d735187b62f549ced4841a8aa808f0e5ce93bd9210f9b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5afe9bd8c45456de46d0d21bb762a35a50bb5f52f541c25cf1a133f7a01ae23b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277774137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e701fb83e1c27ef2909701c1644d227b4be6aba2ef67c9a15beb73a51a4efb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:30:47 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:30:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:32:59 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:33:00 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:33:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:33:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:33:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aebae23ea933618b87b53119336b32efadee3d48ee7cd73f6509a2ede465084`  
		Last Modified: Fri, 13 Oct 2023 01:46:18 GMT  
		Size: 144.8 MB (144825980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1a6b85800b4d40ca312c265699d32991fbab6d04e275d7275c2b50d73323c4`  
		Last Modified: Fri, 13 Oct 2023 01:47:28 GMT  
		Size: 83.4 MB (83365318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12c23ff2d84d3065cb99cf7eda34110a4dc47274e23f365a086f395839c91b3`  
		Last Modified: Fri, 13 Oct 2023 01:47:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:41db9cb56051d65babdbcba115c1af150432fc0e2b899250b1573edbd9767745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274302028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af42b70bac96110bdb8a58ea490a2fdf27d0a9289de49fda09356fe580c00b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:02:05 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:04:02 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:04:02 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:04:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:04:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:04:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98472fc4a9307f34b7d88432e2590b0c37a40b019f0ab081812f6d3b2d7968be`  
		Last Modified: Fri, 13 Oct 2023 01:15:04 GMT  
		Size: 141.6 MB (141570720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df1f3ffe6386f8529fc520a59d725fb4034ecceff2789945ce1c3c1e322a30`  
		Last Modified: Fri, 13 Oct 2023 01:16:11 GMT  
		Size: 83.1 MB (83118115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ae90b96c181f1509617f09b1406e5ed0fbe2252a4ab89e4f89ab679f7a87c8`  
		Last Modified: Fri, 13 Oct 2023 01:16:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
