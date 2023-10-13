## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:1e0a788bcf7dc1fd20149aaffc3093d4d92df94f6dd58f3ccf82fd639a6dc8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:23579126b25077b8ab38d4f64f9cd4113117f8152a146b78033c0b55867ec527
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206986299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8378991cbb7631c51fe5927756ac8559ae96fb808aa22e4d7aef42638e86af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:38:29 GMT
COPY dir:beb55fdaac250289b56099cc1cfaeaa831b83d06c84fba6631b83f617b38e9e3 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:38:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:38:30 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:38:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:38:31 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:38:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:38:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:38:45 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:38:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:38:48 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:38:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:38:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208ab43c237487605baf510387b0b29fb0f524b14a8049a9b227db54a68aa927`  
		Last Modified: Fri, 13 Oct 2023 01:51:43 GMT  
		Size: 158.6 MB (158590461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbd95ca9a994e0a7de8bbe978c7b035966f11f33af721bcc03e4991a7bc513b`  
		Last Modified: Fri, 13 Oct 2023 01:51:32 GMT  
		Size: 12.6 MB (12578353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba38aaa1216d9911cdb93482647009481927dd92362229793c360aad0b07d78`  
		Last Modified: Fri, 13 Oct 2023 01:51:31 GMT  
		Size: 4.4 MB (4399224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269db31e3f5e4126e946a0284d1747738b49adf8042abf945ba4b7b87165c5c9`  
		Last Modified: Fri, 13 Oct 2023 01:51:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22ffb285975f9ddc609ee5a849387fc409309923c0021957e0f0a7c80e1aa96a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203872104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d95bf70e3b9d1aa7687577389b1dcc4f8cf7db50e6d3e5017af59cda1ed428`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:08:26 GMT
COPY dir:dad71274c7bcfed298f99738003c621c42f9777a181dc5466113abef10d5813a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:08:29 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:08:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:08:29 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:08:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:08:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:08:42 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:08:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:08:45 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:08:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:08:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf91946cf8c604d897f9afcef013c6a42b2544e2a098506c400f62c23965303`  
		Last Modified: Fri, 13 Oct 2023 01:19:57 GMT  
		Size: 156.8 MB (156842642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcb8fd4a2270ca9dcc8d11ac6c32818c4c67435fbe262fe601f2105a4945caf`  
		Last Modified: Fri, 13 Oct 2023 01:19:49 GMT  
		Size: 12.6 MB (12565760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97187bdfd6f28cdee1b95d73767bbb3b1d0e708e37ee0bf132f5b3a02442e28`  
		Last Modified: Fri, 13 Oct 2023 01:19:47 GMT  
		Size: 4.4 MB (4399216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8dc633583cf74a5a35d7a0969c49ce821bf815bced2b0b7c4205c53dda0dd6`  
		Last Modified: Fri, 13 Oct 2023 01:19:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
