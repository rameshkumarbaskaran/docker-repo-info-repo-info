## `clojure:temurin-19-tools-deps-1.11.1.1237-bullseye-slim`

```console
$ docker pull clojure@sha256:6677fc2ebb341444e484267b40fe1fbc07a33d8ff0c6bbe7eb44962d7f6d486c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps-1.11.1.1237-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e14220019b46f6519dd9b1a0dc3cb25a77843874575598ccfb480b6870b7e14c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (294010066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030822ad719db15667a6e3ae3eec8a1c5a09ce0193d7952cd2736eb8e6aa09da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:50:20 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:50:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Mar 2023 19:28:09 GMT
ENV CLOJURE_VERSION=1.11.1.1237
# Fri, 03 Mar 2023 19:28:09 GMT
WORKDIR /tmp
# Fri, 03 Mar 2023 19:28:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1cadeebb4ac96c7655f04c60369c6ea69968cc168b44e607df32aac739700751 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 03 Mar 2023 19:28:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Mar 2023 19:28:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Mar 2023 19:28:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Mar 2023 19:28:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b3ccae27fe03c16494d3c8f769e2249b243d16240726cb9587a989c25ac8d0`  
		Last Modified: Wed, 01 Mar 2023 08:01:12 GMT  
		Size: 201.1 MB (201112994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cac6a6fb9bd3a75369529ffc7064140f962837e5e21308b269be1744bf3104e`  
		Last Modified: Fri, 03 Mar 2023 19:38:36 GMT  
		Size: 61.5 MB (61484650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31eed947f9147d28c1bc6a76d15bbf2798bc37947f29c7be0c55ff6b3a851d66`  
		Last Modified: Fri, 03 Mar 2023 19:38:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc489393411db1d7439df56d63886c436966bbdbb42b3412825535726274b3`  
		Last Modified: Fri, 03 Mar 2023 19:38:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps-1.11.1.1237-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:056a84af0dec364c62275c4bf694129f992dcb3fe92c6ef0d82fec3a3f4190f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291516725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea8b1b2fbc9e7e69e2a66e0367b3af7dd07df6d50e7e03b47fa10492ebd2804`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:45 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Mar 2023 19:47:11 GMT
ENV CLOJURE_VERSION=1.11.1.1237
# Fri, 03 Mar 2023 19:47:11 GMT
WORKDIR /tmp
# Fri, 03 Mar 2023 19:47:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1cadeebb4ac96c7655f04c60369c6ea69968cc168b44e607df32aac739700751 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 03 Mar 2023 19:47:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Mar 2023 19:47:25 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Mar 2023 19:47:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Mar 2023 19:47:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee23dab4c9395b25d6fc9f10fb3db021a5fb12f2747057b25dfcd66add5df0fd`  
		Last Modified: Wed, 01 Mar 2023 03:19:32 GMT  
		Size: 199.9 MB (199855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb0959609775c25349379dd5acec1dcc8554cb06bb587bb45ce360d36c3808b`  
		Last Modified: Fri, 03 Mar 2023 19:55:39 GMT  
		Size: 61.6 MB (61597691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f5d934f12d4be67b2bef0aca17dcb9e4840e2ce0d6b3378dd43e84bcb84cff`  
		Last Modified: Fri, 03 Mar 2023 19:55:33 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c0c297beb74d7e77cbf3fa409d0a8aadf1c89608ba0ec6f295e91ddcde2b53`  
		Last Modified: Fri, 03 Mar 2023 19:55:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
