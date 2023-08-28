## `clojure:temurin-8-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:c86c118137fe5ac074262ed7564e2eb857217c7f71d24f48e866dc1b025abe90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef2828a3a5c7e4b33755073ce26b64fbb974c6ed85448203a2636247732affb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194365552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9960345fca261f42d52790fc505e2ccb795996871d9ea6037445c50b8ed7432`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:46:48 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:46:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:40:43 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:40:43 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:40:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:40:57 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:40:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab72539caee6a49c911d508260d1eb9ece05d94c06a86d77b415da3e7508716b`  
		Last Modified: Wed, 16 Aug 2023 01:56:31 GMT  
		Size: 102.7 MB (102690456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d455b9f0db839dda841da295ab7b369c7d2b1e4a8206b8474488b00848d6372`  
		Last Modified: Mon, 28 Aug 2023 19:47:35 GMT  
		Size: 61.6 MB (61611661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f96ec6d79b415ce5be42dc4b16cf5713e47f552b6e2079f20da66baecf8e52`  
		Last Modified: Mon, 28 Aug 2023 19:47:29 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
