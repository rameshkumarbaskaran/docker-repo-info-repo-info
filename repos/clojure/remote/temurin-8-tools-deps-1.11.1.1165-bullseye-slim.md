## `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye-slim`

```console
$ docker pull clojure@sha256:a7583cd2dc89783770b9be486f3680c0787e1d83c50bda976884b450a3c68cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:50d84d13b4c55dd3cfc6e9f964a2d4a3e61e817354684076d6f89aa92fc1a872
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196404501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a1510ef5a2d5380e9d606319cdebaf4faa41f21d207bb734bc8ae3f2563db0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:31:08 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:31:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:33:11 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:33:11 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:33:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:33:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:33:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d3b033801fe47b9b71e1e237e407fb11abe76a075f56d43fe9df4833ebe075`  
		Last Modified: Wed, 05 Oct 2022 01:46:08 GMT  
		Size: 103.5 MB (103513854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af4a09e501ed0dd8ba5ddd3c23d81336d8d2014dc70f5d31b70b510756605fe`  
		Last Modified: Wed, 05 Oct 2022 01:47:09 GMT  
		Size: 61.5 MB (61469926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8430d6a4d29de0619194f1d138155d329a26e43b1736e8696327840f0d718d2b`  
		Last Modified: Wed, 05 Oct 2022 01:47:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5797eff26d82da40d7e82c428e5df50d8279ebc2c1b50db7e400a2e445d7b9ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194071584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26db61bbac45079d1e9076368c9ec0a69ddfa6e0e1122d11e93cf427e3d3bf2f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:54 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:56:19 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 00:56:19 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:56:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 00:56:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 00:56:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911611afa665b0683fbe96bda4abb9185fe2c620cdfcc9b8a6381b9fdee36056`  
		Last Modified: Wed, 05 Oct 2022 01:13:35 GMT  
		Size: 102.6 MB (102613711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be159d2e8ac3bb01bce97a65c807aaa806e8dc7647aecfd7debc502bfc1bf345`  
		Last Modified: Wed, 05 Oct 2022 01:14:48 GMT  
		Size: 61.4 MB (61392860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e7c2eaeb4d25b5876c2b5dac80ff55098bd70f1eb0761014456585e870afe0`  
		Last Modified: Wed, 05 Oct 2022 01:14:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
