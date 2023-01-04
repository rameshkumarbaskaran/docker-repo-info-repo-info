## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:0d4a10a74531041fa065a3ffe0c937df45d3942510fcbb9002a996863c66344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5673ef25dc98517722afb4e073e0e38fe59c55bdbe46d3af61c90ef689ea02b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291327251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d9a536d33fc0b39a891dcde519fc1ff4a69e15d3f4c2a0a8458818c5a17622`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:54:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jan 2023 19:24:23 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 19:24:23 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:24:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 19:24:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:24:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b3a3f45d27e94016fe185e23e24fd68a9307ccd41ac2c3687685a3dfa9cbce`  
		Last Modified: Wed, 04 Jan 2023 19:32:42 GMT  
		Size: 61.5 MB (61475138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6adc9a9f520838080c448ed5b5408d9459f96fe191b9e0ad7026ff27793ad9`  
		Last Modified: Wed, 04 Jan 2023 19:32:34 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d28856a71f86b17d6147644b6b4187720652e074d261f45df1af7e74e5b883d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286845095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f09735fd121505fdef84c8a4ad7b205206669832db48d8b83c245edd7abcd9`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:18:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 02:21:14 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Wed, 21 Dec 2022 02:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jan 2023 18:43:50 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 18:43:51 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:44:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 18:44:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 18:44:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418e472fbc1e675c21a46f7fc728e7299e4becc0622adce50ed53160c548c7f0`  
		Last Modified: Wed, 21 Dec 2022 02:32:36 GMT  
		Size: 195.2 MB (195203361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d23fa8a16190f02af4ee050fdef2e76f4a1e6f6ba3c730ece345a2a2f20e35`  
		Last Modified: Wed, 04 Jan 2023 18:50:55 GMT  
		Size: 61.6 MB (61596344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f2a2961e2f4c4da482f10cbbc28f1677d6ac308b0fd000a31ab42b3ee650c5`  
		Last Modified: Wed, 04 Jan 2023 18:50:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
