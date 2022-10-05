## `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye`

```console
$ docker pull clojure@sha256:cb68eda991a83c44b2571876876b81ab0b0f8eecefa6c239c2d6d40143fe6ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:242d4cf93ac73d279bc6d7a21fc2852c9c226c69f3b458b621220321e09b216d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205856908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d952ce0e174ba291bb5a6c94e0771df9ec24f3d970f3a212e41b761797358`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:30:21 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:32:47 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:32:47 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:33:06 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:33:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:33:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff7f6c810173240005bf7ffb9ab85f81f48ebdf31fbd7f77dfae79e1c463c97`  
		Last Modified: Wed, 05 Oct 2022 01:45:49 GMT  
		Size: 103.5 MB (103513856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77113d852a664c79d0ee3ebd6e2d6a4cce7000183fc4e1f71510b06b9d026f7`  
		Last Modified: Wed, 05 Oct 2022 01:46:49 GMT  
		Size: 47.3 MB (47296185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c734bea734434d25f0aeedc0a227bf0e74a1bb0a83bf6ae175d99d83884010`  
		Last Modified: Wed, 05 Oct 2022 01:46:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1165-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a18ec4bc8f2aab84621b9fd9171253f2f0754896239a3b90111faeb473f2b19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203401632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7019b238fcd26ce5af32267bfece970d2ceb001ce2c0b2e70ace1992140db643`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:17 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:55:52 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 00:55:52 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:56:09 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 00:56:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 00:56:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199e042cfdd7628b0f0e41afb373d86d7e0fb6385396b5a6fc0bec0d3533c7d6`  
		Last Modified: Wed, 05 Oct 2022 01:13:13 GMT  
		Size: 102.6 MB (102613748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1632f0f87c79f80ba5299a7f8e21688385f518258a512c4aeceb636af5de765e`  
		Last Modified: Wed, 05 Oct 2022 01:14:25 GMT  
		Size: 47.1 MB (47086640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e32d84a114c2b2d4ee293e58448f5712c46b2d045d3b9eee883d0e9bd9a0ef`  
		Last Modified: Wed, 05 Oct 2022 01:14:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
