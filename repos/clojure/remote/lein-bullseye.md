## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:ab1d6ca23eb48f50f241dee7871d9de98e87188db9b282e58ab4438ed0688fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6dac47876b99f7989ef8440fbe13aaa89c1945090a7b44b1b7915f5462d5b056
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231915357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36baa81fb05585439994a151804e310542ce24f6c7623847597e1accfe9a812`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:37:54 GMT
COPY dir:beb55fdaac250289b56099cc1cfaeaa831b83d06c84fba6631b83f617b38e9e3 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:37:56 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:37:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:37:56 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:38:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:38:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:38:17 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:38:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:38:20 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:38:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:38:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ccf8356cd78d17de08939bf431ff53640e4ca43a1c706c57dda171ef72ce95`  
		Last Modified: Fri, 13 Oct 2023 01:51:17 GMT  
		Size: 158.6 MB (158590466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bfc8779b5975166d89534f1dccb2ea90930076dff4b1082e1fabc4b1983a78`  
		Last Modified: Fri, 13 Oct 2023 01:51:05 GMT  
		Size: 13.9 MB (13867224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78e93f1cca27459b10b125dc1d33e86d6a2183f315688a4a630853d29154e4`  
		Last Modified: Fri, 13 Oct 2023 01:51:05 GMT  
		Size: 4.4 MB (4399239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29a6ee254a15fa6e53a47717b4360fac9aba1a5d70b6aa66bf7da73b57a147`  
		Last Modified: Fri, 13 Oct 2023 01:51:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f30446c13249c8b3ec2a1ab7e74403d448b5efa0dccbf37dc8affbff63be0eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228806046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154da09fb2505222e6387f8a735df5e562fd36859f7807511eba783791d66828`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:07:57 GMT
COPY dir:dad71274c7bcfed298f99738003c621c42f9777a181dc5466113abef10d5813a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:08:01 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:08:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:08:01 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:08:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:08:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:08:17 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:08:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:08:19 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:08:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:08:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bb21e1699c7611a27c62ff66a5d51660858083a8120d9058d3a4a18060f4a`  
		Last Modified: Fri, 13 Oct 2023 01:19:33 GMT  
		Size: 156.8 MB (156842643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ad14a040dd092807377f1540caf1e9cadf237819662f7c114c1d1e237e508`  
		Last Modified: Fri, 13 Oct 2023 01:19:23 GMT  
		Size: 13.9 MB (13855904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9f1eacb9cbe37c7f2664fbe8591f43157812b28f4788dfa8bb5fa5e90496df`  
		Last Modified: Fri, 13 Oct 2023 01:19:22 GMT  
		Size: 4.4 MB (4399289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d4403ce4975fecf2377c71f1325771e763389d906b9a27ae4d1d5e60a97cf4`  
		Last Modified: Fri, 13 Oct 2023 01:19:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
