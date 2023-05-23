## `clojure:temurin-20-tools-deps-1.11.1.1323-bullseye`

```console
$ docker pull clojure@sha256:8ae2b3b406751d41e16ff5a991437da103507c5038fec7fd84ee0012db2e456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-1.11.1.1323-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8e7d5294416265ac03b139b577ac2df2591efbd90cf88c5c919ad1339bc6a8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329742429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630ff6e7f6f889286d8da2a1a1f72d8bf8e680313821f2a6454eb19025229be2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:12:29 GMT
COPY dir:02736280d197ac4d1b6ebf68d948efb46e7eeffd579505356f8c94946dbcce6f in /opt/java/openjdk 
# Tue, 23 May 2023 08:12:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:13:21 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 08:13:21 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:13:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 08:13:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 08:13:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:13:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:13:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bd6746ac717445327aa16f009827ed695c23cdff0fd0c8eee5b8aead9dbe50`  
		Last Modified: Tue, 23 May 2023 08:20:09 GMT  
		Size: 202.8 MB (202813964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47eb3a387a300d4c0cd9f756e31382b95f2a2bf65398daf737e915caaf159016`  
		Last Modified: Tue, 23 May 2023 08:20:50 GMT  
		Size: 71.9 MB (71878422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4640d3bca5cb815fc5be99b4412cf1614816ae011c4b4d3dfa13937a8fce7e75`  
		Last Modified: Tue, 23 May 2023 08:20:43 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70221613b6051137f228381d9660f05f9470698b9a1bbb2641f9f16bc5dae1c5`  
		Last Modified: Tue, 23 May 2023 08:20:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-1.11.1.1323-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96e58fdb7fa1aca3af3c227a4162b244dba1082949140beadf8b201a56b43aec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326846164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b034dbebc5fdc24ce0c2981c98f2ca5caf9ba3e3920f2cbbad56379643ee8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:31:43 GMT
COPY dir:f555428af67a610819205eec573e23f479077e0999818ee9dc0f3375599d21db in /opt/java/openjdk 
# Tue, 23 May 2023 01:31:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:32:32 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 01:32:32 GMT
WORKDIR /tmp
# Tue, 23 May 2023 01:32:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 01:32:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 01:32:46 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 01:32:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 01:32:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d72676a8287a859ac8d81d8fd618b87b45fc2856a39d92b8d00911f0c0630a`  
		Last Modified: Tue, 23 May 2023 01:38:41 GMT  
		Size: 201.2 MB (201157969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a60fb0e3d6f03ac19327155488e8afe0ce5f75bfdceb6f5c6d0c140110678f`  
		Last Modified: Tue, 23 May 2023 01:39:16 GMT  
		Size: 72.0 MB (71994567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d436872e210dc073ed1ad193345e0926c574dfbe2b6b98e79d2327f24c542`  
		Last Modified: Tue, 23 May 2023 01:39:10 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc076a5e32ab6362aa7e21ffd15c5fcf799b8f830e4ccbfe0fa2234142daf40a`  
		Last Modified: Tue, 23 May 2023 01:39:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
