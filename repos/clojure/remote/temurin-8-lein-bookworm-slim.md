## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:202dc899efc860df53e235690d2d15f59d1df3c33f117a823cad312dfde8c795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5bed526873184242f35749c82df3dcb3bdfd556c33cdca23e2c346b9a9f845fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152148968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a31c06a700b2fa697215df083c1dbc63fd67958aaee35e1814bbf90d122379`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:50:31 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:50:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:53:39 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 01:53:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:53:39 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:53:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 Nov 2023 01:53:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:53:53 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 01:53:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 01:53:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a218e9c40dab330f555e00fbdf54bbc4a1c72977e72f15e20a344c6eb36f3`  
		Last Modified: Thu, 02 Nov 2023 02:02:58 GMT  
		Size: 103.6 MB (103598265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5369c8acd4ea34fcec590de0040ed7a527a7696da24f194964d6c34d86de5cb`  
		Last Modified: Thu, 02 Nov 2023 02:04:39 GMT  
		Size: 15.0 MB (15001645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e9976ddf8bad74272782b95163cc80f2009211189666ac9235def576a3621`  
		Last Modified: Thu, 02 Nov 2023 02:04:39 GMT  
		Size: 4.4 MB (4399222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d63159c14c9d8975051217165aae75ce1ddd570b3be63d77f8558e11216fcd64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151103705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474688d63a14437b00f02ea2427d0a0fba0154b2ade54169963f2894c29d930e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:28:42 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:28:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:31:27 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 03:31:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:31:27 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:31:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 Nov 2023 03:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:31:40 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 03:31:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 03:31:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b95ba4f42cf700bc15c43f945df7888a3f1517eba974a7407a4876a247f3eb1`  
		Last Modified: Thu, 02 Nov 2023 03:38:23 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070065e7bf5ad3040750c168fbb39283cf3b2dad16b2bce5493810037029cbbb`  
		Last Modified: Thu, 02 Nov 2023 03:39:48 GMT  
		Size: 14.8 MB (14823797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fbebf29bd93e34e1b598b73e09dc7d37e72c1714c51fc08bdc34ba614dbae6`  
		Last Modified: Thu, 02 Nov 2023 03:39:47 GMT  
		Size: 4.4 MB (4399258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
