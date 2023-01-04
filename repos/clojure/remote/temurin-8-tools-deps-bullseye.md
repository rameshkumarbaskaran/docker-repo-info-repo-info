## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5ef06c146f0b9dadf4fabe47b65f8a67d41146f15d9bed858ef69f42b3fd45c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2ca3109b6758183fd039942120f4752361f985cbcf1f5d3b3c821393f192ba5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230414609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408d83afba610ea068d5a67a5ba797777d3592f7d03868c3e79196ff96c8e38d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:50:10 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:50:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jan 2023 19:21:44 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 19:21:44 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:22:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 19:22:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:22:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81441fc84c30ecd83d6155d0413d2d8a8941b7d8adaa0d20178da27d0be26b86`  
		Last Modified: Wed, 21 Dec 2022 02:05:09 GMT  
		Size: 103.5 MB (103530611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc94e83a00e8789fad8f7358748b0232631b1b9bbc75c0ce4aa6f1832ee698e`  
		Last Modified: Wed, 04 Jan 2023 19:31:10 GMT  
		Size: 71.9 MB (71858213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1477b33a02f124cb101a30fdcd248f099fe6123ece9bec3d323e16431d2a9af6`  
		Last Modified: Wed, 04 Jan 2023 19:31:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a7b7e3584f24b6b33cd151165aa491da21d7f85fa620db5857f3b1db6d5bd1d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228288209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd380219eecb5e77937406f49b4bd219146a40fbc7fb5854ba90b94c553856f8`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 02:18:06 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Wed, 21 Dec 2022 02:18:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jan 2023 18:41:33 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 18:41:33 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:41:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 18:41:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 18:41:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6100ae9251c3fa47a7e33ea8291f08f02fc3029cfa40a52f572ccce640a5978`  
		Last Modified: Wed, 21 Dec 2022 02:30:41 GMT  
		Size: 102.6 MB (102626555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217fa3f8e12048c0cd3eb87b59403fcb223b05dcd703d0f1c6a8116097f2c79`  
		Last Modified: Wed, 04 Jan 2023 18:49:28 GMT  
		Size: 72.0 MB (71979240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec79c400814f5600d7a32009211416413ba2f7474c4f2979af0677f17cdef08f`  
		Last Modified: Wed, 04 Jan 2023 18:49:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
