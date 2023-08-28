## `clojure:temurin-20-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:4556c48cf85691edbece3be2c68e7d2bd4fe4dfbc811884a99dad6d9f8e6768a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e46df61291fb12416ed64044012fc27177ad352471c7836288c8eb7aa40effc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243794643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742e84c8039702afd21483ec4f22c175bcc8d9fcda01a1b1cf9a62ae82f5e2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:53:50 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:53:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:45:18 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:45:18 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:45:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:45:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:45:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 28 Aug 2023 19:45:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Aug 2023 19:45:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b04b4e3bfe044338b1636c6d1fe76f6e2c078f769b995d868ef50c1b27e924c`  
		Last Modified: Wed, 16 Aug 2023 02:01:19 GMT  
		Size: 152.1 MB (152120026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5970252ec535f249b1151c3023701210f42012a64add2fba90c6772a9a1864ee`  
		Last Modified: Mon, 28 Aug 2023 19:51:41 GMT  
		Size: 61.6 MB (61610784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4047f087205687ed62752272126808b5c090c778df72d81184bc954125958c1`  
		Last Modified: Mon, 28 Aug 2023 19:51:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcfce2ec59a6cd6ea29266c2b704f4fefeb40aceb63fd9af36475ab9f65b585`  
		Last Modified: Mon, 28 Aug 2023 19:51:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
