## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:41fe229cb269d343594726cc4b588edb42439c0bd1b88033128c56bc856c14ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:78454bc986e7832c11164f57eef1161bea912bd5c701150b16f3c9bd9a27f46e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230522224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1266cd6b720e40fcd022d09dd8db227ed5324eff206adb8b3d0f6dfa4fcb939c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:26:08 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:26:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:22:22 GMT
ENV CLOJURE_VERSION=1.11.1.1405
# Wed, 23 Aug 2023 20:22:22 GMT
WORKDIR /tmp
# Wed, 23 Aug 2023 20:22:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "e02966d807e5fcee40d3aeee823196fd296cb97e91746f444ac8c6681731b354 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 23 Aug 2023 20:22:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 23 Aug 2023 20:22:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a5a5971aa40d66285a278288b640fe204504a1357230ee711761ceaf3a5937`  
		Last Modified: Wed, 16 Aug 2023 01:38:52 GMT  
		Size: 103.6 MB (103585023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6740cff1c4687669011931a205047f36ccbb48a0e10a3ef8eef5cd99f9d875`  
		Last Modified: Wed, 23 Aug 2023 20:31:08 GMT  
		Size: 71.9 MB (71879960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f37afd48cdd8fa70bd4381ecdce320f92a4e80543025f65e11b06621922eda2`  
		Last Modified: Wed, 23 Aug 2023 20:31:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a49b6c0335cf51cea014be6731e3dc24a834f5981a2cca7824f3cd93cbfb2f07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228393682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041a0e9ce06c35cfc4a58ba9c466f1eb63e179c6c3285aaa73054168ef0a4229`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:46:16 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:46:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:40:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:40:19 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:40:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:40:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:40:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e72ffee157aface2093ca7b44ca1e9d7d8010e8b3344c5760c1ae633be3d0`  
		Last Modified: Wed, 16 Aug 2023 01:56:15 GMT  
		Size: 102.7 MB (102690463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748cd1a0103b904db491d832eb8a776e6e4a331fdde30a01908d81bf07e00a8e`  
		Last Modified: Mon, 28 Aug 2023 19:47:19 GMT  
		Size: 72.0 MB (71997821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03916d44b232125c3ec91166af93fcca3ddf3d81e34c54a652c5e4f880b0b41a`  
		Last Modified: Mon, 28 Aug 2023 19:47:11 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
