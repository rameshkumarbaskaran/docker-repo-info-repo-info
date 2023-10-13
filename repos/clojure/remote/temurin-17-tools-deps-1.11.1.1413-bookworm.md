## `clojure:temurin-17-tools-deps-1.11.1.1413-bookworm`

```console
$ docker pull clojure@sha256:50deb64190ef5442fd75a3c3ee095fe8489832b5609dbb4e42b1c4e3cd75f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4ccf04ce3044a492a60f7245d384523bc070e8afe89543378f07e86fa2aca400
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277724061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653e37dca9fec04e0a72abe82a474caf3d2e12d565073c4747d15fbd167c0f17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:52:06 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:52:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:57:47 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 12:57:47 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:58:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 12:58:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 12:58:06 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:58:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:58:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f6291b22d70cff059b865d89b1554735b685fb268c97387261bac2bd8f0ee2`  
		Last Modified: Fri, 13 Oct 2023 13:09:53 GMT  
		Size: 144.8 MB (144775717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42efc956e0296233576971da4351a8edd5199abf4e554d12a46ee41229112432`  
		Last Modified: Fri, 13 Oct 2023 13:13:02 GMT  
		Size: 83.4 MB (83365103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878fcfc816f5ca55c42958ee1e8d8fbb900cd3295aa2a7210fe7416ef52b5f3`  
		Last Modified: Fri, 13 Oct 2023 13:12:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9b555ba76fcd2c88885c4f7c1941cf035e4113edf0f445d5078e18a5a03f5d`  
		Last Modified: Fri, 13 Oct 2023 13:12:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1413-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:48dec6dafc60d5a35e5bb707c14c963936f9a073de8cb91dbacf2c8b8b194c87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276275066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abff8481c4cc0591147ecb46d1385b2fe41efff159d421891ae35eed43a00bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:18:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:23:17 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 10:23:17 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:23:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 10:23:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 10:23:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:23:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:23:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d651a3fb90463baef37e8108569d81355c0974d68da3cce0e70482f66c93d`  
		Last Modified: Fri, 13 Oct 2023 10:34:04 GMT  
		Size: 143.5 MB (143543493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb06338cd24a201c4c7ea4ad01018de818e34b6d32991e693acb828dfa341ed`  
		Last Modified: Fri, 13 Oct 2023 10:38:02 GMT  
		Size: 83.1 MB (83117980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae72942548e75f2b29d85e67b4d626fc78d98ae65276761ba14a858aa6e4ace`  
		Last Modified: Fri, 13 Oct 2023 10:37:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9d78b5ad7b5754ee9ffef8c3cd13da02544fca6de6c82fb60065792a158168`  
		Last Modified: Fri, 13 Oct 2023 10:37:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
