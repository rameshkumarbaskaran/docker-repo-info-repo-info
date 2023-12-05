## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:e69c19a81466eb99ba49f7335f462998c59f826df1a4f1ab107c8da8a5b07c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a91d09bc2eec8e07bc0d9bd1ae2119eaabea31cfb4014e1f2aececc184c204f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204892742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bfc2daa31204eb7067ee332fca56a62c0590d2263cf08563bd5313197580a5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:09:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:23:01 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:23:02 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:23:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:23:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:23:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea90c3a76d5ae0f9f3f2436cc57135b1df73c229285da25a50b8cae0bd84e9d5`  
		Last Modified: Tue, 21 Nov 2023 10:29:01 GMT  
		Size: 103.6 MB (103598255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e8f012c86892efcbae42e63945076a76ce3efe844b13d7b4d92d79c2b3fc5c`  
		Last Modified: Tue, 05 Dec 2023 18:36:20 GMT  
		Size: 72.1 MB (72143962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd3a4b725c655f7f7a965a25da3589a47326ba33855ce6cfaeebd41fb9e47d7`  
		Last Modified: Tue, 05 Dec 2023 18:36:12 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e61f51d7a8006d6f0b97fe806fe5a428dd40d24802cde6cb195adce1a498b4a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203779007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14369c82c08ba5bf30953a01648984842d9dc94dd9fb80714753bd2ea3e0e07f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:22:02 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:22:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:39:55 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:39:55 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:40:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:40:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:40:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cedbb3bb41e2be2e3ff2758dd69db21f5b24c910e7f00d1abbb4d1491e79fb3`  
		Last Modified: Tue, 21 Nov 2023 07:40:14 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ae9e124014f51b21997c56a002a7b71f2d8600ca61793d40cbeb2d94aba5c`  
		Last Modified: Tue, 05 Dec 2023 19:50:54 GMT  
		Size: 71.9 MB (71897581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e67d8dcf1b1554e06b3a729bbcec3b98a418d6931231e7211836751355cb8fe`  
		Last Modified: Tue, 05 Dec 2023 19:50:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
