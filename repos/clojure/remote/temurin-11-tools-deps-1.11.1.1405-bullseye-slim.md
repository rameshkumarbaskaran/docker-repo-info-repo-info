## `clojure:temurin-11-tools-deps-1.11.1.1405-bullseye-slim`

```console
$ docker pull clojure@sha256:1570ea6802874e604c602d315540da3f640a41916554fa95750677c34a667520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1405-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39734451fcd1e48b4b8a74c510a4a0b796c7720706984881be82698b81cbdba6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233240913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043f2e7d0fe48accae54baad4555f5f57f84e2722cda2e7442a546a1eba83630`
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
# Wed, 23 Aug 2023 19:44:06 GMT
ENV CLOJURE_VERSION=1.11.1.1405
# Wed, 23 Aug 2023 19:44:06 GMT
WORKDIR /tmp
# Wed, 23 Aug 2023 19:44:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "e02966d807e5fcee40d3aeee823196fd296cb97e91746f444ac8c6681731b354 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 23 Aug 2023 19:44:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 23 Aug 2023 19:44:21 GMT
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
	-	`sha256:fd5677e6854d173ab5148a6360925b461bd434cb5067638c7b4c5ed807ca3502`  
		Last Modified: Wed, 23 Aug 2023 19:50:15 GMT  
		Size: 61.6 MB (61612250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dde9ca0c9bccc810ee15975aa829ed3ef1e8f5cc48f0343a6e45de3aeefa6b`  
		Last Modified: Wed, 23 Aug 2023 19:50:09 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
