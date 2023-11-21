## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:44e835235fef7feabfb1604b5fc03238d49671e639fbacb9b4396b6cf5c1b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b7a10c9db6e6634feee11cf79700a142db494e70e22711b54fa0704b000a235
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237796367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80db3f65170d3a33d278e014f34f64febe291fd2e1128755cf4fa1bb68d6913`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:24:07 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:27:20 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:27:20 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:27:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:27:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:27:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:27:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:27:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c20750b154d64794fedb0a429e74999708e8bd1d859c9bc36ca5afefa982a25`  
		Last Modified: Wed, 01 Nov 2023 01:40:50 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc667bcdb25b51c94fc2f66759828bf5b389cd7485c07bb0e617b650c9b43d7`  
		Last Modified: Wed, 01 Nov 2023 01:42:55 GMT  
		Size: 61.5 MB (61503531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c87d65a2bb99c18869367338d484feb0c4b2e7eb359bef5e0c4503deaab255`  
		Last Modified: Wed, 01 Nov 2023 01:42:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eca7cfd05a31e0f85d64713f066de895dc9f345cc5c8b8ba8f2262d126be277`  
		Last Modified: Wed, 01 Nov 2023 01:42:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa6b2e49cc420e912a099a805ffce041e6a3d5a2222b7d96d97caaf304b1a7b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235367205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e9cd5a81fdc6ac5da5ff72bc2bb4a852b5baf2465babf9638246ca30e98daa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:35:08 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 21 Nov 2023 07:35:08 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:35:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 21 Nov 2023 07:35:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 21 Nov 2023 07:35:22 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:35:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:35:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe46eadb54987b3bb620c0a9d36df587f6f49d8762251e6fcd673d216f2f0563`  
		Last Modified: Tue, 21 Nov 2023 07:49:14 GMT  
		Size: 61.6 MB (61620353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbe8dcafba42b1950b9cbd6f5071d376a478dfb38ae3045136f9d018bb506b8`  
		Last Modified: Tue, 21 Nov 2023 07:49:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece9c66f80364316edb722d7758f01e07f85c0ff2e83d34265fcd50c7ef25e42`  
		Last Modified: Tue, 21 Nov 2023 07:49:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
