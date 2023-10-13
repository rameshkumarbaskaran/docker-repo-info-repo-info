## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:219f96671d1ae9f5036b454e6b45a3f2a13721c175fb9a41f2f7f9296a5d956b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bb876abdb2e461ffc8155cb7d76428f25bfe6a45d6a58a700e9095aba33718f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277724635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1263b14a494cbc2f0980c1477a6e20e82b09e16e84ddc5cd4c57c53d93beab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:34:01 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:34:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:36:13 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:36:13 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:36:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:36:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:36:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:36:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:36:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297dc0c7fb70cdbd48c6c16e128659b9836a465fe2755e7b24f636c965ca5b1`  
		Last Modified: Fri, 13 Oct 2023 01:48:16 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024ab634a549e307f5ad36e7dbd3d98e36c491d549fb55b97af768d755d7b732`  
		Last Modified: Fri, 13 Oct 2023 01:49:26 GMT  
		Size: 83.4 MB (83365662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495ba7c7c010ad58c2f9e894c75d36447f140cbf55e0065c301739a489869f8b`  
		Last Modified: Fri, 13 Oct 2023 01:49:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ceeee8a73992827141fec3ec051bb1779fb85ea03bdf39c5f57acf75f8cf5`  
		Last Modified: Fri, 13 Oct 2023 01:49:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:142fefb325133ab063c1f0befd32f842073f7b0a7490672665248f4c5bb57530
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276275066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8043220bd4889f7d56c2c5d9cf582d25cd83cb5d34069a791cb04dfc03ef3942`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:04:48 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:06:46 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:06:46 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:07:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:07:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:07:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:07:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:07:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c0a26165e5e4720ee0810ab66a47633c5cc6f56db237748131b4b79eaf45df`  
		Last Modified: Fri, 13 Oct 2023 01:16:57 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da72f90cd83b1bd2e1d1e886ec3b0f26914a0768b5256eee7db1a8a71219fe7d`  
		Last Modified: Fri, 13 Oct 2023 01:18:02 GMT  
		Size: 83.1 MB (83117953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a4b204181f1ceff5d1d12cec6aa0a038f614723653b0e2667fcbffb722ec25`  
		Last Modified: Fri, 13 Oct 2023 01:17:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ce45fe7f3b058bdd9f658780a7026881877264f7ae9fdbf278111d03c04a17`  
		Last Modified: Fri, 13 Oct 2023 01:17:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
