## `clojure:temurin-11-lein-2.10.0-bookworm-slim`

```console
$ docker pull clojure@sha256:e96e0373cda2ac2d885bad04b29fc6a9e5b5db90471ba00f3f578100ee8a7e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:14f48272722851b03147af9766848b6a157e0d8a111cbca53a2695e9bc02da10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193817363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bd1a44ecb67cd4c78fe4f09f359e8f3b3773c36719a7139b39867cad1e2dab`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:17:46 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:17:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:19:49 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 01 Nov 2023 01:19:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:19:50 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:20:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 01 Nov 2023 01:20:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:20:04 GMT
ENV LEIN_ROOT=1
# Wed, 01 Nov 2023 01:20:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 01 Nov 2023 01:20:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d63825152d5cbdd4aca989095ba3c4b2885c009fca2083969b63ead3b1ec3ae`  
		Last Modified: Wed, 01 Nov 2023 01:36:36 GMT  
		Size: 145.3 MB (145266659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847c6e9456b01478e6bf3908431e56700f7c57b6b880bbf1d296ab96c95fec5`  
		Last Modified: Wed, 01 Nov 2023 01:37:46 GMT  
		Size: 15.0 MB (15001647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee25b1c1fe8335cc67781fe10b55b7d88ff8f391b0ca9e70b07521d3fc793f`  
		Last Modified: Wed, 01 Nov 2023 01:37:45 GMT  
		Size: 4.4 MB (4399221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbe9176cdc24e1139a96bdacafe5493b2c8bae45747cef477d1fb80241b162b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190404193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a27523b8b1473e4bc7030fddfc22950f0c994369843ce07c18f43c5a14198e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:57:22 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:00:18 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 31 Oct 2023 01:00:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:00:18 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:00:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 31 Oct 2023 01:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:00:31 GMT
ENV LEIN_ROOT=1
# Tue, 31 Oct 2023 01:00:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 31 Oct 2023 01:00:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eb29d768a9f4bddddbb15bd2381be6f475f0d817d5b776808080bd9b3d984e`  
		Last Modified: Tue, 31 Oct 2023 01:17:39 GMT  
		Size: 142.0 MB (142001972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab46b58d2ef8baffae5286ef0223060d31d400d12217cea7c60093ab101ceb96`  
		Last Modified: Tue, 31 Oct 2023 01:19:09 GMT  
		Size: 14.8 MB (14823736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3355a6b93165bc03bc39fc119992ba0f105167bc64f5dafc554b444f83c1e37`  
		Last Modified: Tue, 31 Oct 2023 01:19:08 GMT  
		Size: 4.4 MB (4399201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
