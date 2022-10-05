## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:e65aef69995ca8ce0ccd7121cb09a20f68ada7a7078d00a7b980b4eb6b12d47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:46363e8da8a4d960320397e2625608a60cdffd83fbfca68420a277304f2688b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d7cecc2212f7adce7c7dc894b60acec821a7811690bbcf4d259508575cc23`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:33:50 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:36:08 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:36:08 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:36:24 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:36:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:36:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ca2823c2d209cf0f2e558aa4af2216e66a915bea0f57552265e9d46d73fa6`  
		Last Modified: Wed, 05 Oct 2022 01:47:40 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b6cbce32d4b26685b041e7180001fc04a85689852cd0a3db6416c73037678`  
		Last Modified: Wed, 05 Oct 2022 01:48:46 GMT  
		Size: 47.3 MB (47296292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c3876e8feab1c041c9a876d6a476e934311d90bda2e923d7f3aaae16d32a0d`  
		Last Modified: Wed, 05 Oct 2022 01:48:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eda9d6d063d8d6f6056c0732541b3127c47c64b3ca9ad572ffa5506f5dac75e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295655538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f4109e91c94760c6600175417e062296ec2c341cb2eb61099c35c3dbc85ddb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:56:58 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:56:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:59:33 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 00:59:33 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:59:49 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 00:59:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 00:59:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cb3f012989325cc0cd47bb9a1464650ba884c67cba33ababc47396363e616e`  
		Last Modified: Wed, 05 Oct 2022 01:15:43 GMT  
		Size: 194.9 MB (194867814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada9486845754201e7583aa95ea487c8a924b4862595d27198ced7813df72328`  
		Last Modified: Wed, 05 Oct 2022 01:17:01 GMT  
		Size: 47.1 MB (47086481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1ac7f0b518f93f0b74877cde33f6710ec7a09932f31554fadf87d710a7e0`  
		Last Modified: Wed, 05 Oct 2022 01:16:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
