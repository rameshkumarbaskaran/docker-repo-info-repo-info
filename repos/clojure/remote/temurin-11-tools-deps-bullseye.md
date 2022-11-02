## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a8ef8d5b539323417d90aafd8a175ac325e00d0f6e1c5b10ba0e04c7971f239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9f644877f6dd2cbaa6e1ba3851a4bb2a9c16c5e0c3950b46ba225e5331f4990e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300472570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f9a9c78af4bb75b0e24e75532afdc7b4ef6ffa25737b61411b2736670074b0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:10:35 GMT
COPY dir:24028fba84faa85b57bc32be14abf8fad6a4bd4db557cb5499b6d5cf38d97646 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:10:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:13:35 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:13:35 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:13:55 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:13:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:13:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcd28620e58cb67f5c8f9e27eae0508ebb1bd7db0a5e05838b142166ca46960`  
		Last Modified: Wed, 02 Nov 2022 20:24:27 GMT  
		Size: 198.1 MB (198124725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365c825fd2f20d20bada9bc86af57acfaf9ff5dd524110bd2e703fad09c8eb54`  
		Last Modified: Wed, 02 Nov 2022 20:26:08 GMT  
		Size: 47.3 MB (47300894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f472970f518b3f5ae67631b442f40235bd3776bb2d6f7de572261542664bcc8c`  
		Last Modified: Wed, 02 Nov 2022 20:26:03 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce892b66745b58b39f64a70b522bb27cfb012a0846e0b42905da4017ab77c0ce
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295864448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7852ad26e69b43e3a42a60a6f084a45f5c45a8dae8f28da2cb2206bae53b3a6b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:46:38 GMT
COPY dir:e48336735658172388295f760b71f5f10a9b7d3f960c6e4546718a38dd6452e7 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:46:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:49:12 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:49:12 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:49:26 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:49:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:49:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea5981601b157d45e631f4fdac4fdd41f2d6daaa8c619fc62dfe32805bfb784`  
		Last Modified: Wed, 02 Nov 2022 20:58:15 GMT  
		Size: 194.9 MB (194867680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ab7f18b43bb17ee2c532eaceadad8c0e0c7b1b923678414dea2367999ab744`  
		Last Modified: Wed, 02 Nov 2022 20:59:52 GMT  
		Size: 47.3 MB (47294184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5465a6833cc2ddee4ab6a80c58eff9e4fbe723c9b341d4ebe9aceeb60862000`  
		Last Modified: Wed, 02 Nov 2022 20:59:41 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
