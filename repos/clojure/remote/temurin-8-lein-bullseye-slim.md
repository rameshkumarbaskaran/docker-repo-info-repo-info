## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:c7328b284940b0befb2b4d9fa5e4f7a6f80abc9283c6733f857b0a96758e03f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2599af87881931586f1a597bca8bf04b96bdb9f01dd4aa3a2bb9d4c693fad5fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151978150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf83e7d650cdc0039732ce47c0f50cf65bfaeb0924190f2d5b6344e47e76af1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:18:35 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:19:36 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 03:19:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:19:36 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:19:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 03:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:19:50 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 03:19:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 03:19:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a386eaaac993939aefc9356b5f6cc0468dd852762a0b7bb3e195a40c8caf53b`  
		Last Modified: Thu, 07 Sep 2023 03:29:54 GMT  
		Size: 103.6 MB (103585038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40c954484ada46de7476b960f75a3eaa792dc869d9e55b55c6a3387204a152`  
		Last Modified: Thu, 07 Sep 2023 03:30:18 GMT  
		Size: 12.6 MB (12576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f465357b1cd95cba90594820b7418e1e816907c3d332f65dbe13c3f137bd6f8`  
		Last Modified: Thu, 07 Sep 2023 03:30:17 GMT  
		Size: 4.4 MB (4399235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc4af3b897a8b736d4698ad67db968a35674ee7f9d0a28ddfb410b1e15d699d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149716284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f28546e41d56da64af91c3d74f3ec6c10d3b30a103bd0a3461e9c84e3750142`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:46:48 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:46:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 01:47:38 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 01:47:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 01:47:38 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 01:47:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 01:47:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 01:47:51 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 01:47:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 01:47:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab72539caee6a49c911d508260d1eb9ece05d94c06a86d77b415da3e7508716b`  
		Last Modified: Wed, 16 Aug 2023 01:56:31 GMT  
		Size: 102.7 MB (102690456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36896cd9b70f80993f736a59905624698b33eb1679a60d78789167e6f4f51ae7`  
		Last Modified: Wed, 16 Aug 2023 01:56:51 GMT  
		Size: 12.6 MB (12563733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23507b5c4d4fd9d0966bc1235abcb4b2ddcb45bb9311d33e40a0fe9e724670b9`  
		Last Modified: Wed, 16 Aug 2023 01:56:50 GMT  
		Size: 4.4 MB (4399279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
