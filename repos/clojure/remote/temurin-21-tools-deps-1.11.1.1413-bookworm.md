## `clojure:temurin-21-tools-deps-1.11.1.1413-bookworm`

```console
$ docker pull clojure@sha256:e75b847a9a9b1f99cee326534be8d148c0ee0cef2fbb9de3ea730a409055de79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.1.1413-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6b2a0ca3d4a12065907aeec55e45d2b3f2e145305e1c3c19ddaa2167b6a588f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291539306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd4faf5c16f025cff569aab8699fa144c960e27ab70c90c65b4ade11a96cef9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:26:37 GMT
COPY dir:beb55fdaac250289b56099cc1cfaeaa831b83d06c84fba6631b83f617b38e9e3 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:26:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:39:24 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:39:24 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:39:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:39:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:39:43 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:39:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:39:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22f852b8fd22e21a665af1df7752a2020b022c664cc83027929e2dd78557668`  
		Last Modified: Fri, 13 Oct 2023 01:43:53 GMT  
		Size: 158.6 MB (158590460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d826af09099d5b2ae905ca73d3ab684f0b5efcaabc7221a48c33157fe23e9a8`  
		Last Modified: Fri, 13 Oct 2023 01:52:32 GMT  
		Size: 83.4 MB (83365605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3997fb242eb7128d20df3f5b1f35a2b2f3129ab0ed45020a54778f731c0060ed`  
		Last Modified: Fri, 13 Oct 2023 01:52:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd03ba69a01a8259d0a8e76cc5f07f5ccc7b252a13553912873d06280a7d35f8`  
		Last Modified: Fri, 13 Oct 2023 01:52:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.1.1413-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7d973f7ed2d3bb913dd71dd8a479ab6d819ba7cbf719e8821217119c21f2f56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289574403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3f9b5808fe3d0631e33f182d3808d9ac42de40736c679dbcd491ee2a022d3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:57:56 GMT
COPY dir:dad71274c7bcfed298f99738003c621c42f9777a181dc5466113abef10d5813a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:58:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:09:11 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:09:11 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:09:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:09:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:09:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:09:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:09:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d331f19b05c88fb3c5e4cce50330666ae97dff1cfdcc60262d3635c260452e7`  
		Last Modified: Fri, 13 Oct 2023 01:12:59 GMT  
		Size: 156.8 MB (156842642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3313c21ed7e431e88d66b233a8b1ead20ce14495d8479865393946fac9991af`  
		Last Modified: Fri, 13 Oct 2023 01:20:31 GMT  
		Size: 83.1 MB (83118166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b5ea86837fb403f289ddc2973360dfceb509f23f3bd62bcbb87148a98271ba`  
		Last Modified: Fri, 13 Oct 2023 01:20:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fc2e47ea7bd55dcbc0bd82ffff0e046936df4fb42bd2861f562d081ea1b4dc`  
		Last Modified: Fri, 13 Oct 2023 01:20:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
