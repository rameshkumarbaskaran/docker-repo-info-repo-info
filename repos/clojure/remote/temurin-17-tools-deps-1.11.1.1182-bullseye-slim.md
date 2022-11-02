## `clojure:temurin-17-tools-deps-1.11.1.1182-bullseye-slim`

```console
$ docker pull clojure@sha256:3fb8ab40f970ee8adeec92a1efe2895a149abfb081d702b79f7a2d053f63c093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1182-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a128eefa1025a1cce30da052ae28341b874309ef5d90630644279ef0e23f9cf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285031465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07f05ace24f885fd8976e31792fd472b3e61a188a76dba121bd69cb83871bf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:17:36 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:17:36 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:17:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:17:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:17:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:17:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:17:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fefd7ef72e83fff3f8a5489e4e915e6b58b15a62a497936dc9975764becd08`  
		Last Modified: Wed, 02 Nov 2022 20:29:46 GMT  
		Size: 61.5 MB (61472852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eae1869bdcb9f505273be6dd03651de8dfe03e664075ea660fe55b5935d66e`  
		Last Modified: Wed, 02 Nov 2022 20:29:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc45d4307657dff6e7d01fbab962645622eaa993446b7310515a9f3ad6e9f9a7`  
		Last Modified: Wed, 02 Nov 2022 20:29:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1182-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0870c91f0696f6b69ab33e44fdc75d9705be6e3645248ab505399622298a842c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282561598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89753aecb65160a89b77842033bcbd25f92e3a22becee9001c1674e1d929a58a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:50:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:52:35 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:52:35 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:52:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:52:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:52:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:52:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:52:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f131e4b676fce33d3612804b95c85b17fbae6fcdd8aa1aeedad7087ca0d6d37c`  
		Last Modified: Wed, 02 Nov 2022 21:03:26 GMT  
		Size: 61.6 MB (61592577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c7ad47a7cf93a11c95de7a320a1221d7980ee091b85479932af524e0c131ac`  
		Last Modified: Wed, 02 Nov 2022 21:03:20 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756bb39aceed83e87d6ce81a8ba1b8d2fad6672bae20253278c785f76d739d27`  
		Last Modified: Wed, 02 Nov 2022 21:03:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
