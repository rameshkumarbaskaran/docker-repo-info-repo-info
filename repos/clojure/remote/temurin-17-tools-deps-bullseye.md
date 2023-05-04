## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:46db07664996333e32332b3cfc08dfc041c717086cbd7681a45569602e0bec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:df17c08816696f95b9ac1d466e6b0aeb37532e5711b33c8e736e13cccd8f7a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319510433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea3687c3a955bbb4d8b9a6be194294ee1410290be24ce320cc9802673c904f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:29:34 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 03 May 2023 20:29:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:31:36 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 20:31:36 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:31:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 20:31:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 20:31:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 20:31:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 20:31:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4691a7487ede1e6dd3accb93b84f63e7ba0a18afb5a6dde1cb2605bdef6cce`  
		Last Modified: Wed, 03 May 2023 20:38:14 GMT  
		Size: 192.6 MB (192580399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b948fa5bac2d445fd7c6c55aca1e130a19941fdbc0fcff7f0a2013a73433e4dd`  
		Last Modified: Wed, 03 May 2023 20:39:18 GMT  
		Size: 71.9 MB (71879956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9da316c43f862e11f4fced4492065d8e265cbcbd966e99687330e79cf9a8fb2`  
		Last Modified: Wed, 03 May 2023 20:39:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76204b05ea84e3e122f916abb8baffa29c6693fdef94612b7fb72e09ba97d37c`  
		Last Modified: Wed, 03 May 2023 20:39:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2833d2f7b6ef9d51c7e33d4ee9843fb6814b14fd51a8da345c23148c9a9ff0d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317078298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb514c59936c089c898e224333e1d01657f169376ee56c218685d824bcb3c3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:13:41 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Thu, 04 May 2023 10:13:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 10:15:45 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Thu, 04 May 2023 10:15:45 GMT
WORKDIR /tmp
# Thu, 04 May 2023 10:15:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 May 2023 10:15:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 May 2023 10:15:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 May 2023 10:15:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 May 2023 10:15:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11090c6457d65efbe72f084b567111755856da82721e52490ffc8bec9b85abff`  
		Last Modified: Thu, 04 May 2023 10:22:02 GMT  
		Size: 191.4 MB (191387646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f168c83a8422d55c6a79a7c883938800ff29cfe9b56341647c70d1422a83cc9`  
		Last Modified: Thu, 04 May 2023 10:23:33 GMT  
		Size: 72.0 MB (71996934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbf967c332f2efe74328c078dfc1e349f36c62a8f8a17166c38135431d72e6c`  
		Last Modified: Thu, 04 May 2023 10:23:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9071610704593c366edb7cf8c14ee699bcdfee29c4ce3ac5b227011cce2d0`  
		Last Modified: Thu, 04 May 2023 10:23:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
