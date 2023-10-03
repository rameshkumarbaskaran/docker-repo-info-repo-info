## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b71c4c972afca8f92146c8b93a3c5097b7c33b2315441cad64ed83a44e1a2141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:235f6bf81d269177a9c876688b092fcbcd3ef758bdd99add7cc21255bdb172ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237689116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc61b65cc8129eb1650f3363373f41fd79b3a611008527fe51302c047dc0254`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:44:13 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:44:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:49:21 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:49:21 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:49:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:49:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:49:38 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:49:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:49:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0567cd6aa99e5db3b54cc244cfee493561efcb8009ca2dc2c87b8c882d0bd562`  
		Last Modified: Tue, 03 Oct 2023 08:56:51 GMT  
		Size: 144.8 MB (144775742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a66e86f5e70cb37299f3bd7a1aaabe72ed3ab0d8878b3cf6bbb45f4f8b2a07`  
		Last Modified: Tue, 03 Oct 2023 08:58:34 GMT  
		Size: 61.5 MB (61494645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a3be6b044a709f4750901762b2a42a71dff8e03f6cf045295017c7352b7872`  
		Last Modified: Tue, 03 Oct 2023 08:58:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf66507f831145321c5c7dc6c7765f6ea25a18c00dc20305b0e63d9700e67f7`  
		Last Modified: Tue, 03 Oct 2023 08:58:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d40ebc95e25e1a6c3f603b6482c25d67118aaf294d74e52f3d9e8e0e699c261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235218870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabbbc16879dd6effe0ebc11de8906f8d6d95a58891e07737f7ca0ecd98340d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:48:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:32:36 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:32:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:34:41 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:34:41 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:34:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:34:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:34:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:34:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:34:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0f8e5bf90a9369ab6f51e945ac866f2ec10afab1f1331f92ddd272ac850a21`  
		Last Modified: Tue, 03 Oct 2023 08:41:12 GMT  
		Size: 143.5 MB (143543520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c96c098d53e92d6044955916f0e4d11208adaa4b50ff1f0873e3bd7e33ce906`  
		Last Modified: Tue, 03 Oct 2023 08:42:50 GMT  
		Size: 61.6 MB (61611465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab023f5ec667972b564437b160f643219e3f8534feb9e5ccef7e2bfbf8a57625`  
		Last Modified: Tue, 03 Oct 2023 08:42:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53351dcec976beba6eed810e2d477d468333da4bc8e611d41727de3ede88748f`  
		Last Modified: Tue, 03 Oct 2023 08:42:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
