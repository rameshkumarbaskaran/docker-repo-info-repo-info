## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:7b968cf80b63b031a29f858b3b949ecac3c77768392f32608e76a193770da6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5f7f17949459829be2e6b01b74a354d0485a10526f650cd729646706fff660c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325338336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e85ed98d277d597981dfe296347c168acb518e66c6ec4539e4d90ec45e6ee4`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:53:31 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:53:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 01:55:33 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 21 Dec 2022 01:55:33 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:24:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 19:24:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:24:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09879893307507e7fe968e99bda720fc4263e5da6b74edf0064ca1f992ab9605`  
		Last Modified: Wed, 21 Dec 2022 02:06:55 GMT  
		Size: 198.5 MB (198454573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3d3be68afd83f0d62fd7c72c83194ca3bc1e653214116509ee17d0bc8d0dbe`  
		Last Modified: Wed, 04 Jan 2023 19:32:24 GMT  
		Size: 71.9 MB (71857978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd064217ff8a23171398b31b14671ad3d0985b622ff0a02e48c111796387dcaf`  
		Last Modified: Wed, 04 Jan 2023 19:32:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37530c6dfb9f92dbbee23105f2286e6f595e1ef376ce9610a8b87202f0b62300
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320865236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62773828b3965a0fae804ff706c3a5d7effa2abe184736911b61989fffb45b2b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 02:20:42 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Wed, 21 Dec 2022 02:20:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:22:34 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 21 Dec 2022 02:22:34 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:43:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 18:43:45 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 18:43:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba82789481f43d21d6d2ece93afb47a4345ba46f2c082c71dcc84a5ef12fb90`  
		Last Modified: Wed, 21 Dec 2022 02:32:16 GMT  
		Size: 195.2 MB (195203346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b4d5e2ec95ef7992d4f28a2c6473b15fc1af93d4e21ec0cc1345ca4dc979ee`  
		Last Modified: Wed, 04 Jan 2023 18:50:38 GMT  
		Size: 72.0 MB (71979475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527c46f6a5230ac423ef55447899e0738acc5bd7d3667465363f94e5109b2b2`  
		Last Modified: Wed, 04 Jan 2023 18:50:31 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
