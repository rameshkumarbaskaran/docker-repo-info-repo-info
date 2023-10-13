## `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm-slim`

```console
$ docker pull clojure@sha256:1555a35650acd21453d7e339d71f5cf88e189bfd9e8b9d5751d7ae2f2bd15d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d830c0ddd9e7e985211da8395fc05d2497deef9e5c51c71253134b807d9c4126
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245909639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ffe742269572f20e4edef28cf4c8f2d7819f34afa9f52ece2c3a8487d6103`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:31:21 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:31:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:33:24 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:33:24 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:33:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:33:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:33:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412962c371ae01af0e4de74aef277a006799891be3a74648fb62d23a45c4bd12`  
		Last Modified: Fri, 13 Oct 2023 01:46:40 GMT  
		Size: 144.8 MB (144825953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14ea7d046fe409e80ff3410b72b86796cf50027e64ca45fb955b541ea6c049a`  
		Last Modified: Fri, 13 Oct 2023 01:47:48 GMT  
		Size: 71.9 MB (71933196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ceb4aa83f0dfc9915d04d3e63b2aedcb2dfa96caf370af549cf6afa6033274`  
		Last Modified: Fri, 13 Oct 2023 01:47:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:402770306524ecfea32916bb75c5771a0dd28e49670b8ab7039606047f20b8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242445329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85642c8d45d2aa5c9a9b1fe6e34ab457e221b21c95629170c6a39e72a9706b18`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:02:37 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:02:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:04:21 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:04:21 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:04:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:04:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:04:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf8838260c53d4485d9e40a2d582068c148705388c2ee8a2041f88176fbce32`  
		Last Modified: Fri, 13 Oct 2023 01:15:24 GMT  
		Size: 141.6 MB (141570687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51aeea397f5e324cd303dcedfd69a59bbff48027ed591aaae8f6594dcc979b7`  
		Last Modified: Fri, 13 Oct 2023 01:16:29 GMT  
		Size: 71.7 MB (71694741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34eabd286a7aa91ffa1dcd0533802cb405e3271c24925b59f1136e6cd6241d24`  
		Last Modified: Fri, 13 Oct 2023 01:16:23 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
