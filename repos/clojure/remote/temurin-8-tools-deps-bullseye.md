## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9fd08da797b741f9678bcc802187d861a6f5807331fb9b29c412e51b106e6f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9c4b7e95e97a314ca779f4b9ce544fe38b0f6e06964a0e65d856db37576548b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230753210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbe9802ebe5874b902b5b729a84e5eecba84307e226fba375b08c9d80cb3c2b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:09:29 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:09:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:23:26 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:23:26 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:23:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:23:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340733a9bc147bdf73521b84a2d2eafba8cb7462c33ec7e8d6c8e63126915d10`  
		Last Modified: Tue, 21 Nov 2023 10:29:19 GMT  
		Size: 103.6 MB (103598259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f146f142fd69b55397fce9891eae48c80f53cecae99b9e4778d0e4f057e276b`  
		Last Modified: Tue, 05 Dec 2023 18:36:39 GMT  
		Size: 72.1 MB (72096430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c48f6a5736b7fdce10e2c4dfc3f68bb3685596ccb36743832bebeb0967aaee`  
		Last Modified: Tue, 05 Dec 2023 18:36:31 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c77fe7b70590d93fe45c9073ec59d6d710e4ca9c30e43ad0693f9ca1c27bfd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228625493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48dc149bb6ea2dcaae15a708b3c92257c6f0e16a78519227b0bd30fb0d290ff`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:22:30 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:40:14 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:40:14 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:40:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:40:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:40:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368154bbc0c28d6812f708f5f6016f9d10e7e9305ac7fd1cdd4a216a6df5fd55`  
		Last Modified: Tue, 21 Nov 2023 07:40:29 GMT  
		Size: 102.7 MB (102701584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8dd9c3ada6834adec820843f6cbe01f19f3559fee1e56fb6dbeb69c85dd39e`  
		Last Modified: Tue, 05 Dec 2023 19:51:13 GMT  
		Size: 72.2 MB (72215418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c1f013cac39626813daae0bcc539f17e5bd5decff25646c0290bf1f0b18cca`  
		Last Modified: Tue, 05 Dec 2023 19:51:04 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
