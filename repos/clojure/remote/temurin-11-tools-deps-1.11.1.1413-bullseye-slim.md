## `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:d1d96e1d0b5c7b7591dc3f5e25f2ea511af333be3934a28a82e8e29476db75a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29b46e75ecad3d306947404b7c26cc633f1f8a0120bae1512ad5f03fcb5b83ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233239804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1936b2da5252640bc5a2e393364b3e7fcae1c4cd870098e03faf9005360fa32e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:42:38 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:42:38 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:42:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:42:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:42:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1b1b0243d7471d0e2fffbccfd65b8e8fed25ce1f9fb854c70f872afa006e7e`  
		Last Modified: Mon, 28 Aug 2023 19:48:52 GMT  
		Size: 61.6 MB (61611141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4222f91d82ed7fdd94d711f878348646234f7234c8e08511a603aa243c9ff51c`  
		Last Modified: Mon, 28 Aug 2023 19:48:47 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
