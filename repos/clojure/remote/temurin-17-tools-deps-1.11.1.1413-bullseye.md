## `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:44115d6b0a876665f97466f2d5f4519d4dabad55c21316d6ef82c81ef9a56b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc044198fd8fce0ae4f81074c8089e42d50657ce61268bcf6c58a93b61e6684a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269241625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb99c384399db46d78365bcbc74d6e367cb077943d4cf72cf61fdadcd74de41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:20 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:43:42 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:43:43 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:43:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:43:57 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:43:57 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 28 Aug 2023 19:43:57 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Aug 2023 19:43:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f1b0394be128a63af2359d89c3282164b67cd2fac29716c6f2f5e348ec07a`  
		Last Modified: Wed, 16 Aug 2023 17:34:01 GMT  
		Size: 143.5 MB (143538089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4567a1dde34cb43593837317f26dc485fcf0a1305b685aecc71f6e5a63be0677`  
		Last Modified: Mon, 28 Aug 2023 19:49:54 GMT  
		Size: 72.0 MB (71997740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c63dc81eeb8096d28af8d7926408b4a014684e90a73a439470fc26df4c1c32`  
		Last Modified: Mon, 28 Aug 2023 19:49:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267ce812af3239b9a5fb89c7374a9083f9c3658c703b68474a75740ea56d9a4e`  
		Last Modified: Mon, 28 Aug 2023 19:49:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
