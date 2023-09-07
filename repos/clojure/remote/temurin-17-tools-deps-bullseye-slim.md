## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:52e97e038fd5bc3dc3806c561d5fbda7074f48b34e8dbc9b72adc060ef421c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d56fa7592329b70d75c4b1eceed403a675fa3751edea5d4a5af5a253d9433b7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237688605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b37c0eb9a3f68a43c8fe183ff68d0eff4b42dc7747043e91aa095c89c435d6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 02:03:47 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:24:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:25:58 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 03:25:58 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:26:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 03:26:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 03:26:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:26:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:26:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d09690feda2ec5aced0543a2cf8ee1aadf1e05dd333f551cc4b11eaa287a0`  
		Last Modified: Thu, 07 Sep 2023 02:06:03 GMT  
		Size: 144.8 MB (144775798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e699b99022e3644744bdc3763c5c7a59532b9eda1c19b9495c9eedf26c6edf1`  
		Last Modified: Thu, 07 Sep 2023 03:34:29 GMT  
		Size: 61.5 MB (61494291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b99c929d3f7eedcc45140eef67f23d27c6d86698a2fd509c29554b926ee049`  
		Last Modified: Thu, 07 Sep 2023 03:34:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6498c3ba7f1eca16107fa1b20beb95c40686a1932060e114b66d56468852ac`  
		Last Modified: Thu, 07 Sep 2023 03:34:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d56bc6c3d4ad7f6e3790dbd86e3e42193fa0aab734bf5346ce29c400f88fe91d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235218789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cab92b74782bb354220d9e5b08fbcea5cea482841a24936afe768f750d33e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:48:00 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:48:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:49:57 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Sep 2023 01:49:57 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:50:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Sep 2023 01:50:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Sep 2023 01:50:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 01:50:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 01:50:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75390d7bc4a96162e240272aeff28881955f7af498179aa85faecd879748f913`  
		Last Modified: Sat, 02 Sep 2023 01:55:46 GMT  
		Size: 143.5 MB (143543515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03dc17b915978012134be2e29b4f89c5c9c01664b8080862a16428e4a86fe9`  
		Last Modified: Sat, 02 Sep 2023 01:57:18 GMT  
		Size: 61.6 MB (61611440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0bbf82a7d999c46f1a91774ae920d7673309443101cd2ddc5881870482cf82`  
		Last Modified: Sat, 02 Sep 2023 01:57:12 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e06cacbc944d5277917665a2eb9b7d65adc620b49e435dc3cdac269231a8a`  
		Last Modified: Sat, 02 Sep 2023 01:57:12 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
