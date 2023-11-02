## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:510b97ed64f7f040a762b1c4fe1044a742a2f37c141ad431d0bc205f723f8922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e07dfd8337d0da809ea84f543a5918f5b01ef0edda6dad6e3c240def6a0c46e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230558180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb62bf64c627359f4dfc716b44a64ea4b7b1eb165fb6d22f9e5c46405afc19a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:51:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:51:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:56:34 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 02 Nov 2023 01:56:34 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:56:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 02 Nov 2023 01:56:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Nov 2023 01:56:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae3bc407ed44ee4c19e2acfaafba1a8237df1bc1f1bca7853c10d12070957d`  
		Last Modified: Thu, 02 Nov 2023 02:03:16 GMT  
		Size: 103.6 MB (103598251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5306ae1ef7a3203f79c786da8c3884ca798c871eab0e49d280de095eb259b8b0`  
		Last Modified: Thu, 02 Nov 2023 02:06:39 GMT  
		Size: 71.9 MB (71901259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5268841c693a8c15be517f980ebb4ef5eb32caa5bd60fc13b3f41fc385d7836`  
		Last Modified: Thu, 02 Nov 2023 02:06:32 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eaa875eab72bbcd9fb4f8a5385603d5261c470802bf7c7043fcc2fc7b415d8d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228416047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd19143fdbd0e9cd813358998d614cbc8753b374aff491c2d0f411af65bc21a7`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:22:50 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:25:48 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 02:25:48 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:26:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 02:26:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 02:26:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003c7122229a80b7dbbe3dace4e128ac86e5fd13e14a350774520e4719b064f`  
		Last Modified: Wed, 01 Nov 2023 02:41:39 GMT  
		Size: 102.7 MB (102690456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715ba5b126706d80ca59b435f3971eb241b559218705e431c413f601d24ffefc`  
		Last Modified: Wed, 01 Nov 2023 02:43:33 GMT  
		Size: 72.0 MB (72017216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1332d01531adf190f37ed31abed272fd68681cb79ddb250238429c6498706ec8`  
		Last Modified: Wed, 01 Nov 2023 02:43:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
